# Teraflock Homebrew Tap

```sh
brew install teraflock/tap/tera
```

Installs `flockd` (the node daemon) and `tera` (CLI/TUI). Formulae are
published automatically by goreleaser from teraflock/flockd releases.

> **No formula is published right now.** The CLI was renamed `flock` → `tera`
> (the old name collided with util-linux's `flock(1)`), and the previous
> `flock.rb` was removed because it installed the colliding binary. Goreleaser
> writes `tera.rb` here on the next release tag; until then, install with
> `curl -fsSL https://teraflock.ai/install.sh | sh`.
