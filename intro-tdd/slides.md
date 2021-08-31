#### Coders should test

### Testers should code

## We all should do TDD!

by [Zeger Hendrikse](https://www.it-essence.nl/)

---

### With special thanks to ...

![Uncle Bob](./images/unclebob.gif)

---
![Goals](./images/goals.png)
<ul>
<div>
<li>Coding + testing are the same activity</li>
</div>
<div class="fragment">
<li>See how TDD is done <em>in practice</em></li>
</div> 
<div class="fragment">
<li>Motivation to learn & practice more TDD</li>
</div> 
</ul>

---
### Rulez during this session

<ul>
<div>
<li>Questions are allowed at all times</li>
</div>
<div class="fragment">
<li>
The goal is to illustrate <i>the TDD process</i>
  <ul>
  <li>The goal is <em>not</em> to write the best
    <ul>
    <li>Javascript ever</li>
    <li>Python ever</li>
    <li>...</li>
    </ul>
   </li>
   <li>User story is not the most realistic either</li>
</li>
</div>

---

### Rulez of the TDD game

<table>
  <colgroup>
    <col span="1" style="width: 60%;"/>
    <col span="1" style="width: 40%;"/>
  </colgroup>
			         
  <tbody><tr>
    <td>
      <img alt="Red Green Refactor" src="./images/redgreenrefactor.png"/>
    </td>
    <td>
      <ol>
        <li>Write a failing test</li>
        <li>Make it pass</li>
        <li>Refactor relentlessly</li>
      </ol>
    </td>
  </tr></tbody>
</table>

---

### Rulez of the TDD game

**Small increments**, so we are [not allowed to write](http://blog.cleancoder.com/uncle-bob/2014/12/17/TheCyclesOfTDD.html)
<ol>
  <div class="fragment">
    <li>any code unless it is to make a failing test pass</li>
  </div>
  <div class="fragment">
    <li>any more of a test than is sufficient to fail (also compilation!)</li>
  </div>
  <div class="fragment">
    <li>any more code than is sufficient to pass the one failing unit test</li>
  </div>
</ol>
---

### Kent Beck

![Kent Beck](./images/kentbeck.jpg)

---
### <a href="https://en.wikipedia.org/wiki/Kent_Beck">Kent Beck's</a> [design rules](https://martinfowler.com/bliki/BeckDesignRules.html)

1. Passes the tests
2. Reveals intention ([Clean code](https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29))
3. No duplication ([DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself))
4. Fewest elements (<a href="http://wiki.c2.com/?DoTheSimplestThingThatCouldPossiblyWork">Simplest thing that could possibly work</a>)

---

### Who is doing what

<ul>
<div>
<li>Do you write unit test afterwards</li>
</div>
<div class="fragment">
<li>Do you write unit test beforehand</li>
</div>
<div class="fragment">
<li>Do you do TDD</li>
</div>
</ul>

---

### TDD is not building a bridge nor house!

![cartoon](./images/tdd_cartoon.png)

---

### User story

<div style="text-align: left">
<b>As</b> a worker in a restaurant 

<b>I want</b> to place my clean plates on a stack 

<b>so that</b> I always have plates available to serve dishes
<div>

---

#### Plans are worthless ...

### ... but planning is essential:

- Start with an empty stack
- Define pop on an empty stack
- Define push on an empty stack
- Define pop on a non-empty stack
- Define multiple pushes and pops

&nbsp;

<div class="fragment">
Credits to <a href="http://barbra-coco.dyndns.org/yuri/Kent_Beck_TDD.pdf">Kent Beck</a> and <a href="https://quoteinvestigator.com/2017/11/18/planning/">Eisenhower</a>!
</div>

---

### Let's do this

- Let's do this [in Javascript](./javascript/slides.md)!
- Let's do this [in Python](./python/index.html)!
- Let's do this [in Typescript](./typescript/index.html)!
- Let's do this in Java
- Let's do this in C#
- Let's do this in C++

---

### Retrospective

<ul>
<div>
<li><a href="http://blog.cleancoder.com/uncle-bob/2014/12/17/TheCyclesOfTDD.html">Tests become more <i>specific</i>, code more <i>generic</i></a></li>
</div>
<div class="fragment">
<li><a href="../ci-tbd/index.html">TBD</a> is a no-brainer</li>
</div>
<div class="fragment">
<li>Difficulty is postponing "the gold"</li>
</div>
<div class="fragment">
<li><a href="https://blog.cleancoder.com/uncle-bob/2017/10/03/TestContravariance.html">Contravariant test suites</a></li>
</div>
<div class="fragment">
<li>1, 2, N</li>
</div>
<div class="fragment">
<li>Tests grouped according to shared set-up</li>
</div>
<div class="fragment">
<li>What is still left to test?</li>
</div>
</ul>

---

### It's only the beginning...

<ul>
<div>
<li><a href="https://martinfowler.com/articles/mocksArentStubs.html">Mocks, stubs, fakes, spies, ...</a></li>
</div>
<div class="fragment">
<li><a href="https://khalilstemmler.com/articles/software-design-architecture/organizing-app-logic/">The Clean Architecture</a>: how to cope with dependencies on external systems</li>
</div>
<div class="fragment">
<li><a href="https://blog.devgenius.io/detroit-and-london-schools-of-test-driven-development-3d2f8dca71e5">London vs Detroit schools of TDD</a></li>
</div>
<div class="fragment">
<li>Developer tests his own code: <a href="../four-eyes/index.html">the nightmare of every auditor!</a></li>
</div>
</ul>

---
### Resources

- Kent Beck, [Test-Driven Development By Example](http://barbra-coco.dyndns.org/yuri/Kent_Beck_TDD.pdf) 
- [QWAN’s Little Book of Test Driven Development](tdd-booklet.pdf)
- ...