# Scoop bucket for Patchloom

[Scoop](https://scoop.sh/) bucket for [patchloom](https://github.com/patchloom/patchloom).

## Install

```powershell
scoop bucket add patchloom https://github.com/patchloom/scoop-bucket
scoop install patchloom/patchloom
```

## How versions are published

Each GitHub Release of patchloom runs the `publish-scoop-bucket` job in
[patchloom/patchloom](https://github.com/patchloom/patchloom) release CI.
That job rewrites `bucket/patchloom.json` with the new `version`, zip URLs
(`patchloom-vX.Y.Z` tags), and SHA256 hashes, then commits here.

So the **committed JSON is the source of truth** for `scoop install` /
`scoop update` after users pull the bucket (`scoop update` refreshes the
bucket git clone).

`checkver` / `autoupdate` fields remain in the manifest only as a fallback
if the bucket JSON lags; they are not the primary publish path.

## Update

```powershell
scoop update
scoop update patchloom
```

## Verify

```powershell
patchloom --version
```
