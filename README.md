# Makabhosda Aag Sound on Terminal Error 🔊

A VS Code extension that plays a "makabhosda aag" sound whenever an error appears in your terminal. Perfect for catching errors when you're multitasking!

## Features

- 🎵 Automatically plays a sound when terminal errors are detected
- ⚙️ Configurable error patterns to match
- 🔊 Adjustable volume control
- 🎮 Easy toggle on/off
- 🧪 Test sound command to verify it's working

## Installation

1. Open VS Code
2. Press `Ctrl+P` to open Quick Open
3. Paste the following command and press Enter:
   ```
   ext install Zubair.makabhosda-aag-sound-error
   ```
4. Done! The extension will activate automatically.

## Commands

- **Makabhosda Aag Sound: Toggle Error Sound** - Enable/disable the sound
- **Makabhosda Aag Sound: Test Sound** - Play the sound to test it's working

Access commands via Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`)

## Configuration

Open VS Code settings and search for "Makabhosda Aag Sound" to configure:

### `makabhosdaAagSoundError.enabled`
- **Type:** `boolean`
- **Default:** `true`
- **Description:** Enable/disable the makabhosda aag sound on terminal errors

### `makabhosdaAagSoundError.volume`
- **Type:** `number`
- **Default:** `0.5`
- **Range:** `0.0` to `1.0`
- **Description:** Volume level for the makabhosda aag sound

### `makabhosdaAagSoundError.errorPatterns`
- **Type:** `array`
- **Default:**
  ```json
  [
    "error:",
    "Error:",
    "ERROR:",
    "fail:",
    "FAIL:",
    "Failed",
    "fatal:",
    "FATAL:",
    "Exception",
    "Traceback",
    "command not found",
    "No such file"
  ]
  ```
- **Description:** Patterns to detect errors in terminal output

## How It Works

The extension monitors your VS Code terminal using the `onDidEndTerminalShellExecution` API (available in VS Code 1.93+). When a command exits with a non-zero exit code, the extension plays the makabhosda aag sound to alert you.

## Requirements

- VS Code 1.93 or higher
- One of the following audio players (for Linux):
  - `ffplay` (from FFmpeg)
  - `paplay` (PulseAudio)
  - `aplay` (ALSA)
- macOS and Windows have built-in audio support

## License

MIT
