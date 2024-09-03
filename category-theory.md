# Category Theory

## Rules

* There are `objects` and `arrows` (morphisms)
* Composition:
  * If there's a morphism `f` from `A` to `B`, and there's a morphism `g` from
    `B` to `C`, there must be a morphism from `A` to `C` (`g . f`).
  * `const compose = (f, g) => (x) => f(g(x))`
* Associativity of composition: `(h . g) . f == h . (g . f)`
* Identity: For each `A` there must be a morphism from `A` to `A`.
  * `const id = a => a`

## Types

Types are sets of values>

In Set, objects are sets and morphisms are functions, and idenity maps each
element to a set of itself.

Bottom (`⊥`) is a value in every type, corresponding to a non-terminating
computation. Functions that can return bottom are partial functions.

`Void` is a type with no values (empty set). There's only one function that can
return `Void`, which is an idenity of `Void`:

```haskell
voidIdentity :: Void -> Void
voidIdentity a = a
```

`()` is called 'unit,' which is similar to `void` in imperative languages (think
C++). Usually used for functions with side effects or that discard arguments.

```haskell
foo :: Char -> ()
foo _ = ()
```

There are two possible functions that just take a `Bool` and return a `Bool`:

```javascript
const id = a => a
// id(true) -> true
const not = a => !a
// not(true) -> false
```

## Orders

* Preorder is a category where morphisms are relations of being less than or
  equal.
* Partial order is preorder where for all `a <= b` and `b <= a`, `a == b`.
* Linear order (aka total order) is partual order where any two objects are in a
  relation with each other, one way or another.
* Hom-set is a set of all morphisms from `a` to `b` in category `C` (`C(a, b)`).

## Monoid as Set

Monoid is a set with binary operation which is associative, and there must be a
`unit` in the set.

```haskell
-- the Monoid type class:
class Monoid m where
  mempty  :: m
  mappend :: m -> m -> m
```

## Misc

```javascript
const left = a => ({ type: 'left', value: a })
const right = a => ({ type: 'right', value: a })
const m = e => {
  if (e.type === 'left') return e.value
  else return e.value ? 0 : 1
}
```
