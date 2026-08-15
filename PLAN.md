# PLAN — what's next for downloads

Read `STATE.md` first.

---

## 1. Done — the committed binary is gone

`CamPass.dmg` existed both as a Release asset and as a tracked file, and the two
had drifted: the committed copy was an older, smaller build than the Release.
It has been removed, so the repository now matches the policy the README states.

Note that removing it from `main` does not remove it from history — the 1.6 MB
stays in every clone. That is tolerable once, and it is the reason to have
stopped now rather than after several more products were added the same way.

---

## 2. Add products to the Release scheme, not to the tree

When the next app ships, give it its own stable tag and rolling asset. The
scheme works; the failure mode is someone uploading a file to the repository
because that is the more obvious action.

---

## Deliberately not doing

**No source, ever.** This repository is public and the applications are
private. The separation is the point, and it is worth restating whenever
something is added here.
