# WipEout development log

## 2026-09-03 — canonical Track 01 identity

The release audit found a merged 12-track BIN identity in the prepared source.
A read-only prefix hash of the owned merged BIN produced the exact canonical
Track 01 size, MD5, SHA-1, and CRC32. The SHA-1 matched the earlier portfolio
audit.

The source now keeps the merged identity as a compatibility entry and adds the
canonical Track 01 identity. `disc_probe.json` and `catalog_identity.json` now
name `WipEout (Europe).cue` and `WipEout (Europe) (Track 01).bin`. No retail
data was copied.

Consulted leads:

- `_runs/knowledge/reviews/2026-09-02-public-disc-identity-audit.md`
- `https://openretro.org/game/2130eab4-cb07-4ba2-af2e-c485b516671f/edit`

The web source was used only to confirm canonical filenames. The owned
read-only hashes remain the identity evidence. No package or publication gate
has passed yet.
