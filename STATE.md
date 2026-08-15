# STATE — where downloads actually is

Last updated: 2026-08-12.

---

## In one paragraph

Public hosting for release binaries of Northbound House apps. No source code —
application source lives in private repositories. Today it carries exactly one
product, CamPass, and it does not entirely follow its own stated policy.

---

## The rolling-release scheme

Each product gets a **rolling release** under a stable tag (for example
`campass`) whose asset filename never changes, so the download URL stays
permanent across versions. That is the good idea this repository exists to
implement: the marketing site can hard-code one link and never update it.

---

## The repository contradicts its own policy

`README.md` states that **"only signed, notarized release artifacts are
published here, as GitHub Release assets."**

`CamPass.dmg` — 1.7 MB — is also committed directly into the repository, at the
root, tracked in git.

So there are two copies of the installer: the Release asset the documented
download URL points at, and a tracked file in `main` that nothing points at.
They are not linked. Publishing a new version updates the Release; the committed
copy stays at whatever version it was when it was added, and git history keeps
every version ever committed.

The two copies had already drifted, which is what settled it. The committed
file was 1,683,559 bytes, added on 2026-07-13; the Release asset is 1,911,535
bytes, published 2026-07-14 — a newer build. Nobody was served the stale one,
because the documented download link points at the Release, but the repository
was carrying an outdated installer that a reader could easily have taken for
the current one.

The committed copy has been removed. The Release remains the single source, as
the README always said it should be.
