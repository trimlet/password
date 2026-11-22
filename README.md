# Trimlet Password

A place to keep your passwords, in a small window driven only by the keyboard.

- A list of items (name, user, password), favourites, the history of a password, suggested
  strong passwords. Enter copies the password, `u` the user; passwords are hidden until revealed.
- The items are in one file encrypted with a master password (Argon2id + AES-256-GCM),
  `trimletpassword/vault.trimletpassword` in the app settings folder; the system keychain remembers
  the password, so it is typed only the first time and on a new computer.
- **Sync between your computers** (optional) through trimlet.dev, with an invite code: the server only
  keeps the encrypted vault and never sees the master password. Sync through a private GitHub
  repository is being set up.

## Build

Written in Go with [Fyne](https://fyne.io), for macOS and Windows. Ready-made downloads are not
published yet. To build it, with Go installed (and on a Mac the Xcode command line tools):

```
go run fyne.io/tools/cmd/fyne@v1.7.3 package --release
```

or `go run .` to try it. The console window comes from [trimlet/gui](https://github.com/trimlet/gui),
which `go` fetches by itself.

## How it is made

The code is written with Claude Opus (Anthropic), under the direction and review of a developer with
almost 30 years of experience. Every feature starts from a real, repeated need, and most ideas are
turned down: the goal is to stay small.

## License

GPL-3.0, see [LICENSE](LICENSE).
