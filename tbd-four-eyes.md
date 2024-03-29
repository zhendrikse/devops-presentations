## The four-eyes principle

![Four eyes principle](./images/four-eyes.jpg)

Zeger Hendrikse

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

### The Death 

![death](./images/hiclipart.com.png)

### of Continuous Integration
---

### Agenda

- **The three ways of DevOps** (5 mins)
<!-- .element: class="fragment"-->

- **Summary/overview CICD** (5 mins)
<!-- .element: class="fragment"-->

- **Summary/overview TBD** (10 mins)
<!-- .element: class="fragment"-->

- **Summary/overview Segration of Duties** (10 mins)
<!-- .element: class="fragment"-->

- **Implementing SoD the right way** (5 mins)
<!-- .element: class="fragment"-->

- **Code reviews?** (5 mins)
<!-- .element: class="fragment"-->

- **Questions and answers!** (All that is left)
<!-- .element: class="fragment"-->

---

### Context: three ways of DevOps

1. ![Git](./images/DevOps1.png)
<!-- .element: class="fragment"-->

2. ![Git](./images/DevOps2.png)
<!-- .element: class="fragment"-->

3. ![Git](./images/DevOps3.png)
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

### CICD Overview

![CICD overview](./images/cicd-overview-1.png)

---

### CICD Overview

![CICD overview](./images/cicd-overview-2.png)

---

### CICD Overview

![CICD overview](./images/cicd-overview-3.png)

---

### CICD Overview

![CICD overview](./images/cicd-overview-4.png)

---

### CICD Overview

![CICD overview](./images/cicd-overview-5.png)

---

#### CI check: why version control

### What is the primary purpose of a VCS/Git?

* **A**: To facilitate roll backs and roll forwards
* **B**: To facilitate seamless branching and merging
* **C**: To facilitate communication and collaboration
* **D**: To facilitate a central back-up of source code

---

#### CI check: why version control

### What is the primary purpose of a VCS/Git?

* **A**: To facilitate roll backs and roll forwards
* **B**: To facilitate seamless branching and merging
* **==&gt;C**: To facilitate communication and collaboration **&lt;==**
* **D**: To facilitate a central back-up of source code

---

### Do you practice Continuous Integration?

[![Continuous Integration](./images/what_is_ci_1.png)](https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html)

---

### Do you practice Continuous Integration?

[![Continuous Integration](./images/what_is_ci_2.png)](https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html)

---

### Do you practice Continuous Integration?

[![Continuous Integration](./images/what_is_ci_3.png)](https://thinkinglabs.io/2020/03/23/continuous-integration-is-not-a-tooling-problem.html)

---

#### CI final check

### What does Continuous Integration mean in practice?

* **A**: Building your application and running your unit tests on a server
* **B**: Creating releasable artifacts using a CI pipeline
* **C**: Automating all aspects that are required to build your software
* **D**: Running checks locally, direct commits on trunk and subsequent automated builds

---

#### CI final check

### What does Continuous Integration mean in practice?

* **A**: Building your application and running your unit tests on a server
* **B**: Creating releasable artifacts using a CI pipeline
* **C**: Automating all aspects that are required to build your software
* **==&gt;D**: Running checks locally, direct commits on trunk and subsequent automated builds **&lt;==**

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

* **A** Integrate early and often
* **B** Small batch size (containing changes)
* **C** Pair programming
* **D** Pull requests

---

#### Third question: amplify feedback loops

### Which is the odd one out?

* **A** Integrate early and often
* **B** Small batch size (containing changes)
* **C** Pair programming
* **==&gt;D** Pull requests **&lt;==**

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

- Finance: mortgage requestor approves his own mortgage request 
<!-- .element: class="fragment"-->

- IT: developer writes and tests his own code
<!-- .element: class="fragment"-->

- [Etc.](https://simplicable.com/new/four-eyes-principle)
<!-- .element: class="fragment"-->

---

### SoD at financial institutions

![Pipeline](./images/ci-cd-pipelines.png)

No one should be able to push his code and tests single-handedly to PRD
---

![Person](./images/pngwing.com.png)

---

### What usually goes wrong

- And thus... what would the Pavlov reaction be?
  ![Pavlov](./images/pavlov-de-stopper.gif)

- The answer to life, the universe and everything:
  ![Git](./images/Git-Icon.png)
<!-- .element: class="fragment"-->

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
