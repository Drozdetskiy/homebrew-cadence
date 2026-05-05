# homebrew-cadence

Homebrew tap for [cadence](https://github.com/Drozdetskiy/cadence) — an autonomous task-execution pipeline on top of [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

## Install

```bash
brew tap drozdetskiy/cadence
brew install drozdetskiy/cadence/cadence  # tap-qualified name avoids the homebrew-core `cadence` (Flow smart-contract language) clash
```

`cadence` requires [Claude Code](https://docs.anthropic.com/en/docs/claude-code) on `PATH` and a git repository. See the [project README](https://github.com/Drozdetskiy/cadence#readme) for usage.