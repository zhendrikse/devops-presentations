## The four-eyes principle

![Four eyes principle](./images/four-eyes.jpg)

Zeger Hendrikse

---

#### Warming up: first question

### What does CI mean?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> Continuous Improvement<br />
<b>B:</b> Continuous Integration<br />
<b>C:</b> Continuous Inspection<br />
<b>D:</b> Continuous Insights<br />
</p>

<p><!-- .element class="fragment" -->
<font style="color:#FF0000; font-weight: bold">A:</font> Continuous Improvement<br />
<font style="color:#00FF00; font-weight: bold">B:</font> Continuous Integration<br />
<font style="color:#FF0000; font-weight: bold">C:</font> Continuous Inspection<br />
<font style="color:#FF0000; font-weight: bold">D:</font> Continuous Insights<br />
</p>

</div>

---

### The Death 

![death](./images/hiclipart.com.png)

### of Continuous Integration
---

### Agenda

- <!-- .element: class="fragment"-->
  **The three ways of DevOps** (5 mins)

- <!-- .element: class="fragment"-->
  **Summary/overview CICD** (5 mins)

- <!-- .element: class="fragment"-->
  **Summary/overview TBD** (10 mins)

- <!-- .element: class="fragment"-->
  **Summary/overview Segration of Duties** (10 mins)

- <!-- .element: class="fragment"-->
  **Implementing SoD the right way** (5 mins)

- <!-- .element: class="fragment"-->
  **Code reviews?** (5 mins)

- <!-- .element: class="fragment"-->
  **Questions and answers!** (All that is left)

---

### Context: three ways of DevOps

1. <!-- .element: class="fragment"-->
   ![Git](./images/DevOps1.png)

2. <!-- .element: class="fragment"-->
   ![Git](./images/DevOps2.png)

3. <!-- .element: class="fragment"-->
   ![Git](./images/DevOps3.png)

---

#### Warming up: second question

### What does CD mean?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> Continuous Delivery<br />
<b>B:</b> Continuous Development<br />
<b>C:</b> Continuous Deployment<br />
<b>D:</b> Continuous Design<br />
</p>

<p><!-- .element class="fragment" -->
<font style="color:#00FF00; font-weight: bold">A:</font> Continuous Delivery<br />
<font style="color:#FF0000; font-weight: bold">B:</font> Continuous Development<br />
<font style="color:#00FF00; font-weight: bold">C:</font> Continuous Deployment<br />
<font style="color:#FF0000; font-weight: bold">D:</font> Continuous Design<br />
</p>

</div>

---

### CICD Overview

<div class="r-stack">
  <img class="fragment" src="./images/cicd-overview-1.png" />
  <img class="fragment" src="./images/cicd-overview-2.png" />
  <img class="fragment" src="./images/cicd-overview-3.png" />
  <img class="fragment" src="./images/cicd-overview-4.png" />
  <img class="fragment" src="./images/cicd-overview-5.png" />
</div>

---

#### CI check: why version control

### What is the primary purpose of a VCS/Git?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> To facilitate roll backs and roll forwards<br />
<b>B:</b> To facilitate seamless branching and merging<br />
<b>C:</b> To facilitate communication and collaboration<br />
<b>D:</b> To facilitate a central back-up of source code<br />
</p>

<p><!-- .element class="fragment" -->
<font style="color:#FF0000; font-weight: bold">A:</font> To facilitate roll backs and roll forwards<br />
<font style="color:#FF0000; font-weight: bold">B:</font> To facilitate seamless branching and merging<br />
<font style="color:#00FF00; font-weight: bold">C:</font> To facilitate communication and collaboration<br />
<font style="color:#FF0000; font-weight: bold">D:</font> To facilitate a central back-up of source code<br />
</p>

</div>

---

### Do you practice Continuous Integration?

<div class="r-stack">
  <a class="fragment" href="https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html"><img alt="Continuous Integration" src="./images/what_is_ci_1.png"/></a>
  <a class="fragment" href="https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html"><img alt="Continuous Integration" src="./images/what_is_ci_2.png"/></a>
  <a class="fragment" href="https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html"><img alt="Continuous Integration" src="./images/what_is_ci_3.png"/></a>
</div>

---

#### CI final check

### What does Continuous Integration mean in practice?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> Building your application and running your unit tests on a server<br />
<b>B:</b> Creating releasable artifacts using a CI pipeline<br />
<b>C:</b> Automating all aspects that are required to build your software<br />
<b>D:</b> Running checks locally, direct commits on trunk and subsequent automated builds<br />
</p>

