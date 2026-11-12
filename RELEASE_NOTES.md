# Agent Arcade v0.1.0-beta.1

The first beta of Agent Arcade: native Mac slot-machine widgets that celebrate your AI agents' progress.

## Download and install

Download **Agent-Arcade-v0.1.0-beta.1-macOS-universal.zip** from this release. It supports **macOS 13 or later on Apple Silicon and Intel Macs**. Python, fonts, and all artwork are included; no developer tools or API key are needed to run it.

1. Unzip the download.
2. Open **Install Agent Arcade.command** inside **Agent Arcade Beta**.
3. Open a new Terminal window and run `claude` or `codex` normally.

The installer copies the app to `~/Applications/Agent Arcade`, backs up an existing installation, and adds a removable startup block to `~/.zshrc`. Use `arcade off` to hide the machines, `arcade on` to restore them, and `arcade status` to check the connection. To try the app without shell integration, open the included **Agent Arcade.app** directly.

**This beta is ad-hoc signed and is not notarized by Apple.** macOS may block the downloaded app or installer. Review the macOS security prompt and open it only if you trust this project. Do not disable Gatekeeper.

## Included

- One movable, resizable, optionally always-on-top machine per agent session.
- Automatic local observation of Claude Code and Codex activity.
- Three-lightning-bolt celebrations for assistant updates; reels settle when the turn finishes.
- Twelve illustrated covers, the new ruby-and-gold app icon, optional audio, and a control room.
- Event API and CLI helpers for other agent providers.

## Beta limitations

- Local transcript observation is best effort and can change with provider CLI versions. Other providers require an adapter for turn-level activity.
- Automatic observation cannot show a CLI before its first prompt; the included shell helper can.
- Live XP and recent event history reset when the bridge restarts. Cover choices and the on/off setting persist locally.
- macOS only. XP has no monetary value.

## Privacy and feedback

The bridge listens on loopback (`127.0.0.1:4242`). It reads local session records and exposes short task titles, model/provider information, and activity metadata to the local widget. It does not forward full transcripts, code, tool arguments, or tool output. The download contains no personal session data or credentials.

Report bugs at https://github.com/rcox-shome/agent-arcade-releases/issues. Include your macOS version, Mac architecture, agent CLI/version, and reproduction steps. Remove private prompts, credentials, and personal paths from screenshots or logs before posting.

**SHA256SUMS.txt** is attached so you can check download integrity with `shasum -a 256 -c SHA256SUMS.txt` from the folder containing both release files.
