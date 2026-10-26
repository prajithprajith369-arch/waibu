# Waibu

**Waibu watches your AI coding agent, tells you what it's doing in plain English, stops it wasting your usage, and lets you steer it from a little dot on your screen.**

A small Windows app that sits next to [Claude Code](https://claude.com/claude-code).

## The dot

Waibu waits as a small round logo you can drag anywhere. Its pixel hand acts out what Claude is doing: it **walks on its rock fingers** while Claude works, **waves** when Claude needs your OK, gives a **thumbs up** when it's done, and **dozes** when all is quiet. Click the dot to open the bar.

## The story, in plain English

No logs to read. Waibu tells you what's going on:

> **Fixing the login button.** Claude changed login.js and auth.js. 1 test failed, so it's trying another fix.

You also see how far along it is: looked around, made changes, checking its work (2nd try). Waibu works this out on your PC from Claude's own steps, so it costs **0 tokens**. When Claude finishes, its answer shows up right in the pop-up.

## Speak your prompt

Tap the mic in the panel, or press **Alt + M** anywhere, and just talk. Your words land in the message box so you can check them before sending.

Waibu uses open-source voice models that run on your PC. Pick one the first time, or in **Settings › Voice**:

| Model | Download | Speed for a short sentence |
|---|---|---|
| Moonshine base (recommended) | 63 MB | about half a second · English only |
| Moonshine tiny | 28 MB | even faster · English only |
| Whisper base | 77 MB | a few seconds · other languages |
| Whisper small | 249 MB | 10 seconds or more · other languages, most accurate |

Each model downloads once from Hugging Face. After that your voice never leaves your PC, and Claude only gets the words you send.

## The control bar

The bar grows out of the dot when Claude needs you or has news, and every notification lands there instead of piling up:

- **Live status.** "Fixing the login button · Checking its work · 2nd try".
- **Needs your OK.** Before Claude deletes files, force-pushes or does anything else you choose, the bar turns yellow with **Allow** and **Block** right in it (or press Alt+A / Alt+B).
- **Loop coach.** When Claude repeats the same failing step, Waibu gives it a tip, then stops the loop before it burns your usage.
- **Done** and **limit reset** notices.

Click the arrow and a panel drops down. Drag it anywhere, and resize it from its bottom-right corner. Don't want the bar? Turn it off with the power button in the panel, and back on from the tray icon or Settings. Click the hand in the bar to shrink back to the dot.

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

**[Download Waibu for Windows](https://github.com/prajithprajith369-arch/waibu/releases/latest)** (Waibu-Setup-0.4.1.exe, about 120 MB)

Needs Windows 10 or 11 (64-bit) and Claude Code installed.

## Install

1. Run **Waibu-Setup-0.4.1.exe**. No admin rights needed.
2. Windows may show **"Windows protected your PC"**, because the installer isn't code-signed yet. Click **More info**, then **Run anyway**.
3. Waibu opens. Click **Connect Claude Code** on the welcome screen.
   This adds Waibu to Claude Code's settings for every project, plus Claude Code's status line (that's how Waibu reads your limits). Your existing settings are kept, a status line of your own is never replaced, and a backup is saved as `settings.json.waibu-backup`.
4. Start a new Claude Code session. It shows up in Waibu.

If Waibu isn't running, Claude Code works exactly as before.

### Updating

1. Quit Waibu from its tray icon (right-click > **Quit Waibu**).
2. Run **Waibu-Setup-0.4.1.exe**. Your settings and history are kept.
3. Coming from 0.1.0 only: in Waibu, open **Settings**, click **Disconnect** next to Claude Code, then **Connect everywhere**. This adds the status line so Waibu can show your limits.

## Optional: let Claude ask to see your screen

**Look at my screen** in the control bar works out of the box. If you also want Claude to be able to *ask* for a screenshot itself, turn on **Let Claude ask to see my screen** in Settings. It's off by default because it adds about 130 tokens to every Claude message while installed. You approve every screenshot either way.

## Shortcuts

| | |
|---|---|
| Show or hide the Waibu window | Ctrl + Shift + Space |
| Allow (when asked) | Alt + A |
| Block (when asked) | Alt + B |
| Speak to Claude | Alt + M |
| Close the control panel | Esc |

## Uninstall

1. In Waibu, open **Settings** and click **Disconnect** next to Claude Code.
2. Uninstall Waibu from Windows **Settings > Apps**.

Your Waibu history is kept in `%APPDATA%\Waibu`; delete that folder to remove it too.
