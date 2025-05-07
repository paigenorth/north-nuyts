## Related papers
- signature language for SOGATs: https://dl.acm.org/doi/pdf/10.1145/3290315
- bicat TT Paige: https://doi.org/10.1017/S0960129523000312
- Laretto: https://iwilare.com/directed-equality-for-coend-calculus.pdf

## Two-sides semantics of SigCGAT

### Judgement forms

#### Take 2
```
Γ ctx           means Γ is a cat with class of tight homs
Γ |– T dtype    means Γ.T -> Γ with class of tight homs over tight homs
Γ |– T utype    means Γ.T -> Γ where all homs over a tight hom are tight
terms           sections sending tight to tight
```

```
Γ |– A B dtype
-------------------
Γ |– A -> B dtype

```

#### Take 3
```
Γ ctx           means Γ is a cat with class of tight homs
Γ |– T dtype    means T : Γ^op x Γ -> Cat
Γ |– T utype    means T : Γ^op x Γ -> Set
terms           live in the (lax) end (tight homs are sent to isos in the cospan tip)
non-dep terms   are just functors inverting tight homs
in particular:
Γ |– T : \Circ  is something like a (contravariant) functor to Set
Γ.T             diagonal-two-sided Grothendieck construction of T
```

Function types take only `T : \Circ` and `T : \Triangle` as domain so they remain cleanly bivariant.
