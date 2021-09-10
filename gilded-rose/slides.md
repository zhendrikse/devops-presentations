## The Gilded Rose kata

by [Zeger Hendrikse](https://www.it-essence.nl/)

---
![Goals](./images/goals.png)
<ul>
<div>
<li>Explain various refactoring techniques</li>
</div> 
<div class="fragment">
<li>Learn to refactor in <em><b>small</b></em> steps</li>
</div> 
<div class="fragment">
<li>The one and only useful use of code coverage</li>
</div> 
</ul>

---

### [Martin Fowler](https://martinfowler.com/): good programmers

![Martin Fowler](./images/fowler.jpg)

A fool can write code that a computer can understand.
Good programmers write code that humans can understand.

---

### [Gilded Rose kata](https://github.com/emilybache/GildedRose-Refactoring-Kata)

Store where goods degrade in quality as they approach their sell date

(Prerequisite: [approval testing](../approval-testing/slides.md))

---

#### System updates items daily

* `SellIn` = number of days left to sell the item
* `Quality` = how valuable the item is
* At the end of each day both values are lowered

---

#### Task: add a new category of items

* "Conjured" items degrade in `Quality` twice as fast as normal items

---

<iframe frameborder="0" width="100%" height="500px" src="https://replit.com/@zwh/GildedRosePython?lite=false"></iframe>

---

### 😱 How do I even begin 😱 

```python
def update_quality(self):
  for item in self.items:
    if item.name != "Aged Brie" and item.name != "Backstage passes to a TAFKAL80ETC concert":
      if item.quality > 0:
        if item.name != "Sulfuras, Hand of Ragnaros":
          item.quality = item.quality - 1
    else:
      if item.quality < 50:
        item.quality = item.quality + 1
        if item.name == "Backstage passes to a TAFKAL80ETC concert":
          if item.sell_in < 11:
            if item.quality < 50:
              item.quality = item.quality + 1
...
```
---

### [Extract method](https://wiki.c2.com/?ExtractMethod)

- Turn the fragment into a method whose name explains the purpose of the method

  ```python
  def update_quality(self):
    for item in self.items:
      update_item_quality(item)
  ```

---

### [Refactor Negate If](https://wiki.c2.com/?RefactorNegateIf)

- Eliminate negate and "flip" the conditional

  ```python
  if item.name == "Aged Brie" or item.name == "Backstage passes to a TAFKAL80ETC concert":
  ```
---

### [Lift-Up Conditional](https://www.eficode.com/blog/advanced-testing-refactoring-techniques-2) &mdash; step 1

- Create temporary `foo(self, item)` with all logic

  ```python
  def update_item_quality(self, item):
    self.foo(item)

  def foo(self, item):
    if item.name == "Aged Brie" or item.name == "Backstage passes to a TAFKAL80ETC concert":
    ...
  ```
---

### [Lift-Up Conditional](https://www.eficode.com/blog/advanced-testing-refactoring-techniques-2) &mdash; step 2
  
- Add conditional

  ```python
  def update_item_quality(self, item):
    if item.name == "Aged Brie":
      self.foo(item)
    else: 
      self.foo(item)
  ```

---

### [Lift-Up Conditional](https://www.eficode.com/blog/advanced-testing-refactoring-techniques-2) &mdash; step 3
  
<ol>
<div>
<li>Inline `foo()`, run and inspect coverage!</li>
</div>
<div class="fragment">
<li>Remove dead code</li>
</div>
<div class="fragment">
<li>Inspect coverage of conditionals</li>
  <ul>
    <li>Hover over to see more details</li>
    <li>Remove dead branches</li>
  </ul>
</div>
<div class="fragment">
<li>Take out "Agred Brie" from `else`-clause</li>
</div>
</ol>

---

### Rinse and repeat 

Do the same for the `else`-branch of "Aged Brie"

```python
else:
  if item.name == "Backstage passes to a TAFKAL80ETC concert":
    self.foo(item)
  else:
    self.foo(item)
```

---

### Rinse and repeat 

Do the same for the `else`-branch of "Backstage passes to a TAFKAL80ETC concert"

```python
else:
  if item.name == "Sulfuras, Hand of Ragnaros":
    self.foo(item)
  else:
    self.foo(item)
```

---

### Rearrange if-then-else

```python
if item.name == "Aged Brie":
  ...
elif item.name == "Backstage passes to a TAFKAL80ETC concert":
  ...
else:
  if item.name != "Sulfuras, Hand of Ragnaros":
    ...
```

---

### [Refactor Negate If](https://wiki.c2.com/?RefactorNegateIf)

```python
if item.name == "Aged Brie":
  ...
elif item.name == "Backstage passes to a TAFKAL80ETC concert":
  ...
elif item.name == "Sulfuras, Hand of Ragnaros":
  pass
else:
  ...

```

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

