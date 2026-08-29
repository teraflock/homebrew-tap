# Teraflock Homebrew Tap

```sh
brew install teraflock/tap/tera
```

Installs `flockd` (the node daemon) and `tera` (CLI/TUI). Published
automatically by goreleaser from teraflock/flockd releases.

## macOS only

`tera` ships as a **cask**, not a formula — goreleaser deprecated formula
publishing, and Homebrew's guidance is that pre-built binaries belong in
casks. Homebrew on Linux cannot install casks, so on Linux use:

```sh
curl -fsSL https://teraflock.ai/install.sh | sh
```

or the `.deb` / `.rpm` attached to each
[release](https://github.com/teraflock/flockd/releases).

## Renamed from `flock`

The CLI was `flock` until 2026-08-28. It was renamed because `flock(1)` is a
util-linux binary present on every Linux distribution, and shipping a second
one into `PATH` shadows a tool that shell scripts depend on. The daemon keeps
its name.

`tap_migrations.json` maps the old formula to the new cask, so an existing
install follows the rename:

```sh
brew update && brew upgrade
```

The binaries are not yet notarized (beta). The cask strips the macOS
quarantine flag on install, so Gatekeeper will not report them as damaged.
