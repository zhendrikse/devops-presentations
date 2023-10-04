---
title: Continuous Integration and Trunk-Based Development
author: Zeger Hendrikse
date: 2023-10-04
theme: dracula
highlightTheme: github-dark
---

<section data-background-image="./images/edward-howell-yl6xgqD3X14-unsplash.jpg">

## Trunk Based Development

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

</section>

---

### But first ...

[..] Who the f... are you?

![Zeger](./images/zeger_profile.png)

I am Zeger Hendrikse, nice to meet you too 😉

---

#### Warming up: first question

### What does CI mean?

* **A**: Continuous Improvement
* **B**: Continuous Integration
* **C**: Continuous Inspection
* **D**: Continuous Insights

---

#### Warming up: first question

### What does CI mean?

* **A**: Continuous Improvement
* **==&gt;B**: _Continuous Integration_ **&lt;==**
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

#### Warming up: second question

### What does CD mean?

* **A**: Continuous Delivery
* **B**: Continuous Development
* **C**: Continuous Deployment
* **D**: Continuous Design

---

#### Warming up: second question

### What does CD mean?

* **==&gt;A**: _Continuous Delivery_ **&lt;==**
* **B**: Continuous Development
* **==&gt;C**: _Continuous Deployment_ **&lt;==**
* **D**: Continuous Design

---

## CI in the context of CD

<div class="r-stack">
  <img class="fragment" src="./images/cicd-overview-1.png" />
  <img class="fragment" src="./images/cicd-overview-2.png" />
  <img class="fragment" src="./images/cicd-overview-3.png" />
  <img class="fragment" src="./images/cicd-overview-4.png" />
  <img class="fragment" src="./images/cicd-overview-5.png" />
</div>

---

#### First question: CI practice

##### Which of the following is **not** a CI best practice?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> Deploy the code to a test environment<br />
<b>B:</b> Keep the build fast<br />
<b>C:</b> Everyone commits to the baseline everyday<br />
<b>D:</b> When the build fails, everybody stops and helps to fix the build<br />
</p>

<p><!-- .element class="fragment" -->
<font style="color:#FF0000; font-weight: bold">A:</font> Deploy the code to a test environment<br />
<font style="color:#00FF00; font-weight: bold">B:</font> Keep the build fast<br />
<font style="color:#00FF00; font-weight: bold">C:</font> Everyone commits to the baseline everyday<br />
<font style="color:#00FF00; font-weight: bold">D:</font> When the build fails, everybody stops and helps to fix the build<br />
</p>

</div>

---

#### Second question: version control

##### What is the primary purpose of a VCS?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> To facilitate roll backs and roll forwards<br/>
<b>B:</b> To facilitate seamless branching and merging<br/>
<b>C:</b> To facilitate communication and collaboration<br/>
<b>D:</b> To facilitate a central back-up of source code<br/>
</p>

<p><!-- .element class="fragment" -->
<font style="color:#FF0000; font-weight: bold">A:</font> To facilitate roll backs and roll forwards<br/>
<font style="color:#FF0000; font-weight: bold">B:</font> To facilitate seamless branching and merging<br/>
<font style="color:#00FF00; font-weight: bold">C:</font> To facilitate communication and collaboration<br/>
<font style="color:#FF0000; font-weight: bold">D:</font> To facilitate a central back-up of source code<br/>
</p>

</div>

---

#### Do you practice Continuous Integration?

<div class="r-stack">
  <a href="https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html"><img class="fragment" src="./images/what_is_ci_1.png" /></a>
  <a href="https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html"><img class="fragment" src="./images/what_is_ci_2.png" /></a>
  <a href="https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html"><img class="fragment" src="./images/what_is_ci_3.png" /></a>
</div>

---

#### Third question: amplify feedback loops

##### Which is the odd one out?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> Integrate early and often<br/>
<b>B:</b> Small batch size (containing changes)<br/>
<b>C:</b> Pair-programming<br/>
<b>D:</b> Pull requests<br/>
</p>

<p><!-- .element class="fragment" -->
<font style="color:#00FF00; font-weight: bold">A:</font> Integrate early and often<br/>
<font style="color:#00FF00; font-weight: bold">B:</font> Small batch size (containing changes)<br/>
<font style="color:#00FF00; font-weight: bold">C:</font> Pair-programming<br/>
<font style="color:#FF0000; font-weight: bold">D:</font> Pull requests<br/>
</p>

</div>

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

- Delays integration 
<!-- .element: class="fragment"-->
  - Slower feedback loops
  <!-- .element: class="fragment"-->
    - Kills continuous integration
    <!-- .element: class="fragment"-->

- Increased change batch size
<!-- .element: class="fragment"-->
  - Slower feedback loops
  <!-- .element: class="fragment"-->
    - Decreased deployment frequency
    <!-- .element: class="fragment"-->

- Kills communication 
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

### Rules for TBD
- **Small commits** (approx 10 - 15 lines)
- Commits (_self contained_ and _consistent_) include production and test code
- Always commit and push together
- **No** branches (except for spikes)
- Code commits are reviewed ([early and synchronously](http://allankelly.blogspot.co.uk/2015/03/code-and-other-reviews-small-piece-of.html))

---

### TBD in action

![branches](./images/tbd_in_action.png)

---

### More objections! The usual suspects...

![Dave](./images/davefarley.jpg)

> _At one extreme I get “Heretic, burn him at the stake” kind of feedback, at_
  _the other “Yes, but it can’t possibly work without Feature Branching – you must_
    _work in small teams and/or on trivially simple projects”._ &mdash; [Dave Farley](https://www.davefarley.net/?p=247)

---

### I am (frequently) pulling from the mainline!

---

### TDB: small and frequent commits

### Low-frequency integration

![Merging](./images/merge_1.png)

Suppose S1 and V1 contain a merge conflict...

---

### TDB: small and frequent commits

### Low-frequency integration

![Merging](./images/merge_2.png)

... merge conflicts are late and big!

---

### TDB: small and frequent commits

### High-frequency integration

![Merging](./images/merge_3.png)

Suppose S1 and V1 contain a merge conflict...

---

### TBD: small and frequent commits

### High-frequency integration

![Merging](./images/merge_4.png)

... merge conflicts are small and early!

---

### But how about (major) refactorings?

### Branching by abstraction, step 1

![BBA](./images/bba-step-1.png)

---

### But how about (major) refactorings?

### Branching by abstraction, step 2

![BBA](./images/bba-step-2.png)

---

### But how about (major) refactorings?

### Branching by abstraction, step 3

![BBA](./images/bba-step-3.png)

---

### But how about (major) refactorings?

### Branching by abstraction, step 4

![BBA](./images/bba-step-4.png)

---

### But how about (major) refactorings?

### Branching by abstraction, step 5

![BBA](./images/bba-step-5.png)

---

### But how about unfinished changes?

![Toggles](./images/release-toggles-1.png)

---

### But how about unfinished changes?

![Toggles](./images/toggles-4.png)

---

### But I have an immature team

![Team](./images/immature_team.jpg)

## [Commit Early and Often](https://www.youtube.com/watch?v=Rep7vsUTaVI)

---

### But regulators demand (proof of) four-eyes!


[![Four-eyes](./images/four-eyes.jpg)](https://confluence.aws.abnamro.org/pages/viewpage.action?spaceKey=GRIDAD&title=Four-eyes+principle)

See also [the TBD section](https://confluence.aws.abnamro.org/display/GRIDAD/Four-eyes+principle)
on the [software development pages](https://confluence.aws.abnamro.org/display/GRIDAD/Software+Development) 
