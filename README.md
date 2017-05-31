# Functional Programming projects

### Abstract

> If you could work on open-source, functional programming software projects, with a view to your work helping others (e.g. industry programmers), what type of projects would you like to work on?

### General areas of interest

* blockchain
* distributed programming
* government registries
* logic systems
* e-health
* software developer tools
* geospatial
* secure systems

----

### Scala Library Standardisation

Several of the existing libraries for the Scala programming language have incompatibilities between versions. This means that users cannot use all these libraries in a single project. This has incurred a lot of time for developers at Australian companies, such as [realestate.com.au](https://www.realestate.com.au), [ephox](https://www.ephox.com/) and [skedulo](http://skedulo.com/).

Forking projects such as `[http4s, doobie, argonaut, scalaz, scalacheck, specs2, scalaz-specs2]`, then modifying the code so that there exist versions that are compatible between other would alleviate a lot of this problem. The current solution is for each individual encounter with this problem to do this, but only to the extent necessary to move on with the primary software objective.

----

### Scalaz 8 and scalaz-stream

Scalaz version 8 has been discussed in meetings. Scalaz is used heavily by Atlassian, along with the related scalaz-stream library, which has many bugs. Scalaz version 8 is proposed as an incompatible version of the scalaz library, with a view to implementing what has been learned about the Scala programming language over time.

The Scalaz library is used in almost every Scala software project as a third-party addition [if it isn't used, it is replicated].

Contributors from around the world have expressed a keenness to move on to the next iteration of the Scalaz library, along with fixing all the bugs that are in scalaz-stream.

----

### PureScript core programming language and front-end libraries

[PureScript](http://www.purescript.org/) is a programming language that is used for web programming. It replaces JavaScript by providing stronger guarantees of program correctness, improved library support and better tooling. PureScript is under active development by contributors from around the world.

There is a lot of work to be done on the core language itself, as well as providing higher-level libraries to application developers.

----

### Glasgow Haskell Compiler (GHC)

GHC is an ongoing project for the Haskell programming language, one of the most practical programming language tools in the world. GHC is on the leading edge of research, requiring significant work in implementing that research.

In particular, there has been [recent discussion](https://www.reddit.com/r/haskell/comments/5g8nd0/golangs_realtime_gc_in_theory_and_practice_from/) of how GHC would benefit from having several different user-selectable garbage collectors.

----

### GHCJS

GHCJS (Haskell for Javascript) aims to solve a similar problem to PureScript [that JavaScript should never be handwritten], however, takes a very different approach. GHCJS compiles Haskell source to the JavaScript language, with a view to exploit all the practical properties of Haskell, but aiming at the legacy of JavaScript that is implemented in web browsers today.

----

### Interactive proof writing tools (Agda)

Agda is a dependently-typed proof assistant. Like Haskell, it sits on the leading edge of research and there is a lot of work to be done in implementing that research.

----

### Better program extraction for proof assistants (Coq)

Coq is also a dependently-typed proof assistant. 
It has mature support for describing programs, proving properties about them, and then extracting these programs into other languages.
At the moment there is extraction support for ML, Haskell and Scheme, although the ML support is the most mature.

Improving the extraction support for Haskell and/or adding support for extraction to other languages would both be useful.

----

### Numerical Computing tools for Haskell

Data scientists, today, generally write numerical computing algorithms with the Python programming language. There is an existing and significant effort to achieve similar goals, but with the benefits provided by Haskell. Specifically, program correctness and program composition are desirable goals of numerical computing, and a common complaint is the inability to achieve these with Python.

----

### Implement propagators for concurrent programming (see talks by Edward Kmett)

The properties of joined semi-lattices can be exploited for concurrent programming. The benefits of propagators for concurrent programming have been recently discussed after [talks by Edward Kmett](https://www.youtube.com/watch?v=DyPzPeOPgUE). Further work here would create the ultimate framework for concurrent programming.

https://github.com/ekmett/propagators

----

### Automated Specification-based programming tools e.g. QuickCheck

QuickCheck has become the _de facto_ library for automated testing. However, it has some implementation problems.

* Inability to reproduce steps that lead to a falsified test.
* Underlying random-generation model that cheats the type system, leading to poor composition.
* Inability to provide tool support after the fact, due to poor library design.

It has been discussed regularly among other programmers how this could be significantly improved and with benefit for all.

----

### Implement a Haskell library for Tensor Flow  https://www.tensorflow.org

A large road-block to adoption of Haskell as a key programming
language for scientific computing (Machine Learning, Optimisation,
Computer Vision, etc) is the lack of strong linear algebra bindings.
There exist many work-in-progress attempts at this, but as yet there
is no haskell solution which has the comprehensiveness that you can
find in other languages (for example numpy in Python).

[Tensorflow](https://www.tensorflow.org/) is an effort by Google to produce a state-of-the-art Tensor
algebra package (a tensor is a generalisation of a matrix).  This
library is built upon a C++ base, and is capable of distributing
complex computations across a cluster. It is an ideal candidate for
large scale data analysis.

Tensorflow also implements the FP paradigm of lazy evaluation, as a
tensor flow graph is defined separately to the computation of that
graph.

Haskell tensor flow bindings would lower the barrier to entry for
computational scientists interested in using Haskell, and would result
in data analysis software stacks that were more trustworthy.

[There exist](https://github.com/tensorflow/haskell) low-level bindings to TensorFlow.

----

### Higher-Kinded Types for the Rust programming language

The Rust programming language is an improvement over C for systems
programming. While having some rudimentary programming features (unlike C), it
is missing the all-important higher-kinds.

Higher-kinds are necessary for implementing various programming abstractions
(e.g. lens, monads), with the only available alternative being to endlessly
repeat specialised instances [of what is otherwise generalised].

The creators of the Rust programming are aware of this shortcoming and seek the
necessary expertise and effort to fix it.

----

### Java Virtual Machine meta-programming library in Haskell

Programming languages such as Scala have provided a quick fix for many issues that arise when programming for the JVM. However, Scala is grossly inadequate for any robust programming, as it presents otherwise unnecessary challenges relating to the JVM. For example, one must often choose between, "working program" and "program that performs." Being forced into such a trade is often argued away as a necessity given the target platform (JVM). This is a huge lie.

Rather than design a programming language, then attempt to shoehorn it to a legacy target such as the JVM, design a meta-language for the JVM. The tools to do this in a practical way have not existed until recently (e.g. lens). Many earlier attempts to achieve this goal fell short due to a lack of tooling (e.g. ASM library) to support it.

Using Haskell, and supporting libraries, tool support for legacy targets such as the JVM can finally be realised.

----

### Open aviation data

Open-source projects such as [stratux](http://stratux.me/) provided low-cost (not necessarily certified) avionics to VFR pilots. Websites such as http://flightradar24.com/ provide real-time aviation maps to hobbyists and commercial operators, which include ADS-B information and much more (e.g. aircraft type). However, this information is proprietary, scattered around in unreliable sources and cannot be built upon in a practical way. More so, this information would be valuable to pilots if it were available.

Unifying existing ADS-B open-source projects, existing aviation data from various sources as well as existing certified aviation maps (e.g. VTC and VNC) can assist pilots in traffic collision avoidance (TCAS), flight planning, navigation, energy conservation, making fast and informed decisions in emergencies (e.g. forced landing area).

[CASA](https://www.casa.gov.au/) (the Australian aviation regulating body) regularly seeks advice from experts, especially in technology. Presenting such a system that vastly supersedes existing avionics in function and reliability is an admirable goal.

----

### Open real estate data

The act of searching for real estate, for whatever purpose, is currently a laborious, manual, error-prone task. That is with the best of tools. Does the property have internet access? Does it have line-of-sight to NBN fixed-wireless?

*todo puffnfresh*

----

### hargonaut

The [http://argonaut.io](argonaut) library was originally written by Mark Hibberd and Tony Morris using the Scala programming language. The library put an emphasis on usable error-reporting, program composition using lenses and zippers and strong type-safety. The library was originally written to parse JSON data for commercial applications and has since gained popularity. No other library exists with these goals.

There has been a strong demand for a similar library for the Haskell programming language. Existing Haskell libraries for parsing JSON do not achieve these goals, which often causes lament.

Here is [a recent thread](https://www.reddit.com/r/haskell/comments/4lxmu6/library_request_validate_json_structure_with_nice/) on this.

This is a recurring theme.

----

### geodetic libraries

Pure-functional libraries with strong type guarantees do not exist for geodetic applications. The absence of well-designed data structures to represent geodetic data results in poor program composition and a hard limit on the ability to write higher-level user libraries.

A principled approach to geodetic library design benefits all existing library users, since they no longer must make a (perpetual) trade between being boxed in by limitations of existing libraries, or implementing programs that simply don't work.

----

### Distributed Geospatial Versioning System

Create a data structure that can store GIS features in a canonical way that allows diffing/branch/fork/rebase/immutable model found in Git.  This would be a way to implement a cadastre system but instead of being centralised and controlled by a single entity or government it could be used collabaoratively by GIS users (developers, surveyors, governments, etc). A change to the cadastre system could be a pull request from a 3rd party (like a surveyor).  An example of a similar system can be found at http://geogig.org/

### Constrained lens/optics

Generalising optics (c.f. [van Laarhoven](http://www.twanvl.nl/blog/) lenses) to solve such issues as The Expression Problem (c.f. [Tony Morris, Lambdajam 2016](http://tonymorris.github.io/talks/#9ae5e0fa2e1b0db7589dc5398bab4b07dc971e21)) is a long-standing problem. Edward Kmett implements a library that exploits `ConstraintKinds` in the Glasgow Haskell Compiler (GHC), which provides an optimal approach to achieving this generalisation.

http://hackage.haskell.org/package/constraints

----

### typelead/eta (formerly GHCJVM)

----

### argonaut/xml

----

### Typed assembly languages

There are techniques that come from [typed assembly languages](https://www.cs.cornell.edu/talc/) that can be used to make code generation easier and more likely to be correct.
These could be targetted to LLVM and JVM and refined, to enable various language and platform agnostic tooling.

There has been some recent success with language agnostic descriptions of problems coupled with code generators in the [Swagger](http://swagger.io/) project for REST APIs, and there are some othe areas where taking this approach could make some exciting technologies available to people working in industry.

----

### Session types

Session types provide a typing discpline for protocols, and checking that no communication errors or deadlocks will occurr.
There are [various implementations](http://simonjf.com/2016/05/28/session-type-implementations.html) that exist with various levels of maturity.

The combination of
- a language-agnostic description of protocols,  
- a tool to verify the validity of procotols, and
- a set of code-generator for various languages (a la Swagger)
could make it easier for programmers to develop code for protocols with high confidence, particularly in settings where the various endpoints may be implemented in different languages or for different platforms. 

----

### Event sourcing tools

Event source and CQRS are another area where there are [tools and techniques](https://www.youtube.com/watch?v=d1zFoFlIneo) that could be more widely applied, and where the combination of language-agnostic descriptions of the problems and code generation could bear fruit.

Unlike with sessions types, there are several processes and tools used in these environments that could be written in a generic manner.

----

### A modular tookit for domain-specific languages (DSL)s

When programming languages are formalized, they are often presented incrementally.

Many of the increments can be captured into components, containing the relevant fragments of the grammar, semantics, typing rules, pretty printing and test data generation.

A toolkit of these components would make it significantly easier for programmers to focus on the domain-specific parts of designing DSLs.

The system would be widely useful when the set of components were built up at least until the point where they could work with System F.
Adding support for linear types or region inference would extend the usefulness.

Such a toolkit should allow for the development of tooling - including REPLs, debuggers, code formatters and documentation tools - and test suites than can be reused by the various permutations of the components, which would increase the utility of such a toolkit.

