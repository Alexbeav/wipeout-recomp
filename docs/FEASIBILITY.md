# WipEout feasibility binding

## Identity

- Title and region: WipEout, Europe.
- Serial: SCES-00010.
- Source executable path: `disc/SCES_000.10`.
- Load address: `0x80010000`.
- Entry point: `0x80078420`.
- Source disc binding: `disc/WipEout (Europe).cue`.

The source `game.toml` confirms these values. This preparation did not read or
copy retail content.

## Current evidence

The clean source commit is `c1baf6732c5ea888b39cf68ba69e5f2a45683a7f`. It uses PSXRecomp
`eecf3b2a4ee3148f01f8f92b512930fd6307d82e` and recomp-ui `87bbf43c419c16b97bf433a84d600969159e2e84`. The source
contains 556 non-comment seed rows.

The current portfolio package records an automated build, audit, launcher
marker check, and startup smoke result. That receipt is build and startup
evidence only. It does not prove full-game correctness.

The current public topology is the aggregate Wave 1 `v0.2.3` kit. This title
does not have a public standalone repository.

## Refresh result

No refresh build ran. The exact next workbench source is not selected. Upstream
`master` is untagged and diverges from the accepted portfolio source. This
preparation does not change the runtime pin, UI pin, or title version.

## Track recommendation

Keep the recompilation track. The existing source and package receipts support
continued package work. They do not establish an enhanced or full-quality
state.

Widescreen, high-frame-rate simulation, and new input work are outside this
refresh. Review them only after the exact base passes the title gates.

## Smallest decisive next steps

1. Select one exact accepted PSXRecomp source.
2. Test the setup-marker fail-closed contract on that source.
3. Build this title in this isolated preparation branch.
4. Record exact Windows, Linux, and macOS package identities.
5. Ask Alex to test the exact packages.
6. Assign a release version only after the version gate passes.

## Evidence

- Source `game.toml`, `catalog_identity.json`, `VERSION`, and Git submodule
  entries at `c1baf6732c5ea888b39cf68ba69e5f2a45683a7f`.
- Portfolio `wipeout/BUILDINFO.json`.
- Portfolio `wipeout/RECEIPT.md`.
- Portfolio `_runs/knowledge/reviews/2026-09-01-upstream-refresh-audit.md`.
- Portfolio `_runs/knowledge/reviews/2026-09-01-release-waves-refresh-preparation.md`.

## 2026-09-03 refresh correction

The prepared source had only the merged 697,375,056-byte BIN identity. The
candidate now also accepts canonical Track 01: 64,988,112 bytes, MD5
`23c2abd60259c0ddb84a2c4e72278729`, SHA-1
`93a70ff5be6d8a4b25bf40ba453e6ded864ad645`, and CRC32 `7f6c5a6a`.
`disc_probe.json` and `catalog_identity.json` now name the canonical CUE and
Track 01. The merged identity remains as an explicit compatibility entry in
`game.toml`. This is a source correction. No new package has passed yet.

## 2026-09-03 three-platform candidate

The `v0.1.1` candidate uses public package-only framework child
`e081d29da2fa9862204f63e6b2004d76f1d0cb2d`. Its exact parent is the previously qualified Wave 1 source
`eecf3b2a4ee3148f01f8f92b512930fd6307d82e`. The child removes two non-SDK helpers with private paths
from setup packages. It does not change runtime, recompiler, BIOS, UI, or title
behavior.

The candidate targets Windows x64, Linux x64, macOS ARM64, and macOS x64. It
requires an owned regional retail BIOS and does not ship OpenBIOS. Build-only
CI, complete archive audit, native package tests, an exact release manifest,
and final R4 authorization remain required. No `v0.1.1` release exists.

## 2026-09-03 portable Linux package

The release workflow now builds Linux in a pinned Ubuntu 20.04 container.
The package gate rejects a setup host or emitter that needs a glibc version
newer than 2.31. This keeps the release compatible with the qualified Rocky
Linux 9 host. Windows and both macOS builds keep their existing runners.
