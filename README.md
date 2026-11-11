# Agent Arcade — public beta

<img src=".github/app-icon.png" width="128" alt="Agent Arcade: a ruby-and-gold slot machine with three lightning bolts">

Native Mac slot-machine widgets that celebrate your AI agents' work. Each session gets a movable, resizable machine with spinning reels, milestone celebrations, and gloriously excessive artwork.

**[Download v0.1.0-beta.1 for macOS](https://github.com/rcox-shome/agent-arcade-releases/releases/tag/v0.1.0-beta.1)**

This repository hosts public downloads, release notes, and bug reports. The source repository is private.

## Install

Requires **macOS 13 or later**, on **Apple Silicon or Intel**. Python, fonts, and all artwork are bundled. No API key or developer tools are needed.

1. Download **Agent-Arcade-v0.1.0-beta.1-macOS-universal.zip** from the release page and unzip it.
2. Open **Install Agent Arcade.command** inside **Agent Arcade Beta**.
3. Open a new terminal and run `claude` or `codex` normally.

To try the app without terminal integration, open the included **Agent Arcade.app** directly. The installer copies the app to `~/Applications/Agent Arcade`, backs up an existing installation, and adds a removable block to `~/.zshrc`.

**This beta is ad-hoc signed and is not notarized by Apple.** macOS may block the downloaded app or installer. Review the macOS security prompt and open it only if you trust the project. Do not disable Gatekeeper.

## What it does

- Shows one independently movable, resizable, optionally always-on-top slot machine per session.
- Observes local Claude Code and Codex activity. Other providers can use the event API.
- Celebrates assistant updates while reels keep spinning; settles the reels when a turn finishes.
- Includes twelve illustrated covers, optional arcade audio, and a control room.

Use `arcade off` to hide the machines, `arcade on` to restore them, and `arcade status` to inspect the local connection. Demo outcomes are simulated; XP has no monetary value.

## Beta notes and privacy

Local transcript observation is best effort and may change with agent CLI versions. Other providers need an adapter for turn-level activity. Live XP and recent event history reset when the bridge restarts.

The bridge listens on `127.0.0.1:4242`. It reads local session records and shares short task titles, model/provider information, and activity metadata with the local widget. It does not forward full transcripts, code, tool arguments, or tool output. Personal session data and credentials are not included in the download.

Each release includes **SHA256SUMS.txt**. Put it beside the downloaded ZIP and run `shasum -a 256 -c SHA256SUMS.txt` to check download integrity.

## Feedback

[Report a bug](https://github.com/rcox-shome/agent-arcade-releases/issues) with your macOS version, Mac architecture, agent CLI/version, and reproduction steps. Remove private prompts, credentials, and personal paths from screenshots or logs before posting.
