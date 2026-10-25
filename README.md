# Waibu

**Waibu watches your AI coding agent, stops it wasting your usage, and lets you steer it from one bar at the top of your screen.**

A small Windows app that sits next to [Claude Code](https://claude.com/claude-code).

## The control bar

One bar at the top of your screen shows what Claude is doing, and every notification lands there instead of piling up:

- **Live status.** "Running the tests · my-shop · 7 steps", in plain English.
- **Needs your OK.** Before Claude deletes files, force-pushes or does anything else you choose, the bar turns yellow with **Allow** and **Block** right in it (or press Alt+A / Alt+B).
- **Loop coach.** When Claude repeats the same failing step, Waibu gives it a tip, then stops the loop before it burns your usage.
- **Done** and **limit reset** notices.

Click the arrow and a panel drops down. Drag it anywhere.

- **Tell Claude something.** Your message reaches Claude right after its current step, even while it's working in your terminal.
- **Look at my screen.** Waibu takes a screenshot and hands it to Claude with its next step.
- **What are you doing?**, **Explain the last error**, **Pause after this step**, and **Stop**.
- **Your session and weekly limits**, with reset times, and a notice when your session limit resets (Pro and Max plans).

## Also in the Waibu window

- **Tasks** and **History**: everything Claude did, its answers and the files it changed.
- **Approvals**: choose what Waibu asks you about, and add your own rules.
- **Token saver**: how many tokens Waibu saved you, with a 7-day chart.
- **Give Claude tasks** from Waibu, and stop them any time.

Everything stays on your PC. Waibu has no account and sends nothing anywhere.

## Download

**[Download Waibu for Windows](https://github.com/prajithprajith369-arch/waibu/releases/latest)** (Waibu-Setup-0.2.0.exe, about 115 MB)

Needs Windows 10 or 11 (64-bit) and Claude Code installed.

## Install

1. Run **Waibu-Setup-0.2.0.exe**. No admin rights needed.
2. Windows may show **"Windows protected your PC"**, because the installer isn't code-signed yet. Click **More info**, then **Run anyway**.
3. Waibu opens. Click **Connect Claude Code** on the welcome screen.
   This adds Waibu to Claude Code's settings for every project, plus Claude Code's status line (that's how Waibu reads your limits). Your existing settings are kept, a status line of your own is never replaced, and a backup is saved as `settings.json.waibu-backup`.
4. Start a new Claude Code session. It shows up in Waibu.

If Waibu isn't running, Claude Code works exactly as before.

### Updating from 0.1.0

1. Quit Waibu from its tray icon (right-click > **Quit Waibu**).
2. Run **Waibu-Setup-0.2.0.exe**. Your settings and history are kept.
3. In Waibu, open **Settings**, click **Disconnect** next to Claude Code, then **Connect everywhere**. This adds the status line so Waibu can show your limits.

## Optional: let Claude ask to see your screen

**Look at my screen** in the control bar works out of the box. If you also want Claude to be able to *ask* for a screenshot itself, turn on **Let Claude ask to see my screen** in Settings. It's off by default because it adds about 130 tokens to every Claude message while installed. You approve every screenshot either way.

## Shortcuts

| | |
|---|---|
| Show or hide the Waibu window | Ctrl + Shift + Space |
| Allow (when asked) | Alt + A |
| Block (when asked) | Alt + B |
| Close the control panel | Esc |

## Uninstall

1. In Waibu, open **Settings** and click **Disconnect** next to Claude Code.
2. Uninstall Waibu from Windows **Settings > Apps**.

Your Waibu history is kept in `%APPDATA%\Waibu`; delete that folder to remove it too.
