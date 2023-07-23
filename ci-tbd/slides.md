<section data-background-image="./images/edward-howell-yl6xgqD3X14-unsplash.jpg">

## Trunk Based Development

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

</section>

---

![Zeger](./images/zeger_profile.jpg)

Zeger Hendrikse

DevOps coach

---

### Warming up: first question

#### What does CI mean?


* **A**: Continuous Improvement
* **B**: Continuous Integration <font style="color: green;">&#10004;</font><!-- .element: class="fragment"-->
* **C**: Continuous Inspection
* **D**: Continuous Insights


---

### Context: three ways of DevOps

![First way](./images/DevOps1.png)
<!-- .element: class="fragment"-->

![Second way](./images/DevOps2.png)
<!-- .element: class="fragment"-->

![Third way](./images/DevOps3.png)
<!-- .element: class="fragment"-->

---

### Warming up: second question

#### What does CD mean?

* **A**: Continuous Delivery <font style="color: green;">&#10004;</font><!-- .element: class="fragment"-->
* **B**: Continuous Development
* **A**: Continuous Deployment <font style="color: green;">&#10004;</font><!-- .element: class="fragment"-->
* **D**: Continuous Design

---

### CI in the context of CD

<div class="r-stack">
  <img class="fragment" src="./images/cicd-overview-1.png" />
  <img class="fragment" src="./images/cicd-overview-2.png" />
  <img class="fragment" src="./images/cicd-overview-3.png" />
  <img class="fragment" src="./images/cicd-overview-4.png" />
  <img class="fragment" src="./images/cicd-overview-5.png" />
</div>

---

### First question: CI practice

#### What is **not** a CI best practice?

* **A**: Deploy & test the code to a test environment <font style="color: green;">&#10004;</font><!-- .element: class="fragment"-->
* **B**: Keep the build fast
* **C**: Everyone commits to the baseline everyday
* **D**: When the build fails, everybody stops to fix it

---

### Second question: version control

#### What is the primary purpose of a VCS?

* **A**: Facilitate roll backs and roll forwards
* **B**: Facilitate seamless branching and merging
* **C**: Facilitate communication and collaboration <font style="color: green;">&#10004;</font><!-- .element: class="fragment"-->
* **D**: Facilitate a central back-up of source code

---

#### Do you practice Continuous Integration?

<div class="r-stack">
  <img class="fragment" src="./images/what_is_ci_1.png" />
  <img class="fragment" src="./images/what_is_ci_2.png" />
  <img class="fragment" src="./images/what_is_ci_3.png" />
</div>


---

### Third question: amplify feedback loops

#### Which is the odd one out?

* **A** Integrate early and often
* **B** Small batch size (containing changes)
* **C** Pair programming
* **D** Pull requests <font style="color: green;">&#10004;</font><!-- .element: class="fragment"-->

---

### Which branching strategy should I choose?

![Choose](./images/pngwing.com.png)

---

### So right off the bat ...

[![Branching](./images/dontBranch.jpg)](https://www.davefarley.net/?p=247)

---

### The Big Controversy

![Dave](./images/davefarley.jpg)

> [...] I get “Heretic, burn him at the stake” kind of feedback [...] &mdash; [Dave Farley](https://www.davefarley.net/?p=247)

---

### What do we usually see?

![branches](./images/branches_intro.png)

---

### The Death 

![death](./images/hiclipart.com.png)

### of Continuous Integration

---

### Negative effects of branches

- <!-- .element: class="fragment"-->
  Delays integration 
  <!-- .element: class="fragment"-->
  - Slower feedback loops
  <!-- .element: class="fragment"-->
  - Kills continuous integration
  <!-- .element: class="fragment"-->

- <!-- .element: class="fragment"-->
  Increased change batch size
  <!-- .element: class="fragment"-->
  - Slower feedback loops
  <!-- .element: class="fragment"-->
  - Decreased deployment frequency
  <!-- .element: class="fragment"-->

- <!-- .element: class="fragment"-->
  Kills communication 
  <!-- .element: class="fragment"-->
  - Headphone/hero developers!
  <!-- .element: class="fragment"-->

---

![Jez](./images/jezhumble.jpg)

> _The trunk-based development is all about communication. We use version_
  _control to communicate what we're doing to the rest of the team. To do it_
  _regularly enough, we have to work in very small batches._ [Jez Humble](https://github.com/rht-labs/enablement-docs/issues/123)

---

### State of DevOps report

[![TBD](./images/organizational_performance.jpg)](https://www.thoughtworks.com/insights/blog/enabling-trunk-based-development-deployment-pipelines)

---

### Trunk Based Development (TBD)

- <!-- .element: class="fragment"-->
  **Small commits** (approx 10 - 15 lines)
- <!-- .element: class="fragment"-->
  Commits (_self contained_ and _consistent_) include production and test code
- <!-- .element: class="fragment"-->
  Always commit and push together
- <!-- .element: class="fragment"-->
  **No** branches (except for spikes)
- <!-- .element: class="fragment"-->
  Review [early and synchronously](http://allankelly.blogspot.co.uk/2015/03/code-and-other-reviews-small-piece-of.html)

---

### TBD in action

![branches](./images/tbd_in_action.png)

---

#### More objections: the usual suspects...

![Dave](./images/davefarley.jpg)

> _At one extreme I get “Heretic, burn him at the stake” kind of feedback, at_
  _the other “Yes, but it can’t possibly work without Feature Branching – you must_
  _work in small teams and/or on trivially simple projects”._ &mdash; [Dave Farley](https://www.davefarley.net/?p=247)

---

### I am (frequently) pulling from the mainline!

---

### TDB: small and frequent commits

#### Low-frequency integration

![Merging](./images/merge_1.png)

Suppose S1 and V1 contain a merge conflict...

---

### TDB: small and frequent commits

#### Low-frequency integration

![Merging](./images/merge_2.png)

... merge conflicts are late and big!

---

### TDB: small and frequent commits

#### High-frequency integration

![Merging](./images/merge_3.png)

Suppose S1 and V1 contain a merge conflict...

---

### TBD: small and frequent commits

#### High-frequency integration

![Merging](./images/merge_4.png)

... merge conflicts are small and early!

---

#### But how about (major) refactorings?

##### Branching by abstraction, step 1

![BBA](./images/bba-step-1.png)

---

#### But how about (major) refactorings?

##### Branching by abstraction, step 2

![BBA](./images/bba-step-2.png)

---

#### But how about (major) refactorings?

##### Branching by abstraction, step 3

![BBA](./images/bba-step-3.png)

---

#### But how about (major) refactorings?

##### Branching by abstraction, step 4

![BBA](./images/bba-step-4.png)

---

#### But how about (major) refactorings?

##### Branching by abstraction, step 5

![BBA](./images/bba-step-5.png)

---

#### But how about unfinished changes?

![Toggles](./images/release-toggles-1.png)

---

#### But how about unfinished changes?

![Toggles](./images/toggles-4.png)

---

#### But I have an immature team

![Team](./images/immature_team.jpg)

#### [Commit Early and Often](https://www.youtube.com/watch?v=Rep7vsUTaVI)
<!-- .element: class="fragment"-->

---

#### But regulators demand (proof of) four-eyes!


![Four-eyes](./images/four-eyes.jpg)

