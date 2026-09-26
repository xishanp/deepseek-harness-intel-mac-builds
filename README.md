# DeepSeek Harness — Unofficial Intel macOS x64 Builds

This repository hosts **unofficial, self-built Intel (x86_64) macOS binaries** of
[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness).

> **Not affiliated with DeepSeek.** These builds are compiled locally by an
> individual from the official open-source repository. They are **not** official
> DeepSeek-distributed binaries, and they are **not** official DeepSeek DMGs.

## Why this repository exists

Upstream release artifacts are primarily aimed at Apple Silicon. Intel Mac users
can build the desktop app from source themselves — this repository simply
publishes the result so other Intel Mac users do not have to reproduce the
toolchain.

## Releases

See the [Releases](../../releases) page. Each release includes:

- `DeepSeek-Harness-<version>-mac-x64-unsigned.zip` — the `.app` bundle
- a matching `.sha256` checksum file
- release notes with full build provenance

## Build characteristics

| | |
|---|---|
| Platform | macOS x64 / Intel (`darwin-x64`) |
| Build method | Official source, locally self-compiled |
| Signing | **Unsigned**, no Apple Developer signature |
| Notarization | **Not notarized** by Apple |
| Packaging | `.app` bundle in `.zip` (no source code included) |

Because these builds are unsigned and unnotarized, macOS Gatekeeper blocks them on
first launch. See the release notes for how to allow the app manually.

## Verifying a download

```bash
shasum -a 256 DeepSeek-Harness-*.zip
```

Compare the output against the `.sha256` file published with the release.

## What is NOT included

No API keys, tokens, `.env` files, personal configuration, caches, or logs are
ever included in these packages. You provide your own credentials at runtime.

## License

DeepSeek Harness is licensed under the **MIT License**, © 2026 DeepSeek.
Builds published here are redistributed under the same license; see [LICENSE](LICENSE).

Upstream project: <https://github.com/deepseek-ai/deepseek-harness>
