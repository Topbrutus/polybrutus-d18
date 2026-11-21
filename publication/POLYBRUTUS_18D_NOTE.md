# Polybrutus 18D: Exact Conservative Euclidean Completion and a Twelvefold Weighted-Graph Mode

**Research author:** Gabriel St-Pierre  
**Affiliation:** Independent researcher  
**Project:** Polybrutus-X72  
**Date:** 20 November 2026  
**Version:** 0.1.0  
**Status:** Reproducible computational mathematics preprint; not independently human peer reviewed  
**Predecessor:** Polybrutus 17D, DOI 10.5281/zenodo.24409067  
**Frozen scientific source:** https://github.com/Topbrutus/polybrutus-d18/tree/v0.1.0 (upon release)

## Abstract

We construct an exact **twenty-three-point labelled Euclidean configuration** with **minimum affine dimension eighteen**, by conserving all **231 labelled squared distances** of the published Polybrutus 17D metric and adjoining one further orthogonal radius-R point. The new point introduces **22 squared pair distances of exactly 2R²**, yielding **253 labelled pair distances** in eight exact normalized families. Exact coordinate-difference rank and centered squared-distance Gram rank both equal eighteen, and an explicit algebraic Gram factorization establishes positive semidefiniteness. A separately programmed rational-metric verifier reconstructs all 253 labelled distances and confirms the minimal affine rank without importing the primary geometric generator.

For a **chosen theoretical complete weighted-graph scalar-oscillator model**, with equal unit masses and couplings `w_ij=R²/d_ij²`, the full 23-by-23 graph Laplacian has an eigenvalue **23/2 of exact multiplicity twelve** and an eigenvalue **11 of exact multiplicity four**. Both properties are reproduced in two exact symbolic/rational implementations. No physical eighteen-dimensional spacetime, experimentally measured resonance, particle discovery, or novel universal mathematical theorem is claimed.

## 1. Frozen provenance and research context

Polybrutus begins with seven analytically defined points on a Euclidean three-sphere surface of radius R (a two-dimensional sphere embedded in three-dimensional space). The original analytic coordinates were preserved in the first higher-dimensional extension, which added five regular-simplex vertices in an orthogonal four-dimensional subspace. The resulting twelve-vertex, sixty-six-pair metric with affine rank seven was deposited as Polybrutus 7D, DOI **10.5281/zenodo.24407952**.

Later dimension-specific computational case studies extended this labelled metric by one new perpendicular radius-one point per dimension: Polybrutus **8D** (13 vertices, 78 pairs, DOI 10.5281/zenodo.24408344), **9D** (14, 91, DOI 10.5281/zenodo.24408448), **10D** (15, 105, DOI 10.5281/zenodo.24408569), **11D** (16, 120, DOI 10.5281/zenodo.24408650), **12D** (17, 136, DOI 10.5281/zenodo.24408720), **13D** (18, 153, DOI 10.5281/zenodo.24408769), **14D** (19, 171, DOI 10.5281/zenodo.24408836), **15D** (20, 190, DOI 10.5281/zenodo.24408887), **16D** (21, 210, DOI 10.5281/zenodo.24408979), and **17D** (22, 231, DOI 10.5281/zenodo.24409067).

The present research starts solely from the **immutable Git tag** `Topbrutus/polybrutus-d17@v0.1.0`, commit **`1ef37f156292aa80f8c3f5d07bb889dc4b4492ab`**, whose exact source and metric certificates from D08 through D17 are copied unchanged into `prior/`. We do not change any earlier labelled point, source tag, published DOI or metric.

## 2. Exact twenty-three-point Euclidean metric

Set normalized radius `R=1`. Let `p1,...,p22` denote the exact frozen 17D unit vectors in eighteen coordinate-storage slots. The original regular-simplex block occupies a centered four-dimensional hyperplane in five storage coordinates, imposing one linear relation.

Append a zero coordinate to each old vector:

```
q_i=(p_i,0),         i=1,...,22.
```

Introduce the twenty-third vector as the perpendicular unit basis direction in a new nineteenth slot:

```
q23=e19=(0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1).
```

All 23 points have unit norm and `q23` is orthogonal to all 22 predecessor vectors. No former point moves, so all **231 labelled squared predecessor distances** remain identical. Each new pair satisfies:

```
||q23-q_i||²=||q23||²+||q_i||²-2<q23,q_i>=2,   i=1,...,22.
```

Scaling all coordinates by arbitrary radius `R>0` changes every squared distance by a factor `R²`, giving the twenty-two new values `2R²`. The total labelled unordered pair count is therefore

```
C(23,2)=253=231+22.
```

Define the exact normalized squared-distance family parameter `k=4d²/R²`. Its complete histogram is:

| k | 4 | 7 | 8 | 9 | 10 | 12 | 13 | 16 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Labelled pairs | 6 | 2 | **222** | 3 | 10 | 6 | 2 | 2 |

These eight multiplicities sum to 253. Their exact squared-distance total equals:

```
sum_{i<j} d_ij²/R² = 2071/4.
```

At radius one, the nineteen-slot exact centroid is

```
G=(0,0,1/46,0,0,0,0,0,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23,1/23).
```

The number of coordinate slots is **nineteen**, but the metric's intrinsic minimal affine rank is **eighteen** due to the one exact simplex coordinate relation. This distinction is fundamental.

## 3. Exact certificate of minimum affine dimension eighteen

Let `X` be the **23-by-19** exact coordinate matrix and `D` the symmetric **23-by-23 matrix of squared Euclidean distances** between labelled points. Define the exact centering projection `H=I-11ᵀ/23` and the centered Euclidean-distance Gram matrix:

```
B = -1/2 H D H.
```

