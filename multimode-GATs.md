# Multimode GATs - April 2026 - Andreas

## Contextual and multimode GATs
In May '25, we discussed:
- contextual GATs, which have a directed sort of contexts and undirected sorts of terms and types
- GATs which have sorts living in various modes (I will now call them modes, we've been calling them sorts last time but I think that was misleading). I will call these **multimode GATs**.

## Enriched GATs?
We had also seen a connection to enriched category theory. At the moment, I fail to reconstruct the connection. I have two candidates that we might have been thinking of:
1. Enriched categories have a sort of objects that is in the mode of sets, and a dependent sort of morphisms at mode V. As such, they are a familiar example of a multimode GAT. Perhaps for that reason, we just started to call them enriched GATs?
2. Directed sorts, such as the sort of contexts of a contextual GAT, take semantics as objects in Cat. Cat is a 2-category, i.e. a Cat-enriched category. Did we want to generalize from there, going to V-enriched categories?

## Multimode MATs

### Definition
Given:
- a mode theory, i.e. a 2-category `M` of modes, modalities and 2-cells,
- a semantics of the mode theory, i.e. a 2-functor `M^coop -> {Categories, Adjunctions}`
- a collection of mode-indexed sorts,

It is quite straightforward to define what is a MAT for that setup:
- a bunch of operations
- each operation lives at some mode `q`,
  - has output sort of mode `q`
  - has as arity, an MTT context of mode `q`.
    Do wee allow locks in that context?
    - if no: then we can simplify the mode theory semantics to `M -> Cat`
    - if we want to consider GATs rather than MATs, then we probably need to have DRAs in the semantics in order to be able to express what premises we require for a rule to be well-formed.
- each equation rule lives at some mode `q`,
  - equates two MTT expressions of a sort at mode `q`
  - has as arity, an MTT context of mode `q`.
  
If we want to be able to consider substructural modes (e.g. a monoidal category V without assuming that it is cartesian), then we need a richer system than MTT.

### Model
A model consists of:
- for every sort, an object in the semantics of the corresponding mode
- semantics for each of the operations, in the obvious sense,
- satisfying the equation rules, in the obvious sense.

## Guiding examples
Let's consider some examples in a manner as faithful as possible, in order to get a view on what features are required of a fully powerful formalism for multimode ATs.

### Enriched categories
Mode theory:
- Set, the category of sets
  - the universe of sets is a set UniSet
- V, a monoidal category
  - not necessarily cartesian, so at mode V, we have an affine logic
  - not necessarily closed, but we do have external Homs, i.e. function types at mode Set.
  - the universe of V-objects is a set UniV
  
Sorts:
- Obj : UniSet @ Set
- Hom : Obj -> Obj -> UniV @ Set

Operations:
- id : (x : Obj) -> I -o Hom x x @ Set
- comp : (x y z : Obj) -> Hom y z ⊗ Hom x y -o Hom x z @ Set

Laws:
...

Can we clean this up by extending V with:
- internal Homs, (co)freely?
- products, (co)freely?
- even coproducts, freely, so that we get a modality Set -> V?

### Conclusion from 1 guiding example
- for every mode, you use the internal language of that mode,
- you need appropriate stuff to tie those languages together.

If your modes are all structural models of DTT, and there are plenty of DRAs in between, then we can use MTT.
Otherwise, you need other funky stuff.
Specifically, for contextual GATs, I think we need 2DTT, 2-dimensional directed type theory.
