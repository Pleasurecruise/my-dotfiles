# my-dotfiles

Chezmoi-managed dotfiles for macOS, Linux, and Windows.

## Quick start

1) Install chezmoi

- macOS: brew install chezmoi
- Linux: sh -c "$(curl -fsLS get.chezmoi.io)" -- -b /usr/local/bin
- Windows (PowerShell): winget install chezmoi

2) Initialize from this repo

```sh
chezmoi init --apply <repo-url>
```

3) Edit and apply

```sh
chezmoi edit ~/.bashrc
chezmoi apply
```

## Structure

- `dot_bashrc` -> `~/.bashrc`
- `dot_zshrc` -> `~/.zshrc`
- `dot_zprofile` -> `~/.zprofile`
- `dot_config/chezmoi/chezmoi.toml` -> Chezmoi config

## Platform notes

- macOS: uses Homebrew paths and optional mirrors
- Windows: keeps PATH changes minimal; favors user-level env

## Environment policy

- macOS: prefer Homebrew; only use official install scripts when upstream recommends them (e.g., nvm, rustup)
- macOS: use Homebrew-managed version managers where available (pyenv, jenv, goenv, rbenv)
- Linux: install version managers via apt or official scripts as appropriate