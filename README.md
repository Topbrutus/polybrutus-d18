# POLYBRUTUS 18D — Exact Euclidean 23-point metric and a twelvefold ideal graph mode

**Human researcher and scientific responsibility:** Gabriel St-Pierre, independent researcher.  
**Scientific status:** exact computational mathematics preprint, not independently human peer reviewed.  
**Generative AI disclosure:** OpenAI ChatGPT (Astra) substantially assisted the two separately coded mathematical checkers, chosen theoretical graph model, provenance, scientific drafting and archival workflow. AI is not an author.

## Exact verified results (radius R=1)

- **23 labelled vertices**, **253 exact pairwise squared distances** and minimal affine Euclidean embedding dimension **18**.
- The immutable Polybrutus D17 predecessor retains all **231/231 labelled squared distances** without moving any previous point. Adding one orthogonal unit vector introduces **22 new distances squared, all exactly 2**.
- Eight normalized squared-distance classes `k=4d²/R²`: `{4:6,7:2,8:222,9:3,10:10,12:6,13:2,16:2}`.
- Exact sum of squared pairwise distances: `2071 R²/4`.
- Coordinate-difference rank **18**, centered Euclidean squared-distance Gram rank **18**, and exact positive-semidefinite Gram identity `B=(HX)(HX)^T`. The embedding uses 19 storage-coordinate slots but one exact simplex-hyperplane relation.
- **Chosen theoretical scalar-oscillator complete graph:** unit masses and inverse-squared-distance weights `w_ij=R²/d_ij²`; the exact weighted graph Laplacian has eigenvalue **23/2** with multiplicity **12**, and eigenvalue **11** with multiplicity **4**. These are model eigenvalues, not measured frequencies.
- Two **separately implemented** symbolic/rational verifier programs confirm all **253/253** labelled distances, prior 231 distances, affine and Gram rank, and exact eigenvalue multiplicities. Four deliberately invalid cases are detected.

## Reproduce

```sh
python -m pip install sympy==1.14.0
python src/verify_d18.py
python tests/independent_d18.py
```

The second checker does not import the primary or predecessor point generator. `prior/` contains fixed source programs and metric certificates copied from the immutable D17 source tag `Topbrutus/polybrutus-d17@v0.1.0`, commit `1ef37f156292aa80f8c3f5d07bb889dc4b4492ab`.

## Research archive

- `src/verify_d18.py`: exact metric, Gram rank and factorization, model characteristic polynomial, four negative controls.
- `tests/independent_d18.py`: independently written rational metric and full exact characteristic-polynomial multiplicity checks.
- `results/certificate_d18.json`: exact squared distances for all 253 labelled pairs plus polynomial, rank and provenance.
- `SPECIFICATION_D18.md`, `PREUVE_D18.md`, `PROVENANCE.md`: specification, proof and source chain.
- `publication/POLYBRUTUS_18D_NOTE.pdf` and `.md`: CC BY 4.0 scientific preprint. Code MIT.
- `SHA256SUMS.txt`: source Git blob checksums, frozen with scientific tag.

**Published predecessor:** [Polybrutus D17, DOI 10.5281/zenodo.24409067](https://doi.org/10.5281/zenodo.24409067).  
**Canonical seven-point source:** https://github.com/Topbrutus/polybrutus/blob/main/SPECIFICATION.md

**Scientific limitations:** Orthogonal completions and uniformly joined weighted graph spectral shifts are established mathematics. This is a reproducible **specific** 18D labelled metric, not a new physical extra dimension, discovery of a novel universal theorem or observed natural resonance.
