# homebrew-cadence

Homebrew tap for [cadence](https://github.com/Drozdetskiy/cadence). The tap exposes the CLI as `cadence` and installs `cadence-runner` from PyPI into a Python virtualenv with all dependencies pinned via `resource` blocks.

## Repo layout

- `Formula/cadence.rb` — the Homebrew formula (URL, sha256, license, Python dep, resource blocks, `install`/`test`).
- `README.md` — install instructions for end users.

## Commits

English. Subject line follows one of these forms:

- **Release bump**: `Release: cadence X.Y.Z` — for routine version bumps that update only `url`, `sha256`, and (when deps changed) the `resource` blocks.
- **Other changes**: `<imperative summary>` — short, imperative, sentence-case (e.g. `Update README install command to tap-qualified form`, `Fix sha256 mismatch on PyYAML resource`).

Keep the subject under ~70 chars so GitHub renders it cleanly. Add a body only when there is non-obvious context worth preserving (e.g. what was verified locally, why a resource was pinned to a specific version). One short clause per body line.

Author as the user — no `Co-Authored-By` trailer. Never commit directly during a release without first verifying locally:

```bash
brew audit --strict drozdetskiy/cadence/cadence
brew install --build-from-source drozdetskiy/cadence/cadence
brew test drozdetskiy/cadence/cadence
```

## Install command

The canonical install is **tap-qualified**: `brew install drozdetskiy/cadence/cadence`. The unqualified `brew install cadence` resolves to the homebrew-core formula (Flow smart-contract language), so the README and any docs that mention the install command must use the tap-qualified form.
