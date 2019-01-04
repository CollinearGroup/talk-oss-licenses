# OSS Licensing
> Everything you wanted to know about licensing but were too afraid to ask

---

### An Unfortunate Event

* Jun, 2015 - Prototype Kick-off
* Mar, 2018 - First Major User Signed Up
* Oct, 2018 - Production Software Audit

Note:

* As consultants at Collinear we help clients achieve their goals
* We choose NodeJs for an IoT project which was a new thing in 2015
* Client touted this as their next big service offering, signed customer in early 2018
* Late 2018 - Client ran an audit that exposed the fact that we were misusing OSS licenses
* Everything ground to a halt when we realized we couldn't release the product
* **This was the general feeling across the organization...**

+++

![](https://i.imgflip.com/2ohjvu.jpg)

Note:

* Betrayal of the ultimate degree.

+++

### Topics

<!-- TODO: update all titles -->
* **Why Open Source?**
* What You Need to Know
* Our Solution
* The Moral Obligations of Using OSS?

Note:

* We need to take a step back and have a good answer to the question from clients/mgmt
* We'd like to share our findings to hopefully save you some pain

+++

# Why is Open Source?

Note:

* I believe it is our responsibility as professionals to have an elementary understanding of the tools we use.
* How many have thought to themselves "Why is OSS?"

+++

### Free Software vs Open Source

> Free software gives the user "the freedom to run it, to study and change it, and to redistribute copies with or without changes."

- Richard Stallman, "Why Open Source misses the point of Free Software"


<!-- TODO: fix??? -->
Note:

* Open Source started as "Free Software"
* RMS: Founded the GNU project, an unix os
* A philosophy vs a purely practical development approach
* It's not just free software, it's strategic collaborative and create some common good that we can mutually benefit from. which is where licensing typically comes into play as a contract between each other on a piece of softwares intended use.
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

* **Developers being able to use "free code" without a second thought is beautiful, but is actually what got my team into trouble**

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

* Why is Open Source?
* **What You Need to Know**
* Our Solution
* The Moral Obligations of Using OSS?

+++

[`choosealicense.com`](https://choosealicense.com/)

Note:

* Here's a great link to go to if you don't want to remember anything I'm saying it will send you off in the right direction.

+++

### *copy-left*

![](https://dwheeler.com/essays/floss-license-slide-image.png)

+++

![](https://alistapart.com/d/considering-open-source-licenses/fig1.png)

+++

```md
# DON'T BE A DICK PUBLIC LICENSE

> Version 1.1, December 2016

> Copyright (C) [year] [fullname]

Everyone is permitted to copy and distribute verbatim or modified
copies of this license document.

> DON'T BE A DICK PUBLIC LICENSE
> TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

1. Do whatever you like with the original work, just don't be a dick.
```

Note:

* Your OSS Strategy has to deal with all these licenses.

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

* Why is Open Source?
* What You Need to Know
* **Our Solution**
* The Moral Obligations of Using OSS?

+++

### Our Solution

#### license-checker
> Demo

Note:

* Great little tool
* --summary
* --onlyunknown

+++ 

### Our Solution

TODO: Flow diagram of how CI/CD system can the tool and checked the licenses.

Note: 

* A great tool, but I think we can improve on it.
  * Doesn't show top level dep (remember: copy-left?)
  * Doesn't support npm custom license recommendation

+++ 

### license-validator
> Demo

[yea](https://github.com/CollinearGroup/license-validator)

Notes:

* Solves above issues and requires 0 setup, is even interactive!
* Again: this just helps you cover your butt when using OSS that your company isn't managing for you.

---

### Topics

* Why is Open Source?
* What You Need to Know
* Our Solution
* **The Moral Obligations of Using OSS?**

+++ 

### Free like a Puppy?

Note:

* event-source and the controversial mgmt ("I get nothing from this")
* instagram sold for 4 billion dollars almost 100% open source

+++ 

### The Business Models in Use Today

Notes: 

Open core, proprietary features (redis)
Support and Training (redhat)
Run the software as a service (Amazon/redis)
Mongo?
Is there a new one, Patreon?
Tidelift and the BitCoin attack.