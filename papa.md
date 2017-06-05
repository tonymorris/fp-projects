# General prelude for haskell (called papa)

### Goals

* to remove unsafe functions from default scope. For example, `head`.
* to reimplement removed functions with a safe type.
  * for example, `head :: Cons s s a a => s -> Maybe a`
* to re-export common modules at a top-level module.
  * for example, `Control.Lens` and `Data.Semigroupoid`.
* to read a source file and know which module an identifier comes from.
  * The top-level Papa module is imported with everything implied.
  * All other modules explicitly import identifiers. 
* to use a prototype project for internal build infrastructure.
* to provide subsequent projects a quick way to import 

### packages

##### `papa`

Top-level package which exports all others.

##### `papa-base`

Exports modules in `base` that are safe and useful to have re-exported into
default scope.

----

*The following packages depend on one or more third-party packages, expressed in
the package name. It is a potentially large size, depending on the tree of
required packages.*

##### `papa-lens`

Re-implementations of functions that necessarily depend on the `lens` package.

##### `papa-semigroupoids`

Re-implementations of functions that necessarily depend on the `semigroupoids` package.

##### `papa-lens-semigroupoids`

Re-implementations of functions that necessarily depend on the `lens` package and the `semigroupoids` package.

##### `papa-bifunctors`

Re-implementations of functions that necessarily depend on the `bifunctors` package.

*(etc etc)*

----

