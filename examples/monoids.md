```
M : Circle
e : M
* : M -> M -> M
lunit : (x : M) -> e * x =_M x   // is this a functor Tw(Γ) -> Set?
runit : (x : M) -> x * e =_M x
assoc : (x y z) -> (z * y) * x = z * (y * x)
```

## Semantics
context         category
substitution    functor
type            displayed cat
term            section

jud form type   Γ^op -> Set
inf rule type   Tw(Γ) -> Set
- non-dep inf rule tpe   Γ^op x Γ -> Set
- dep inf rule type      Tw(Γ) -> Set
**small type**  Γ -> Set

## From small types to inf rule type
Is there a general construction that takes:
- A : Γ -> Set
- B : ∫_Γ A -> Set
and gives
- ΠAB : Tw(Γ) -> Set

ΠAB (γ0 --f--> γ1) = (a : A γ0) -> B (γ1 , (fmap[A] f) a)

## System Fω
(Can we have bivariant jud form types?)
```
KSub : KCtx -> CovPsh(KCtx)
```
