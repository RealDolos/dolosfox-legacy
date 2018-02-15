Dolosfox Nightly
====

A firefox "fork" that can still into (some) legacy add-ons.
Mostly by putting back some stuff mozilla removed. But not that much stuff actually.

Instructions
---

* `hg clone https://hg.mozilla.org/mozilla-central`

* `git clone` this repo.

* `cd mozilla-central`

* `./mach bootstrap`

* Apply the patchset (`hg import` or `patch`, with some fuzzing probably, maybe a merge or two)

* `ln -s $PWD/../dolosfox/branding browser/branding/dolosfox`

* Create an appropriate `.mozconfig`, I suggest you do the following (with platform being your platform)

  ```echo source $PWD/../dolosfox/.mozconfig.platform > .mozconfig```

* `./mach build && ./mach package` (package gives you a zip with binaries)

* To create a windows setup.exe `./mach build installer`

* To test, you may want `./mach run`


If in doubt, consult the [build instructions on MDN](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions).


Updating
---

Enable the hg rebase extension if you haven't already and `hg pull --rebase`
Resolve conflicts as needed.

Dolosfox builds should disable the mozilla updater.

FAQ
---

* _Who is that old guy in your logo?_

  It's an in-joke. If you're no "in", you haven't missed much, also you probably don't want to know anyway.

* _What does "Dolos" even mean?_

  That's my name, ignorant person of personage, you! Also, it's greek (google it) and also ud defines it as "Doing shit by yourself" which seems fitting, too.

* _Will you support add-on ***xyz***, it's still broken?!_

  Probably not.

* _Will you merge my pull request?_

  Maybe, but probably not, tbqh, unless it's really good and really solves something.

* _Will you fix the bugs I report?_

  Most likely not, unless the cause is my patchset.

* _Can I get support from you?_

  If you're willing to pay a lot, maybe. Otherwise, no!

* _Can I get support from mozilla?_

  mozilla decided to abandon proper extensions for political reasons, not technical ones (as this patchset shows). So let me answer with a counter-question: What do you think?!

* _Where are the binaries?_

  I don't provide binaries. If anybody else wants to provide their binaries to the public, fine, but don't consider them endorsed by me.

* _Is Dolosfox endorsed/supported/ok with mozilla?_

  Firefox is open source, so "ok with" should be yes (unless I abuse their trademarks, which I do not). "Endorsed" and "supported" are a firm "hell no!".

* _Do I have to use your branding?_

  Yes (i.e. "of course not!")

* _How long will this "fork" be alive?_

  For the forseeable future probably, because WebExtensions (aka "let's copy the useless stuff from google, but with many new bugs") suck for most things (if things are even possible with them).