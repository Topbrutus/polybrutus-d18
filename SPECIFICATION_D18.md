# Polybrutus D18 — Exact twenty-three-point Euclidean configuration

**Frozen parent:** `Topbrutus/polybrutus-d17@v0.1.0`, commit `1ef37f156292aa80f8c3f5d07bb889dc4b4492ab`, DOI `10.5281/zenodo.24409067`.

Let `p1,...,p22` be the exact frozen D17 radius-one vectors in 18 coordinate-storage slots. The five-simplex coordinate block obeys one exact zero-sum constraint. Embed every old vector as `q_i=(p_i,0)` in 19 storage-coordinate slots, and append `q23=e19=(0,...,0,1)`, orthogonal to all old vectors.

For each old point:
```
||q23-q_i||²=||q23||²+||q_i||²-2<q23,q_i>=2.
```
For arbitrary radius `R>0`, scale all points by `R`, giving new squared distances `2R²`. Preserve **all 231 predecessor labelled pair distances** and add 22 pairs to reach `C(23,2)=253`. The intrinsic exact affine dimension is **18**, despite the 19 storage slots.

For `k=4d²/R²`, normalized families are `4:6,7:2,8:222,9:3,10:10,12:6,13:2,16:2`; the exact sum of squared distances is `2071R²/4`. At radius one the coordinate centroid is `(0,0,1/46,0,0,0,0,0,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23)`.

## A chosen ideal weighted oscillator graph

With unit scalar masses and mathematically chosen complete-graph weights `w_ij=R²/d_ij²`, the added 23rd vertex couples uniformly with weight 1/2 to the 22 predecessor vertices. For the predecessor graph Laplacian `L17`,
```
L18 = [ L17 + (1/2)I22      -(1/2)1 ]
      [ -(1/2)1ᵀ                   11 ].
```
The exact characteristic polynomial satisfies
```
chi23(z)=z(z-23/2)*chi22(z-1/2)/(z-1/2)
        =z(z-23/2)^12(z-11)^4 f6(z-8),
f6(z)=chiP7(z)/z.
```
Eigenvalue 23/2 has exact multiplicity 12, and eigenvalue 11 multiplicity 4. These are model-specific dimensionless eigenvalues, not observed frequencies.
