# Polybrutus D18 — Reproducible exact metric and model spectrum certificate

## 1. Conservative labelled metric

The prior D17 metric has 22 unit vectors and 231 exact labelled squared distances. Extend every vector with one zero coordinate and add a new orthogonal unit vector. All old squared distances are identical and all new pair distances have square `1+1=2`. Thus 231 old + 22 new = **253** labelled unordered pairs. The histogram for `k=4d²/R²` is `{4:6,7:2,8:222,9:3,10:10,12:6,13:2,16:2}`; the squared-distance sum equals `2071R²/4`.

## 2. Exact minimal affine rank and Euclidean realizability

Let `X` denote the exact 23-by-19 stored coordinate matrix, `D` the exact 23-by-23 **squared Euclidean distance matrix**, and `H=I-11ᵀ/23` the centering projection. Symbolic exact computation proves
```
rank([q2-q1,...,q23-q1])=18
rank(B)=18
B=-(1/2)HDH=(HX)(HX)^T.
```
The final identity proves positive semidefiniteness. Because a complete *labelled* Euclidean squared-distance matrix uniquely determines its centered Gram matrix, **every Euclidean realization** of these 253 pair distances has affine rank exactly 18. Storage-coordinate count 19 includes one constrained simplex direction.

## 3. Chosen graph spectrum

Assign a hypothetical scalar oscillator with unit mass to each vertex, with chosen complete-graph weights `w_ij=1/d_ij²`. The new 23rd vertex has uniform coupling weight 1/2 to all 22 predecessor vertices. Thus
```
L18=[ L17+(1/2)I22  -(1/2)1 ]
    [ -(1/2)1ᵀ             11 ].
```
Separating global uniform, new differential and old shifted nonuniform modes yields
```
chi23(z)=z(z-23/2)*chi22(z-1/2)/(z-1/2).
```
The frozen predecessor had `chi22(z)=z(z-11)^11(z-21/2)^4 f6(z-15/2)`, where `f6(z)=chiP7(z)/z` is the six-nonzero-mode polynomial of the original seven-point graph. Exact substitution gives
```
chi23(z)=z(z-23/2)^12(z-11)^4 f6(z-8).
```
The primary program independently computes the entire exact 23-by-23 characteristic polynomial and verifies the recurrence and closed form. Values `f6(7/2) != 0` and `f6(3) != 0` exclude hidden higher multiplicities: **23/2 exactly twelvefold** and **11 exactly fourfold**. A separate rational-distance implementation reconstructs the complete weighted graph and verifies both multiplicities by exact polynomial derivatives.

## 4. Independent checks and falsification

All **253** labelled exact squared distances are reconstructed independently from rational canonical seven-point rules, five simplex vertices with internal squared distances `5/2`, and eleven perpendicular unit basis vertices. The 231 frozen predecessor values are checked pair by pair, not merely by distance histogram. Four negative controls reject a corrupted labelled pair, a duplicated vertex with rank loss, a tilted nonorthogonal addition, and relabelled points that preserve histogram but not labelled distances.

No independent human peer review, physical frequency measurement, new particle or novel universal mathematical theorem is claimed.
