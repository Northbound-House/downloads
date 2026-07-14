# Northbound House — Downloads

Public hosting for release binaries of [Northbound House](https://northboundhouse.com)
apps. This repository contains **no source code** — application source lives in
private repositories. Only signed, notarized release artifacts are published here,
as GitHub Release assets.

## Products

### CamPass — pass the camera between your Macs

- **Download:** [`CamPass.dmg`](https://github.com/Northbound-House/downloads/releases/download/campass/CamPass.dmg)
- **Site:** https://campass.northboundhouse.com

## How releases are organized

Each product has a **rolling release** under a stable tag (e.g. `campass`) whose
asset filename never changes — so the download URL stays permanent across versions:

```
https://github.com/Northbound-House/downloads/releases/download/<product-tag>/<Asset>.dmg
```

To ship a new version, replace the asset on that product's release with the new
(same-named) build. Per-version history, if needed, is kept as additional
versioned releases (e.g. `campass-v1.2.0`).
