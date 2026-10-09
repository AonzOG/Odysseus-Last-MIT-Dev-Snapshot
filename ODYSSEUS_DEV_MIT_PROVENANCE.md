# Odysseus: historical MIT-licensed `dev` source provenance

**Record prepared:** 9 October 2026 (Fiji time)  
**Preservation repository:** https://github.com/AonzOG/Odysseus-Last-MIT-Dev-Snapshot  
**Original upstream repository:** https://github.com/odysseus-dev/odysseus  
**Original upstream branch:** `dev`

## 1. Original MIT-licensed source revision

- **Original upstream Git commit SHA:** `bdbe69946f66305a8b4d1577eeaf1f4e398f6660`
- **Original source Git tree SHA:** `4701eedf3af9c2a434375ad4c3e8f0c75ad7d097`
- **Original MIT `LICENSE` Git blob SHA:** `7087e2d598700ecb40f09a0fbf3f12952fcf641e`
- **Original commit timestamp:** 9 June 2026, 20:44:38 UTC (10 June 2026, 08:44:38 Fiji time).
- **Tracked files in original source tree:** 1,022.
- **License evidence:** At the pinned commit, the original upstream `LICENSE` starts with `MIT License`, and the upstream `README.md` identifies its license as MIT and refers to `LICENSE` and `ACKNOWLEDGMENTS.md`.

Primary evidence:

- Historical upstream MIT commit: https://github.com/odysseus-dev/odysseus/commit/bdbe69946f66305a8b4d1577eeaf1f4e398f6660
- Exact upstream snapshot: https://github.com/odysseus-dev/odysseus/tree/bdbe69946f66305a8b4d1577eeaf1f4e398f6660
- MIT license as present in that commit: https://github.com/odysseus-dev/odysseus/blob/bdbe69946f66305a8b4d1577eeaf1f4e398f6660/LICENSE

## 2. Later AGPL relicensing on the same upstream `dev` history

- **Subsequent upstream commit SHA:** `52ae2004220c3b67f9e98507647c0351db71f950`
- **Its direct parent SHA:** `bdbe69946f66305a8b4d1577eeaf1f4e398f6660`
- **Subsequent commit timestamp:** 9 June 2026, 21:20:34 UTC (10 June 2026, 09:20:34 Fiji time).
- **Observed changes:** The commit changed the original `LICENSE` from MIT to `AGPL-3.0-or-later`, updated the `README.md` license statement, and made a separate change to `static/js/cookbookServe.js`.

Primary evidence:

- Exact commit and its parent: https://github.com/odysseus-dev/odysseus/commit/52ae2004220c3b67f9e98507647c0351db71f950
- License after the change: https://github.com/odysseus-dev/odysseus/blob/52ae2004220c3b67f9e98507647c0351db71f950/LICENSE

This record concerns the `dev` branch specifically. The upstream `main` branch had a separate, earlier MIT-to-AGPL change; no claim is made that the above `dev` commit was the first AGPL change anywhere in the project.

## 3. Independently preserved copy in AonzOG/Odysseus-Last-MIT-Dev-Snapshot

- **Preservation repository:** https://github.com/AonzOG/Odysseus-Last-MIT-Dev-Snapshot
- **Preservation commit SHA:** `be93308bce9c1c67665754b7640bb9b123dbca8e`
- **Preservation commit Git tree SHA:** `4701eedf3af9c2a434375ad4c3e8f0c75ad7d097`
- **Preserved MIT `LICENSE` blob SHA:** `7087e2d598700ecb40f09a0fbf3f12952fcf641e`
- **Tracked source files:** 1,022, including original source code, tests, `LICENSE`, `ACKNOWLEDGMENTS.md`, and GitHub workflow files.

**Verification result:** The full Git tree of the preservation commit is *identical* to the full Git tree of the original MIT-licensed upstream `dev` commit. This matches every tracked file and its Git mode and content, not just the licensing file. The preserved commit does **not** reproduce the changes introduced by the later AGPL-transition commit.

- Preserved GitHub commit: https://github.com/AonzOG/Odysseus-Last-MIT-Dev-Snapshot/commit/be93308bce9c1c67665754b7640bb9b123dbca8e
- Preserved original license: https://github.com/AonzOG/Odysseus-Last-MIT-Dev-Snapshot/blob/be93308bce9c1c67665754b7640bb9b123dbca8e/LICENSE

## 4. Independent Git verification

These commands check the fixed historical commits, rather than a `main` branch that may acquire documentation or later development changes:

```bash
git clone https://github.com/AonzOG/Odysseus-Last-MIT-Dev-Snapshot.git
cd Odysseus-Last-MIT-Dev-Snapshot
git rev-parse be93308bce9c1c67665754b7640bb9b123dbca8e^{tree}
git show be93308bce9c1c67665754b7640bb9b123dbca8e:LICENSE
git remote add historical https://github.com/odysseus-dev/odysseus.git
git fetch historical dev
git rev-parse bdbe69946f66305a8b4d1577eeaf1f4e398f6660^{tree}
git rev-parse 52ae2004220c3b67f9e98507647c0351db71f950^
git show bdbe69946f66305a8b4d1577eeaf1f4e398f6660:LICENSE
```

Both tree-SHA commands should return `4701eedf3af9c2a434375ad4c3e8f0c75ad7d097`. The subsequent-commit parent command should return `bdbe69946f66305a8b4d1577eeaf1f4e398f6660`. Both displayed historical and preserved licenses should begin with `MIT License`.

## 5. Scope and licensing notice

This repository preserves a historical revision that the original upstream made available with an MIT license; it is not a claim to relicense subsequent AGPL-licensed upstream revisions. Preserve original copyright, MIT license and acknowledgement notices, and honor any applicable licenses for bundled third-party material. Nothing here claims affiliation with or endorsement by upstream maintainers.

This is a technical record of observable source-control history and matching file contents, **not** a legal judgment or a guarantee against an intellectual-property dispute. Uploading this document creates a later Git commit and changes the resulting `main` tree SHA; the fixed preservation commit `be93308bce9c1c67665754b7640bb9b123dbca8e` remains the proper byte-for-byte historical comparison.