The primary symbolic verifier independently checks all three exact equalities without numerical approximations:

```
rank([q2-q1,...,q23-q1]) = 18;
rank(B) = 18;
B = (H X)(H X)^T.
```

The last equality establishes positive semidefiniteness through an **exact algebraic factorization**, rather than approximate floating-point eigenvalues. Since a complete labelled Euclidean squared-distance matrix uniquely determines the centered Gram matrix, **every Euclidean realization of these exact 253 labelled squared distances** has affine dimension eighteen. That is the precise mathematical content of the phrase *Polybrutus 18D*.

A separate independently implemented rational checker reconstructs each squared distance without importing the primary geometric generator. It uses rational coefficients of the original seven points (including the exact `sqrt(3)` factor encoded through a quadratic form), five mutually equidistant simplex points with squared internal distances `5/2`, and eleven additional mutually perpendicular radius-one unit directions. It confirms **253/253** labelled squared distances, **231/231** old distances and the centered Gram rank **18**.

## 4. A twelvefold eigenvalue in a chosen weighted-graph model

Choose a mathematical complete graph on the 23 labelled vertices. Assign hypothetical equal unit scalar masses and positive all-pairs pair weights `w_ij=R²/d_ij²`. This choice defines a **model**. It is not inferred from an experimental instrument.

The new vertex has squared radius-normalized distance 2 to every old vertex, so all twenty-two newly added graph couplings have weight `1/2`. Let `L17` denote the 22-by-22 weighted graph Laplacian of the parent, and `L18` the 23-by-23 new Laplacian. The exact block relation is:

```
L18=[ L17+(1/2)I22      -(1/2)1 ]
    [ -(1/2)1ᵀ                11 ].
```

Writing the characteristic polynomials `chi22(z)=det(zI-L17)` and `chi23(z)=det(zI-L18)`, the uniform zero mode and the intergroup mode give the following exact recurrence:

```
chi23(z)=z(z-23/2)chi22(z-1/2)/(z-1/2).
```

The frozen Polybrutus 17D case has the factorized predecessor polynomial

```
chi22(z)=z(z-11)^11(z-21/2)^4 f6(z-15/2),
f6(z)=chiP7(z)/z,
```

where `chiP7` is the original seven-point complete weighted-graph characteristic polynomial, and `f6` describes its six nonzero modes. Substitution produces the explicit factorization

```
chi23(z)=z(z-23/2)^12(z-11)^4 f6(z-8).
```

The primary verifier computes the **complete exact 23-by-23 characteristic polynomial** directly and checks that it equals both the recurrence and the closed form. It also checks `f6(7/2)!=0` and `f6(3)!=0`, excluding accidental additional factors at the named roots. Thus the model has eigenvalue **23/2 with exactly twelvefold multiplicity** and eigenvalue **11 with exactly fourfold multiplicity**.

The second program reconstructs the graph directly from its independently derived rational metric, computes the full exact characteristic polynomial, and checks its root multiplicities via the vanishing and nonvanishing of successive polynomial derivatives. These numbers are normalized, dimensionless **model eigenvalues**, not measured frequencies in hertz.

## 5. Reproducibility and negative controls

The frozen source contains `src/verify_d18.py`, `tests/independent_d18.py`, `results/certificate_d18.json` listing **all 253 exact labelled squared distances**, copies of predecessor programs and metrics in `prior/`, mathematical specification and proof, source provenance, GitHub Actions workflow and an SHA-256 Git-blob index.

Reproduction commands:

```sh
python -m pip install sympy==1.14.0
python src/verify_d18.py
python tests/independent_d18.py
```

Both programs must report PASS and the **same SHA-256** for the regenerated JSON certificate. Four deliberately invalid cases are rejected: tampering with a squared-distance entry, duplicating a vertex and losing the new affine direction, tilting the newly adjoined unit vector toward the original geometry, and swapping point labels while keeping the unlabelled histogram unchanged.

The Zenodo record will contain exactly three scientific attachments: the immutable source ZIP created using `git archive v0.1.0`, the present scientific PDF note, and the exact JSON labelled-distance certificate. Their byte lengths and cryptographic hashes permit external verification and reconstruction.

## 6. Scientific precedence, scope and limits

Orthogonal completion of Euclidean configurations, centered squared-distance Gram matrices and the spectrum of uniformly joined weighted graphs are **established mathematical methods**. This manuscript contributes one explicit computationally reproducible **particular 18D labelled configuration and model graph**, not discovery of those general mathematical operations. Its affine rank statement does **not** imply that physical spacetime has eighteen dimensions. The hypothetical graph model is not an experiment, measured vibration, elementary particle interaction or physical frequency.

Independent human mathematical peer review has not taken place.

## 7. Research authorship, AI disclosure and licensing

**Human research author and scientifically responsible investigator:** Gabriel St-Pierre, independent researcher. He originated the Polybrutus programme, established the dimension-specific publication procedure, and directs the investigation.

**Generative AI disclosure:** OpenAI ChatGPT (Astra) substantially assisted exact symbolic proof and verification, design and implementation of primary geometry software and an independently coded rational-metric checker, chosen theoretical graph-spectral analysis, GitHub provenance auditing, scientific manuscript drafting, documentation and archival release operations. The AI is **not** listed as a research author. Human peer review remains pending.

**Licenses:** scientific paper and prose CC BY 4.0; research source code MIT.

**Source lineage:** canonical original Polybrutus https://github.com/Topbrutus/polybrutus/blob/main/SPECIFICATION.md ; frozen D17 source https://github.com/Topbrutus/polybrutus-d17/tree/v0.1.0 ; predecessor DOI https://doi.org/10.5281/zenodo.24409067 ; full earlier DOI chain in the repository's `PROVENANCE.md`.
