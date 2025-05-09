## Examples
- enriched category
  - structures on enriched categories
- adding stuff to languages
  - polymorphism
  - parametricity?
  - LF
- FOLDS paper: different sorts have different h-levels

## Semantics
requirement     V monoidal cat  V has displayed objects

context         Category        CwF
substitution    functor         CwF morphism
type            displayed cat   displayed CwF
term            section         section

jud-form-types  Γ^op -> Cat     ?
inf-rule-types  Γ^op x Γ -> Set ?
- Because you have both input & output for chosen sorts
- Even for directed output types, you view them as sets, because model morphisms should preserve them on the nose, not laxly/pseudo.
- Should we specify that these are function types with covariant domain (premises) & covariant codomain (conclusion)?
                Σ(Argtype : Γ -> Set) . (∫_Γ Argtype -> Set)
  What do Kaposi et al. do? I think they have a separate argument, to prove that you have syntax models. So I think `Γ^op x Γ -> Set` is good enough here.
  
small types     Γ -> Set (Paige says maybe Γ -> Cat, this is still Conduché)
  (i.e. single judgements; the things occurring as the domain of a ∏-type)
