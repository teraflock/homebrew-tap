# Teraflock Homebrew Tap

```sh
brew install teraflock/tap/tera
```

Installs `flockd` (the node daemon) and `tera` (CLI/TUI). Formulae are
published automatically by goreleaser from teraflock/flockd releases.

> **No formula is published right now.** The CLI was renamed `flock` → `tera`
> (the old name collided with util-linux's `flock(1)`). The last published
> formula, `flock.rb` for v0.1.3, was removed rather than edited: it installs
> a binary named `flock` from the v0.1.3 tarball, which is the collision being
> removed, so pointing it at `tera` would only produce a formula that fails.
>
> Goreleaser writes `tera.rb` here on the **next release tag** — that tag is
> what restores `brew install`. Until then:
> `curl -fsSL https://teraflock.ai/install.sh | sh`.
