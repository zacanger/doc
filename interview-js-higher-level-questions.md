* what are some programming paradigms?
  * objects linked to other objecs (oolo) (aka prototypal inheritance)
  * functional programming (closures, first class/higher-order functions)

* fp in a nutshell?
  * avoid shared state and mutable data
  * js was originally conceptualized as scheme for the browser!
  * pure functions (same input means same output, every time)
  * composition (break things down smaller so one can build them up from reusable bits)
  * langs: hs, ml, f#, ocaml, erlang, lisp(s), elm (sorta), erlang, clojure
  * functions as arguments

* inheritance
  * classical
    * class -> instances
    * subclasses (hierarchies)
    * 'new' or 'class' keywords
    * is-a type of relationship
  * prototypal
    * has-a, uses-a, or does-a type of relationships
    * object -> instances
    * factory functions or Object.create()
    * can be composed from other objects
    * types
      * delegation (prototype chain)
      * concatenative (mixins; Object.assign())
        * copies values from one obj to another
        * can work with multiples, e.g. `let finalObj = Object.assign(firstObj, secondObj, thirdObj)`
        * doesn't work on 'non-enumerable own properties' (lol wat)
          * if property is created with Object.defineProperty() basically i guess
      * functional (using closure to create private state)

* oop vs fp
  * oop
    * pros
      * easily comprehended
      * imperative, which is straightforward to read sortakinda
    * cons
      * often depends on shared state
      * multiple entities (behaviors, properties, whatever) may be attached to the same
        'parent,' which would make them all dependent on that parent's state
  * fp
    * pros
      * avoids shared state (so, no actions trying to compete for or access the same resource(s))
      * becomes more readable (because imperative programming gets really verbose/hairy sometimes)
      * lends itself very well to composition (build this thing out of all these small things)
    * cons
      * _can_ reduce readability, if stuff is too abstract
      * higher learning curve, usually
      * relies somewhat on knowledge of category theory, algebras, and lambda calculus

* favour composition over inheritance
  * code reuse with smaller bits composed into bigger bits
  * avoids hierarchies
  * avoids gorilla-banana problem
  * helps with flexibility, refactoring, code portability

* data binding, data flow
  * two-way data-binding
    * ui bound to model bound to ui
    * when ui changes, model changes. when model changes, ui changes.
  * one-way data-flow
    * model is single source of truth
    * ui changes trigger messages that say we want to change the model ('store' in react)
    * only model can change state

* monolithic vs micro
  * monolithic architecture
    * app is one unit of code
    * bits share memory, resources
    * tightly integrated
  * microservice architecture
    * small, independent applications
    * own memory space
    * independent scaling

* async
  * synchronous code is executed sequenially
  * can block things while waiting on net, IO, etc
  * asynchronous code doesn't block
  * (node's event loop, for example)

