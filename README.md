# Scoop bucket for Patchloom

[Scoop](https://scoop.sh/) bucket for [patchloom](https://github.com/patchloom/patchloom),
a structured file-editing CLI for AI agents.

## Install

```powershell
scoop bucket add patchloom https://github.com/patchloom/scoop-bucket
scoop install patchloom/patchloom
```

## Update

```powershell
scoop update patchloom
```

The manifest uses Scoop `checkver` / `autoupdate` against GitHub Releases
(tags `patchloom-vX.Y.Z`). No manual version bumps are required after a
new release is published.

## Verify

```powershell
patchloom --version
```
