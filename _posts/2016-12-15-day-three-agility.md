---
layout: post
title: "Day Three: Agility"
---

Hello again. Today I'm doing some programming for Lyon. The website is blocked by DNS changes that are still propagating. Once the switchover is complete I'll be able to show practitioners what it looks like and get feedback quickly and easily.

Speaking of which - I've been reading about agile development. Essentially - a methodology in which the project is **agile** and *responsive to change* rather than comprehensively planned from the beginning. The theory is that project requirements **always** change so the concept and design plans become almost immediately stale. The importance of *working software* is also emphasized, particularly over extensive documentation that can become quickly outdated in the face of rapid change. Automatic documentation tools like Doxygen and Sphinx's autodoc rule here. *Continuous delivery* also fits into this - it's better to deploy a new version once a week with few features than once a month with many. Quick and often deliveries of software allow rapid iteration and problem solving - especially when face to face time can be arranged with end-users.

The relevance of this to my Lyon project is clear - I've recently been debating internally how expansive the first version of the software should be and how much 'future-proofing' I should do on the database models. As a solo developer - I don't have the necessary skills or experience to completely plan and design the software before I start coding. If I used some of the Agile software development principles I would immediately know that I should start small and be prepared to change my schema often as the requirements change or features are developed.

With that in mind, I've decided on a modest, bare-bones feature set for the first iteration of my API. The endpoints will be:

* Client
* Event
* Practitioner
* Invoice
* InvoiceItem
* Payment

This will almost certainly change as I develop it - and that's OK!
