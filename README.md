# elabz/homebrew-tap

Homebrew tap for [squawk](https://github.com/elabz/squawk) — voice-to-terminal
dictation for macOS: hold Space in iTerm to talk, and the transcript lands at
your cursor.

```sh
brew install elabz/tap/squawk
squawk install-agent
squawk setup
squawk doctor
```

The formula compiles squawk's `SquawkPTT` helper from source on your machine, so
no Apple notarization or Developer account is involved and the app is never
Gatekeeper-quarantined. `install-agent` then loads the push-to-talk LaunchAgent.

Run `squawk uninstall` before `brew uninstall` — Homebrew cannot unload a
launchd agent or clear privacy grants.

The formula's source of truth lives in the main repo at
[`packaging/homebrew/squawk.rb`](https://github.com/elabz/squawk/blob/main/packaging/homebrew/squawk.rb);
this tap holds a copy at `Formula/squawk.rb`.
