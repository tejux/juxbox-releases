# Juxbox

Juxbox is a local-first developer utility workbench for macOS. It puts everyday encoding, formatting, identity, security, and math tools in one fast desktop app, with composable workflows for sending output from one tool into another.

Your input and output stay on your device while you work. No account or cloud service is required.

![Juxbox overview](assets/juxbox-overview.png)

## Install

### Homebrew Cask

The recommended installation method is Homebrew:

```bash
brew tap tejux/tap
brew install --cask juxbox
```

To upgrade an existing installation:

```bash
brew update
brew upgrade --cask juxbox
```

### Download the DMG

You can also install Juxbox directly from the [latest release](https://github.com/tejux/juxbox-releases/releases/latest):

1. Download `Juxbox-<version>.dmg` and its matching `.sha256` file.
2. Optionally verify the download:

   ```bash
   shasum -a 256 Juxbox-<version>.dmg
   cat Juxbox-<version>.dmg.sha256
   ```

   The two SHA-256 values should match.

3. Open the DMG and drag `Juxbox.app` to your Applications folder.

Juxbox releases are universal macOS builds for Apple Silicon and Intel Macs. macOS 12 or later is required.

## What is included

### Encoders

- Base64 encode and decode
- URL encode and decode

### Formats

- JSON beautify
- JSON minify

### Identity

- JWT decode
- JWT signature verification for RS* and HS* tokens

### Security

- X.509 certificate inspection
- RSA, ECDSA, and Ed25519 private-key inspection
- SSH private-key, public-key, and signed-public-key inspection

### Math

- Arbitrary-precision calculator with `+`, `-`, `*`, `/`, `%`, `^`, and grouping with parentheses, brackets, or braces
- Number-base conversion with `0b` binary, `0n` octal, and `0x` hexadecimal prefixes, plus binary auto-detection

## Workflows

Use **Send output to…** to pass the entire output of one tool into another. If you select a portion of the output first, only that selection is sent.

Tool visibility can be customized from **Tools → Pick Tools**. The selection is saved across restarts, and **Tools → Show All Tools** restores the default view.

## Uninstall

If installed with Homebrew:

```bash
brew uninstall --cask juxbox
```

To also remove Juxbox's saved preferences and application data:

```bash
rm -rf "$HOME/Library/Application Support/Juxbox"
rm -rf "$HOME/Library/Caches/Juxbox"
defaults delete com.juxbox.app 2>/dev/null || true
```

## Releases

Each version is published as a Git tag and includes:

- A universal macOS DMG
- A SHA-256 checksum file
- Release notes

See the [release history](https://github.com/tejux/juxbox-releases/releases) for downloads and changelogs.

## License and source

This repository contains Juxbox's public release artifacts. The application is distributed through the [Juxbox Homebrew tap](https://github.com/tejux/homebrew-tap).
