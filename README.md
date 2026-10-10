# Mac Input Guard

Keep your Mac’s built-in or USB microphone selected while using Bluetooth headphones or speakers.

[Українською](README.uk.md) · [Download the app](https://github.com/simplaerai-sv/mac-input-guard-app/releases/latest)

## Why this app exists

Mac Input Guard was created after one recurring annoyance: macOS kept switching the default input to the microphone on a Bluetooth headset or speaker. The microphone the user wanted — the built-in Mac microphone or an external USB microphone — had to be selected again by hand.

If the Bluetooth microphone does not give you the voice quality you want, this unexpected switch can affect calls, meetings, recordings, and speech recognition. Mac Input Guard keeps your preferred microphone selected, so you can continue listening through Bluetooth while speaking through the input you chose.

This app is for anyone tired of correcting that microphone selection over and over.

## Useful cases

- **Bluetooth headphones for listening, built-in mic for speaking.** Keep playback on your headphones while using your laptop microphone as the default input.
- **USB microphone or webcam at your desk.** Use it first; fall back to the built-in microphone when it is unplugged, and switch back when it returns.
- **Calls, meetings, recording, and dictation.** Keep the intended input selected instead of discovering later that an unwanted microphone was used.
- **Frequent Bluetooth reconnections.** Avoid reopening Sound settings just to restore your preferred microphone.

## Screenshot

![Mac Input Guard settings window in English](assets/mac-input-guard-en.jpg)

*The primary USB webcam is disconnected, so the built-in backup microphone is in use. Device names follow the macOS language; the app interface is English.*

## What it does

Choose a primary and a backup microphone. When the primary USB microphone is disconnected, the app selects the backup. When it returns, the app switches back. The built-in Mac microphone is the final fallback if both chosen devices are absent. Bluetooth microphones are excluded from the priority list.

The app has a normal settings window, a menu-bar shortcut, a visible current-input status, an automatic-selection switch, and optional startup at login. Closing the window leaves the app running; **Quit app** stops it.

It changes only the system default input. Apps that use their own explicit input selection may need their input set to **System default**. It does not record audio, change your speakers, or contact a server.

## Install

1. Download `Mac-Input-Guard-1.5.0-universal.zip` from [Releases](https://github.com/simplaerai-sv/mac-input-guard-app/releases/latest).
2. Unzip it and move **Mac Input Guard.app** to **Applications**.
3. Open the app, choose your primary/backup microphones, and leave automatic selection on.
4. Turn on **Start at login** if wanted. The app creates its own startup entry; no Terminal setup is needed.

Requires **macOS 13 or later**. The universal binary includes **Apple Silicon and Intel**. Functional testing was performed on Apple Silicon; execution on a physical Intel Mac has not yet been verified.

This release is ad-hoc signed and is **not Apple-notarized**. macOS may display a warning for an app downloaded outside the App Store. Review [Apple's instructions](https://support.apple.com/guide/mac-help/open-a-mac-app-from-an-unknown-developer-mh40616/mac) before deciding to open it. A SHA-256 checksum is provided with each release.

## Languages

English and Ukrainian are included. Choose **Interface language** in the app. To install a community translation, use **Add language from file…** and select its JSON file.

Use **Save translation template…** in the app to export a ready-to-edit JSON example with all strings and instructions. You can also download [the template](translations/template.json).

See [translation instructions](TRANSLATIONS.md) and [the English template](translations/en.json). Missing strings fall back to English. Imported translations are local text files, not executable plugins.

## About this repository

This public repository contains downloads, user documentation, and editable translations. Application source code is maintained in a private repository. Use [Issues](https://github.com/simplaerai-sv/mac-input-guard-app/issues) for problems and suggestions; do not attach passwords, device serial numbers, or private logs.
