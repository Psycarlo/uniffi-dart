---
name: Release
about: Checklist for releasing a new version of uniffi-dart
title: "Release vX.Y.Z+vA.B.C"
labels: release
assignees: ''
---

## Release checklist

Replace `X.Y.Z` with the uniffi-dart version and `A.B.C` with the
targeted uniffi-rs version throughout.

### Version bump

- [ ] Determine version: bump **minor** for breaking changes, **patch**
      otherwise
- [ ] Update `version` in `Cargo.toml` (e.g. `0.X.Y+v0.A.B`)

### Documentation

- [ ] Update installation instructions in `README.md`
- [ ] If the upstream uniffi-rs version changed, add a row to the
      versioning table in `README.md`
- [ ] Update `CHANGELOG.md` — prefix breaking changes with
      `**BREAKING**:` and critical fixes with `**IMPORTANT**:`

### Review & merge

- [ ] Open a PR with the above changes
- [ ] Get approval and merge to `main`

### Tag & release

- [ ] Create a git tag on `main`: `vX.Y.Z+vA.B.C`
- [ ] Create a GitHub Release from the tag with the changelog entry
