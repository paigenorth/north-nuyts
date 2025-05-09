```
Obj : Circle
Hom : Obj -> Obj -> Circle
id : (x : Obj) -> Hom x x
_º_ : (x y z : Obj) -> Hom y z -> Hom x y -> Hom x z
lunit : (x y : Obj) -> (f : Hom x y) -> id y º f = f
runit : (x y : Obj) -> (f : Hom x y) -> f º id x = f
assoc : (w x y z : Obj) -> (f : Hom w x) (g : Hom x y) (h : Hom y z) -> (h º g) º f = h º (g º f)
```

## Semantics (copied from monoids.md)
context         category
substitution    functor
type            displayed cat
term            section

jud form type   Γ^op -> Set
inf rule type   Tw(Γ) -> Set
- non-dep inf rule tpe   Γ^op x Γ -> Set
- dep inf rule type      Tw(Γ) -> Set
small type      Γ -> Set


