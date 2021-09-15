<section data-background-image="./images/clay-banks-a9kHtTbjpwY-unsplash.jpg" style="color:black;">

<h3 style="color: black;">Refactoring Legacy Code</h3>

<h2 style="color: black;">Using approval testing</h2>

by [Zeger Hendrikse](https://www.it-essence.nl/)

&nbsp;

&nbsp;

&nbsp;

&nbsp;

</section>

---
![Goals](./images/goals.png)
<ul>
<div>
<li>Learn about legacy code</li>
</div> 
<div class="fragment">
<li>Learn about approval testing</li>
</div>
<div class="fragment">
<li>When to use it and when not</li>
</div> 
</ul>

&nbsp;

&nbsp;

&nbsp;


---

![Michael Feathers](./images/legacy_code.png)

> To me, legacy code is simply code without tests &#8212; [Michael Feathers](https://www.goodreads.com/book/show/44919.Working_Effectively_with_Legacy_Code)

---

### Or even better...

> Legacy Code is valuable code you’re afraid to change &#8212; [Nicolas Carlo](https://understandlegacycode.com/blog/what-is-legacy-code-is-it-code-without-tests/)

---

### 😱 But we need to modify it 😱 


![Question](./images/hiclipart.com.png)

---

### [The naive](https://github.com/nicoespeon/talk-how-to-change-untested-code): Edit and Pray 🙏

1. Edit the code
2. Test manually
3. Pray you didn't broke anything

&nbsp;
<div class="fragment">
Drawbacks: very risky &amp; stressful
</div>

---

### [The ideal](https://github.com/nicoespeon/talk-how-to-change-untested-code): Write the damn tests ✅

1. Reverse engineer the specs from the code
2. Write automated tests
3. Refactor the code
4. Add your feature

&nbsp;
<div class="fragment">
Drawbacks: very costly and sl-o-o-o-w...
</div>

---
### [The pragmatic](https://github.com/nicoespeon/talk-how-to-change-untested-code): Approval tests 💁

1. 📸 Generate an output you can snapshot
2. ✅ Use test coverage to find all input combinations
3. 👽 Use mutations to verify your snapshots

---

### [Approval tests](https://approvaltests.com/)

Also known as

- Characterization Tests
- Golden Master
- Snapshot Tests
- Locking Tests
- Regression Tests
---

### What we are going to test

```python
class Calculator():
  @staticmethod
  def addNumbers(x: int, y: int) -> int:
    return x + y
```

---

### How we verify

```python
import unittest
from approvaltests.approvals import verify
from calculator import Calculator

class CalculatorTest(unittest.TestCase):

  def test_main(self):
    # ARRANGE
    x: int = 1
    y: int = 2;
    # ACT
    result = Calculator.addNumbers(x, y)
    # APPROVE
    verify(result)
```

---

### Even with combinatorial tests 🤩

```python
...
from approvaltests.combination_approvals import verify_all_combinations

class CalculatorTest(unittest.TestCase):

  def test_add_combinatorial(self):
    verify_all_combinations( Calculator.addNumbers, [[1,2], [4,3]])
```

---

<iframe frameborder="0" width="100%" height="500px" src="https://replit.com/@zwh/ApprovalTestDemo-1?lite=false"></iframe>

---

### Approval testing [use cases](file://solon.prd/files/P/Global/Users/C65923/UserData/Downloads/raid_informaatika_2021.pdf)

- Code without tests that needs to be changed
- APIs that return JSON or XML
- Complex return objects
- Strings longer than one line
---

### [You should NOT keep these tests](https://github.com/nicoespeon/talk-how-to-change-untested-code)

Problems:

<ul>
<div>
  <li>Existing behavior is captured, bugs included</li>
</div>
<div class="fragment">
  <li>Tests will fail whenever behavior changes. Noisy!</li>
</div>
<div class="fragment">
  <li>People will get used to just update them</li>
</div>
<div class="fragment">
  <li>You can't read them to understand what the code does</li>
</div>
<div class="fragment">
  <li>Delete them or have a plan to replace them with unit tests.</li>
</div>
</ul>


---
### Retrospective

<ul>
<div>
<li><a href="https://martinfowler.com/articles/mocksArentStubs.html">Mocks, stubs, fakes, spies, ...</a></li>
</div>
<div class="fragment">
<li><a href="https://khalilstemmler.com/articles/software-design-architecture/organizing-app-logic/">The Clean Architecture</a>: how to cope with dependencies on external systems</li>
</div>
<div class="fragment">
<li><a href="https://blog.devgenius.io/detroit-and-london-schools-of-test-driven-development-3d2f8dca71e5">London school / Detroit schools</a></li>
</div>
<div class="fragment">
<li>Developer tests his own code: <a href="../four-eyes/index.html">the nightmare of every auditor!</a></li>
</div>
</ul>

