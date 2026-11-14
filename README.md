<p align="center"><img src="icon.png" width="128" alt="Dicto icon"></p>

# Dicto

Dicto is a free dictation app for macOS. Press a shortcut in any app and speak. Dicto turns your speech into text on your Mac, cleans it up, formats it for the app you're typing in, and pastes it at your cursor.

This repository only hosts Dicto's downloads and release notes.

## Download

**[Download Dicto.dmg](https://github.com/vivekkhandelwal55/dicto-releases/releases/latest/download/Dicto.dmg)** (latest version) · [All releases](https://github.com/vivekkhandelwal55/dicto-releases/releases)

Requires macOS 14 or later on Apple Silicon (M1 or newer).

## Install

1. Open the DMG and drag **Dicto** into **Applications**.
2. The first time, right-click Dicto in Applications, choose **Open**, then click **Open** again. Dicto isn't notarized by Apple yet, so a normal double-click is blocked the first time. If macOS still refuses, run:
   ```sh
   xattr -dr com.apple.quarantine /Applications/Dicto.app
   ```
3. Allow **Microphone** and **Accessibility** access when asked. Accessibility lets Dicto paste text into the app you're using.
4. Download a speech model in the welcome screen.
5. For AI formatting, open **Settings → Smart Formatting** and paste your Ollama API key (ollama.com → Settings → API keys), or point it at a local Ollama.

To check a download, compare it with the `.sha256` file attached to each release: `shasum -a 256 Dicto.dmg`.

## Privacy

Speech recognition runs on your Mac; audio never leaves it. When AI formatting is on, only the transcribed text and the name of the app you're typing in are sent, to the model provider you configure.

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/vivekkhandelwal55/dicto-releases/issues).

## Credits

Dicto builds on [OpenSuperWhisper](https://github.com/Starmel/OpenSuperWhisper) and [whisper.cpp](https://github.com/ggerganov/whisper.cpp), among other open-source projects. Their licence notices are in **Settings → Acknowledgements** in the app and in `Acknowledgements.txt` in the DMG.
