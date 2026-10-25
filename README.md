# Waibu

**Waibu watches your AI coding agent, stops it wasting your usage, and explains what it's doing in plain English.**

A small Windows app that sits next to [Claude Code](https://claude.com/claude-code):

- **Live view.** See what Claude is doing right now ("Running the tests", "Changing login.js") instead of reading terminal logs.
- **Loop coach.** When Claude repeats the same failing step, Waibu gives it a tip, then stops the loop before it burns your usage.
- **Needs your OK.** Before Claude deletes files, force-pushes or does anything else you choose, a pop-up asks you to Allow or Block.
- **Give Claude tasks** from the Waibu window, and stop them any time.
- **Tasks, History and Token saver.** Everything Claude did, and how many tokens Waibu saved you.

Everything stays on your PC. Waibu has no account and sends nothing anywhere.

## Download

**[Download Waibu for Windows](https://github.com/prajithprajith369-arch/waibu/releases/latest)** (Waibu-Setup-0.1.0.exe, about 115 MB)

Needs Windows 10 or 11 (64-bit) and Claude Code installed.

## Install

1. Run **Waibu-Setup-0.1.0.exe**. No admin rights needed.
2. Windows may show **"Windows protected your PC"**, because the installer isn't code-signed yet. Click **More info**, then **Run anyway**.
3. Waibu opens. Click **Connect Claude Code** on the welcome screen.
   This adds Waibu to Claude Code's settings for every project. Your existing settings are kept, and a backup is saved as `settings.json.waibu-backup`.
4. Start a new Claude Code session. It shows up in Waibu.

If Waibu isn't running, Claude Code works exactly as before.

## Shortcuts

| | |
|---|---|
| Show or hide Waibu | Ctrl + Shift + Space |
| Allow (when asked) | Alt + A |
| Block (when asked) | Alt + B |

## Uninstall

1. In Waibu, open **Settings** and click **Disconnect** next to Claude Code.
2. Uninstall Waibu from Windows **Settings > Apps**.

Your Waibu history is kept in `%APPDATA%\Waibu`; delete that folder to remove it too.
