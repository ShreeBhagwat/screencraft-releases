# ScreenCraft releases

Public download artifacts for [ScreenCraft](https://screencraft.in) — the macOS source repo is private.

Each release attaches:

- `ScreenCraft-<version>.dmg` — Developer ID signed and notarized by Apple, universal binary, macOS 13+
- `ScreenCraft-<version>.dmg.sha256` — SHA-256 hash for download verification

## Download

Latest release: <https://github.com/ShreeBhagwat/screencraft-releases/releases/latest>

Or programmatically (used by the app's self-update check):

```sh
curl https://screencraft.in/api/latest
```

Response:

```json
{
  "version": "1.0.0",
  "tag": "v1.0.0",
  "url": "https://github.com/ShreeBhagwat/screencraft-releases/releases/download/v1.0.0/ScreenCraft-1.0.0.dmg",
  "sha256": "<hex>",
  "size": 7654321,
  "publishedAt": "...",
  "minMacOS": "13.0"
}
```

## Verify a download

```sh
shasum -a 256 ScreenCraft-1.0.0.dmg
# compare against ScreenCraft-1.0.0.dmg.sha256
```
