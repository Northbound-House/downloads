# PLAN — what's next for downloads

Read `STATE.md` first.

---

## 1. Decide which copy of the binary is real

`CamPass.dmg` exists both as a Release asset and as a tracked file in `main`,
and the README says only the former should exist.

Almost certainly: **remove the committed copy** and keep the Release asset, so
the repository matches the policy it states. The download URL already points at
the Release, so nothing breaks.

Note that removing it from `main` does not remove it from history — the 1.7 MB
stays in every clone. That is tolerable once. It is the reason to stop now
rather than after several products have been added the same way.

The alternative is to change the README to describe what actually happens. That
is worse: committing binaries to git has no upside here, and the Release
mechanism already gives permanent URLs.

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