<p><!-- .element class="fragment" -->
<font style="color:#FF0000; font-weight: bold">A:</font> Building your application and running your unit tests on a server<br />
<font style="color:#FF0000; font-weight: bold">B:</font> Creating releasable artifacts using a CI pipeline<br />
<font style="color:#FF0000; font-weight: bold">C:</font> Automating all aspects that are required to build your software<br />
<font style="color:#00FF00; font-weight: bold">D:</font> Running checks locally, direct commits on trunk and subsequent automated builds<br />
</p>

</div>

---

### Which branching strategy should I choose?

![Choose](./images/pngwing.com.png)

---

### So right off the bat ...

[![Git](./images/dontBranch.jpg)](https://www.davefarley.net/?p=247)

---

### The Big Controversy

![Dave](./images/davefarley.jpg)

> [...] I get “Heretic, burn him at the stake” kind of feedback [...] &mdash; [Dave Farley](https://www.davefarley.net/?p=247)

---

### The death of _continuous_ integration...

![branches](./images/branches_intro.png)

---

#### Third question: amplify feedback loops

### Which is the odd one out?

<div class="r-stack" align="left">

<p><!-- .element class="fragment" -->
<b>A:</b> Integrate early and often<br />
<b>B:</b> Small batch size (containing changes)<br />
<b>C:</b> Pair programming<br />
<b>D:</b> Pull requests<br />
</p>

<p><!-- .element class="fragment" -->
<font style="color:#00FF00; font-weight: bold">A:</font> Integrate early and often<br />
<font style="color:#00FF00; font-weight: bold">B:</font> Small batch size (containing changes)<br />
<font style="color:#00FF00; font-weight: bold">C:</font> Pair programming<br />
<font style="color:#FF0000; font-weight: bold">D:</font> Pull requests<br />
</p>

</div>

---

### Negative effects of branches

- <!-- .element: class="fragment"-->
  Delays integration 
  - <!-- .element: class="fragment"-->
    Slower feedback loops
  - <!-- .element: class="fragment"-->
    Kills continuous integration

- <!-- .element: class="fragment"-->
  Increased change batch size
  - <!-- .element: class="fragment"-->
    Slower feedback loops
  - <!-- .element: class="fragment"-->
    Decreased deployment frequency

- <!-- .element: class="fragment"-->
  Kills communication 
  - <!-- .element: class="fragment"-->
    Headphone/hero developers!

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

## The four-eyes principle

![Four eyes principle](./images/four-eyes.jpg)

---

### Four-eyes is **NOT** equivalent to pull requests


#### Ok Zeger, I want to know more, tell me more! 
<!-- .element: class="fragment"-->

---

### The FEP is a risk control technique

![Pilots](./images/airline-pilot-language.jpg)

---

### FEP: Segregation of Duties (SoD)

![WC eend](./images/wc-eend.png)

---

### FEP: Segregation of Duties (SoD)

- <!-- .element: class="fragment"-->
  Finance: mortgage requestor approves his own mortgage request 

- <!-- .element: class="fragment"-->
  IT: developer writes and tests his own code

- <!-- .element: class="fragment"-->
  [Etc.](https://simplicable.com/new/four-eyes-principle)

---

### SoD at financial institutions

![Pipeline](./images/ci-cd-pipelines.png)

No one should be able to push his code and tests single-handedly to PRD
---

![Person](./images/pngwing.com.png)

---

### What usually goes wrong

- <!-- .element: class="fragment"-->
  And thus... what would the Pavlov reaction be?
  ![Pavlov](./images/pavlov-de-stopper.gif)

- <!-- .element: class="fragment"-->
  The answer to life, the universe and everything:
  ![Git](./images/Git-Icon.png)

---

### But really...

_Somewhere_ an independent (automated!) approval should happen:

![Pipeline](./images/ci-cd-pipelines.png)

What did ABN-AMRO choose?

---

### Automated registration of changes in Snow

- Minor and path versions are _pre_ approved
- Major versions require manual approvals (still)

---

### But I need my code reviews!

![Code review](./images/code_review.jpg)
... but do you **really** do?

---

### But I need proof too!

- Eventually it boils down to trust
  - PRs are often superficially reviewed
  - TBD should involve all team members

- We may need to educate the auditors
  - No more (additional) manual steps
  - Convince of a modern way to assert SoD

---

#### Let's think
### Let's be critical
## Let's be inventive!

---
### References
- [Four-eyes principle](https://confluence.aws.abnamro.org/pages/viewpage.action?spaceKey=GRIDAD&amp;title=Four-eyes+principle)
- [Trunk Based Development](https://confluence.aws.abnamro.org/display/GRIDAD/Trunk+Based+Development)
---

# Questions

![Person](./images/pngwing.com.png)
