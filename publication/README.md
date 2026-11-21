# Polybrutus D18 — Controlled scientific release

This is an unreviewed mathematical preprint with disclosed generative AI support.

1. Run both exact and independently coded verification programs and require identical JSON certificate SHA-256.
2. Create a **private** GitHub repository and make both tests pass in GitHub Actions.
3. Freeze the tested commit under annotated tag `v0.1.0`, without moving prior releases.
4. Build source ZIP with `git archive v0.1.0`; hash source ZIP, PDF and JSON and stage exactly those three in **one direct Zenodo draft**.
5. Verify draft metadata: author, CC BY 4.0, parent DOI, frozen Git tag, complete AI disclosure, and exact file checksums.
6. Make GitHub public, confirm the tag commit via unauthenticated public GitHub API, publish the **same** Zenodo draft, and verify DOI and three file checksums in public Zenodo API.
7. Add DOI to README, CITATION.cff, manifest and Memoria; preserve frozen scientific tag.

Do not create a duplicate record through automated GitHub Zenodo harvesting. No secrets or private chats in public Git.
