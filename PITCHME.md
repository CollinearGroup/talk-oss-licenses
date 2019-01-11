# OSS Licensing
> Everything you wanted to know about licensing but were too afraid to ask

Note:

* My name is... I have some friends here...
* We work for Collinear Group and do software consulting mainly for enterprises. Mainly the aviation industry.
* **As a consultant for an enterprise company, hopefully you'll find some value in us sharing some recent licensing experiences.**

---

### An Unfortunate Event

* Jun, 2015 - Prototype Kick-off
* Mar, 2018 - First Major User Signed Up
* Oct, 2018 - Production Software Audit

Note:

* Jun 2015: We choose NodeJs for an IoT project which was a new thing in 
* Mar 2018: Client touted this as their next big service offering
* Late 2018: Client ran an audit that exposed the fact that we were misusing OSS licenses
* Everything ground to a halt when we realized we couldn't release the product
* **This was the general feeling across the organization...**

+++

![](https://i.imgflip.com/2ohjvu.jpg)

Note:

* Betrayal of the ultimate degree.

---

### Topics

* **Why Open Source?**
* What You Need to Know
* Our Solution

Note:

* We need to take a step back and have a good answer to the question from clients/mgmt

+++

# Why Open Source?

Note:

* How many of you have thought about why you use OSS?

+++

### Free Software vs Open Source

> Free software gives the user "the freedom to run it, to study and change it, and to redistribute copies with or without changes."

Richard Stallman, "Why Open Source misses the point of Free Software"

Note:

* Open Source started as "Free Software"
* Richard M.S. - Founded the GNU project, an unix os
* A philosophy vs a purely practical development approach
* Licensing is the contract that protects both of these different ideas
* **Since we are dealing with Open Source it is useful to note why others use it**

+++ 

### Why Open Source?

According to...

* Google: Customers want options
* Dgraph: Adoption of new tech
* MediaWiki: Genuine humanitarians
* Collinear Group: To give back and showcase our work
* Developers: ¡free code!

Note:

* Developers want "free code"
  * "I get nothing from this" - people were mad about this statement when their "free code" ended up looking like it would hurt them.
  * Google rep at Conference noted "free like a puppy" implying responsibility even as a user
  * We are not actually using "free code" we are using "open sourced" code.
* **Developers being able to use OSS without a second thought is beautiful, but is actually what got my team into trouble**

+++

### Open Source Adoption Stages

1. *Individual Devs*
1. *Project*
1. Organization
1. Company

Note:

* You should be able to find yourself on this list, and if you are in the first two categories then you need to really understand the constraints of using OSS.
* In step 3 and 4, the lawyers and leaders have typically done the hard part for you. Cite: American Express, approving every module.

---

### Topics

* Why Open Source?
* **What You Need to Know**
* Our Solution

+++

[`choosealicense.com`](https://choosealicense.com/)

Note:

* Here's a great link to go to if you don't want to remember anything I'm saying it will send you off in the right direction.

+++

### *copy-left*

![](https://dwheeler.com/essays/floss-license-slide-image.png)

Note:

* The stronger restrictions apply to the left.
* **This simple graph almost makes the problem look manageable**

+++

![](https://alistapart.com/d/considering-open-source-licenses/fig1.png)

* The real world is full of crazy licenses **for instance...**

+++

```md
# DON'T BE A DICK PUBLIC LICENSE

> Version 1.1, December 2016

> Copyright (C) [year] [fullname]

Everyone is permitted to copy and distribute verbatim or modified
copies of this license document.

> DON'T BE A DICK PUBLIC LICENSE
> TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

1. Do whatever you like with the original work,
   just don't be a dick.
```

Note:

* Your OSS Strategy has to deal with all these licenses.
* **Obviously you want to use a safe license for your projects, probably not the DBDPL so what should you use?**

+++

### Recommendation for your next OSS contribution

* Apache 2.0
* If not, (like ISC) consider a Contributor License Agreement
* If you like controversy: [Commons Clause](https://commonsclause.com/)

Note:

* How many people spent more than 2 seconds during an `npm init` to think "what is an ISC license"?
* CLA - Ensures that the repo maintainer gets the rights over contributions.
* Commons Clause - prohibits turning around and selling software like AWS did with Redis.
* Google banned the GPL and CC'd licenses.
* MongoDB was AGPL but just became even more restrictive (any service that uses the service should be open sourced?).

---

### Topics

* Why Open Source?
* What You Need to Know
* **Our Solution**


+++

### A First Attempt

![](/assets/img/license-checker-summary.png)

Note:

* `licenses-checker` available to install and run
* **One of the licenses here was a WTFPL**

+++

![](/assets/img/wtfpl-expand-template.png)

Note:

+++

![](/assets/img/expand-temp-dep.png)

Note:

* Since it's grunt, a dev dep, we don't actually need to worry about it.

+++

![](/assets/img/gitlab-ci.png)

Note:

* To start putting this together we ran license checker like so

+++

![](/assets/img/check-licenses_js.png)

Note:

* A custom script managed which licenses AND modules to validate, returning code 0 or 1 
* **While this works, it's a bit of manual setup and discovery and we wanted to make it easier for ourselves**

+++ 

### Our Solution

![](/assets/img/license-validator.png)

Note:

* Demo
* Open `oasgraph` and run validator
* Solves above issues and requires 0 setup
* Again: this just helps you cover your butt when using OSS that your company isn't managing for you.
* Limitations: NOn-SPDX licenses and NPM recommendation

---

# Questions?

---

# Thank You!
