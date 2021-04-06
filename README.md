Some Papers I Really Liked
==========================

This is a list of articles (and similar objects such as lecture notes) that have nothing
in common other than the fact that I read them and I really liked them.

Similarly, the notes I have written for each of them here are not intended to make much
sense to anyone other than me.

In order to really like a paper I have to have felt like I understood what the authors
were trying to say, so, many of these are tutorials or otherwise more on the accessible
side of things.

This document is written in [Feedmark](https://catseye.tc/node/Feedmark) format, with
entries ordered chronologically within each section.

*   [Programming Languages](#programming-languages)
*   [Type Systems](#type-systems)
*   [Reasoning about Programs](#reasoning-about-programs)
*   [Software Engineering](#software-engineering)
*   [Mathematics](#mathematics)
*   [Logic](#logic)
*   [Theorem Proving](#theorem-proving)

Programming Languages
---------------------

### Fundamental Concepts in Programming Languages

*   authors: Christopher Strachey
*   date: August 1967
*   wikipedia: https://en.wikipedia.org/wiki/Fundamental_Concepts_in_Programming_Languages
*   available @ [citeseerx](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.332.3161)

Strachey notes that mathematicians have problems seeing functions as first-class objects.
(In the term-rewriting language Aardappel, first-class functions were also evaluated to be
not so hot.)  This coincides, in an oblique way, with defunctionalization (see below).

### Definitional interpreters for higher-order programming languages

*   authors: John C. Reynolds
*   date: 1972
*   publication: ACM
*   available @ [citeseerx](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.110.5892)

This is the paper where the term "meta-circular" is introduced (while discussing the
wisdom of trying to define the meaning of a language using an interpreter written in
another language, or possibly even that same language) as well as the term "defunctionalization".
Reynolds notes a connection to state machines:

> Thus our third interpreter
> is actually a state-transition machine, whose states each consist of the name of a serious
> function plus a list of its arguments.

And this is a pithy statement:

> Although the basic concept of assignment is well understood by any competent programmer,
> a surprising degree of care is needed to combine this concept with the language features
> we have discussed previously.

This paper was republished in Higher-Order and Symbolic Computation, issue 11, in 1998
(pages 363–397).  There is another paper
"[Definitional interpreters revisited](http://homepages.inf.ed.ac.uk/wadler/papers/papers-we-love/reynolds-definitional-interpreters-revisited.pdf)"
where Reynolds recollects on this paper.

### The essence of compiling with continuations

*   authors: C. Flanagan, Amr Sabry, Bruce F. Duba, M. Felleisen
*   date: June 1993
*   publication: PLDI '93: Proceedings of the ACM SIGPLAN 1993 conference on Programming language design and implementation
*   available @ [rice](http://www.cs.rice.edu/~javaplt/311/Readings/essence-retro.pdf)

This is the paper that introduces "A-normal form".

This paper can sometimes be found attached to a newer paper which is a retrospective on the original paper.

### Trampolined style

*   authors: Steven E. Ganz, Daniel P. Friedman, Mitchell Wand
*   date: September 1999
*   publication: ICFP '99: Proceedings of the fourth ACM SIGPLAN international conference on Functional programming
*   available @ [citeseerx](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.44.8614)

This is my own slogan: Trampolines are just defunctionalized continuations.  The `cont`
function in Interpreter III in Reynolds' paper above is an example of a trampoline.

Type Systems
------------

### On Understanding Data Abstraction, Revisited

*   authors: William R. Cook
*   date: 2009
*   publication: OOPSLA '09: Proceedings of the 24th ACM SIGPLAN conference on Object oriented programming systems languages and applications
*   available @ [cs.utexas.edu](https://www.cs.utexas.edu/~wcook/Drafts/2009/essay.pdf)

Cogently shows that there is a difference between abstract data types and object-orientation,
and describes it.

### In Search of Types

*   authors: Stephen Kell
*   date: 2014
*   publication: Onward!
*   available @ [kent.ac.uk](https://www.cs.kent.ac.uk/people/staff/srk21/papers/kell14in-author-version.pdf)

When a type theorist says "type" they mean something from the typed lambda calculus.
When a software engineer says "type" they mean something they use to stop some bits
of their data from being confused with other bits of their data.  When the two groups
meet, hilarity ensues.

Reasoning about Programs
------------------------

### Can Programming Be Liberated from the von Neumann Style?

*   subtitle: A Functional Style and Its Algebra of Programs
*   authors: John Backus
*   date: August 1978
*   publication: Communications of the ACM
*   available @ [acm](https://dl.acm.org/doi/10.1145/359576.359579)

Contains the assertion that "von Neumann languages lack useful mathematical
properties".

Since this paper was written, there have been two schools of thought, based on
the reaction to this assertion.

One school agrees with the assertion and has persued what Wikipedia calls
"[function-level programming](https://en.wikipedia.org/wiki/Function-level_programming)"
which is sometimes also called "point-free programming"
or "calculation of programs", or more loosely "equational reasoning",
and of which _concatenative languages_ and _recursion schemes_ are followers to an extreme degree.

The other school agrees with the assertion but accepts the reality that
von Neumann languages are entrenched and, often, are the languages with
which the highest performance can be achieved, so has, in some sense,
shouted "damn the torpedoes" and has wrestled with turning von Neumann
programming from an art into a science *despite* its lack of useful
mathematical properties.  This school has given us "separation logic"
among other things.

### Algorithmics

*   subtitle: Towards programming as a mathematical activity
*   authors: Lambert Merteens
*   date: 1986
*   publication: CWI Monographs (North-Holland Publishing Co., Amsterdam)
*   available @ [citeseerx](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.694.5650)
*   available @ [cwi.nl](https://ir.cwi.nl/pub/2686/2686D.pdf)
*   available @ [kestrel.edu](https://www.kestrel.edu/people/meertens/publications/papers/Algorithmics.pdf)

Motivates a lot of the "calculational style" of developing programs.
Point-free functions, concatenative languages, recursion schemes are all related.

### Laws of Programming

*   authors: C. A. R. Hoare et al.
*   date: 1987
*   publication: Communications of the ACM, August 1987, Vol. 30 No. 8
*   available @ [ox.ac.uk](http://www.cs.ox.ac.uk/bill.roscoe/publications/20.pdf)

This applies the ideas of "calculational style" to imperative, rather than functional,
programs.  In the process it gives a mini-overview of denotational semantics.
Since specifications and programs are written in the same notation, this leads into
what is often called "program refinement".

### Algebraic Identities for Program Calculation

*   authors: Richard Bird
*   date: 1989
*   publication: The Computer Journal
*   available @ [academic.oup.com](https://academic.oup.com/comjnl/article-pdf/32/2/122/1445670/320122.pdf)

> To _calculate_ a program means to derive it from a suitable specification
> by a process of equational reasoning.

### A tutorial on the universality and expressiveness of fold

*   authors: Graham Hutton
*   date: July 1999
*   publication: Journal of Functional Programming
*   available @ [nott.ac.uk](https://www.cs.nott.ac.uk/~pszgmh/fold.pdf)

Hutton talks about the universal property of `fold`, showing that it
can be used in proofs to avoid the need for inductive proofs.  If I was
feeling bold, I might go one further and say: the universal property of
`fold` *is* induction!

Software Engineering
--------------------

### Statecharts

*   subtitle: A Visual Formalism for Complex Systems
*   authors: David Harel
*   date: July 1986
*   available @ [inf.ed.ac.uk](https://www.inf.ed.ac.uk/teaching/courses/seoc/2005_2006/resources/statecharts.pdf)

Even if you're not sold on the visual formalism Harel presents, it's
worth thinking about what it means to have a formal description of
the reactive behaviour of a system, and what it means to combine
such formal descriptions hierarchically and in parallel.

For motivating why one should care about the reactive behaviour of their
computer program in the first place, see Samek's paper below.

### Why software jewels are rare

*   authors: David Parnas
*   date: February 1996
*   publication: IEEE Computer Society
*   available @ [yodaiken](https://www.yodaiken.com/papers/Why_software_jewels_are_rare.pdf)

> 1. Design before implementing.
> 2. Document your design.
> 3. Review and analyze the documented design.
> 4. Review implementation for consistency with the design.

### Send-Receive Considered Harmful

*   subtitle: Myths and Realities of Message Passing
*   authors: Sergei Gorlatch
*   date: January 2004
*   publication: ACM Transactions on Programming Languages and Systems, Vol. 26, No. 1
*   available @ [citeseerx](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.192.7656&rep=rep1&type=pdf)

My own experience is that the actor model removes potentials for data races while
it introduces potentials for deadlocks.  You have to know what your communication
patterns *are*, at a higher level, before implementing them with message-passing.
That's the basic message of this paper too.

### Making Wrong Code Look Wrong

*   authors: Joel Spolsky
*   date: May 2005
*   publication: Joel on Software
*   available @ [joelonsoftware](https://www.joelonsoftware.com/2005/05/11/making-wrong-code-look-wrong/)

Mainly for the metaphor about the dirty oven.  The stuff about naming conventions,
like Hungarian notation, is valid, but is much better handled with flow typing
and type-and-effect systems.  You can out-and-out ignore the opinions about exceptions.

### State Machines for Event-Driven Systems

*   authors: Miro Samek
*   date: May 2016
*   publication: Barr Group Blog
*   available @ [barrgroup](https://barrgroup.com/embedded-systems/how-to/state-machines-event-driven-systems)

Samek makes a very persuasive case for using state machines to describe the
reactive behaviour of software.  Ad-hoc introduction of state variables
(especially boolean flags), as opposed to stepping back and thinking about
the thing as a finite state-transition system, is a common beginner mistake
that leads to "spaghetti state" and, quite often, bugs (where a state that
simply shouldn't exist, is entered, with undefined behaviour).

It seems that most of this article was originally published as "Who Moved my State?" in Dr Dobbs Journal in
2003.  There were several followup articles, including "[Back to Basics](https://web.archive.org/web/20090906195311/http://www.ddj.com/cpp/184401737?pgno=5)".
Nowadays these seem to only be available in archive.org's WayBack machine.

Mathematics
-----------

### The Lattice of Topologies: Structure and Complementation

*   authors: A. K. Steiner
*   year: 1966
*   publication: Transactions of the AMS
*   available @ [ams](https://www.ams.org/journals/tran/1966-122-02/S0002-9947-1966-0190893-2/S0002-9947-1966-0190893-2.pdf)

The set of all topologies on a set forms a lattice where the discrete
topology is the supremum and the trivial topology is the infimum.

I figured this must be the case before I found this paper.  I also
figured it must be an established result.  I enjoyed locating the
paper in which it was established.

### Infinity - A simple, but not too simple introduction

*   authors: Martin Meyries
*   year: 2015
*   publication: arXiv.org
*   available @ [arxiv](https://arxiv.org/abs/1506.06319)

Before you do any serious thinking about mathematics you should probably try to decide what
your feelings towards infinity are.

Logic
-----

### The Galois Connection between Syntax and Semantics

*   authors: Peter Smith
*   date: June 2010
*   publication: Logic Matters
*   available @ [logicmatters](https://www.logicmatters.net/2010/06/03/the-galois-connection-between-syntax-and-semantics/)

Smith goes into how there is a Galois connection between the syntax and semantics
of a logical system.  I think the idea could be applied to any formal language that has
been given a semantics.  (Is semantics a quotient of syntax?  Does taking a quotient
induce a Galois connection?  I wonder, I mean, I think so because it seems to just be
two different ways of talking about the same thing, or at least closely related things...)

### Syntax versus Semantics

*   authors: Reinhard Kahle, Wilfried Keller
*   date: July 2015
*   publication: arXiv.org
*   available @ [arxiv](https://arxiv.org/abs/1507.04678)

Distinguishing symbols pertaining to the syntax, from symbols pertaining to the
semantics, by colouring them differently.

Theorem Proving
---------------

### How to believe a machine-checked proof

*   authors: Robert Pollack
*   date: July 1997
*   publication: BRICS
*   available @ [citeseerx](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.50.1529)

Addresses some basic philosophical issues regarding machine-checked proofs.

### The LCF Approach to Theorem Proving

*   authors: John Harrison
*   year: September 2001
*   publication: slides from a talk given at the University of Manchester
*   available @ [cam.ac.uk](https://www.cl.cam.ac.uk/~jrh13/slides/manchester-12sep01/slides.pdf)

The LCF approach is to have an abstract data type representing valid proofs,
exposing only those operations which represent valid proof steps, so that
the result of each of those operations is also necessarily a valid proof.

### Automated Reasoning for the Working Mathematician

*   authors: Jeremy Avigad
*   year: 2019
*   publication: slides from a talk given in London
*   available @ [cmu](http://www.contrib.andrew.cmu.edu/~avigad/Talks/london)

Lots of discussion on _how much_ automation can or should be used, and when,
when formalizing mathematics.

### The Future of Mathematics?

*   authors: Kevin Buzzard
*   year: January 2020
*   publication: slides from a talk given at Pittsburgh
*   available @ [ams](http://www.andrew.cmu.edu/user/avigad/meetings/fomm2020/slides/fomm_buzzard.pdf)

> If my work in pure mathematics is neither useful nor
> _100 percent guaranteed_ to be correct, it is surely a waste of time.
