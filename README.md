# Installing from .vsix file (Manual)

If you downloaded the `.vsix` file from GitHub (e.g., `maakabhosraaag-terminal-error-1.1.3.vsix`):

1. Open VS Code
2. Go to Extensions (`Ctrl+Shift+X`)
3. Click the `...` menu (top right) → `Install from VSIX...`
4. Select the `.vsix` file you downloaded
5. The extension will install and activate automatically

You do **not** need to package or publish the extension yourself if you have the `.vsix` file.

# Maakabhosraaag Error on Terminal 🔊

A VS Code extension that plays a "maakabhosraaag" sound whenever an error appears in your terminal. Perfect for catching errors when you're multitasking!

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
  ext install Zubair.maakabhosraaag-terminal-error
  ```
4. Done! The extension will activate automatically.

## Commands

- **Maakabhosraaag: Toggle Error Sound** - Enable/disable the sound
- **Maakabhosraaag: Test Sound** - Play the sound to test it's working

Access commands via Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`)

## Configuration

Open VS Code settings and search for "Maakabhosraaag" to configure:

### `maakabhosraaagError.enabled`
- **Type:** `boolean`
- **Default:** `true`
- **Description:** Enable/disable the maakabhosraaag sound on terminal errors

### `maakabhosraaagError.volume`
- **Type:** `number`
- **Default:** `0.5`
- **Range:** `0.0` to `1.0`
- **Description:** Volume level for the maakabhosraaag sound

### `maakabhosraaagError.errorPatterns`
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
   "Traceback"
  ]
  ```
- **Description:** Patterns to detect errors in terminal output

## Audio Player Requirements

The extension uses system audio players to play sounds:

- **Linux:** Requires `paplay` (PulseAudio), `aplay` (ALSA), or `ffplay` (FFmpeg)
- **macOS:** Uses built-in `afplay` (✅ Works out of the box)
- **Windows:** Uses PowerShell's SoundPlayer (✅ Works out of the box with WAV format)

### Installing Audio Players (Linux)

If you don't have an audio player installed:

```bash
# For Ubuntu/Debian (PulseAudio)
sudo apt-get install pulseaudio-utils

# For ALSA
sudo apt-get install alsa-utils

# For FFmpeg
sudo apt-get install ffmpeg
```

## Packaging the Extension

To package and install the extension:

1. Install vsce (VS Code Extension Manager):
  ```bash
  npm install -g @vscode/vsce
  ```

2. Package the extension:
  ```bash
  vsce package
  ```

3. Install the `.vsix` file:
  - Open VS Code
  - Go to Extensions (`Ctrl+Shift+X`)
  - Click the "..." menu → "Install from VSIX"
  - Select the generated `.vsix` file

## Publishing (Optional)

To publish to the VS Code Marketplace:

1. Create a publisher account at https://marketplace.visualstudio.com/
2. Update `publisher` in `package.json`
3. Run:
  ```bash
  vsce publish
  ```

## How It Works

1. The extension monitors all terminal output using VS Code's `onDidWriteTerminalData` event
2. When terminal data is written, it checks against configured error patterns
3. If an error pattern is matched, it plays the sound file
4. The sound is played using system audio players (platform-specific)

## Troubleshooting

### Sound not playing?

1. **Check the sound file exists:** Make sure `sounds/makabhosda_aag.mp3` exists
2. **Test the sound:** Use the "Maakabhosraaag: Test Sound" command
3. **Check audio player:** Ensure you have a compatible audio player installed (see requirements)
4. **Check system volume:** Make sure your system volume is not muted
5. **Check extension logs:** Open Output panel → select "Maakabhosraaag Error"

### Too many false positives?

Adjust the `maakabhosraaagError.errorPatterns` setting to be more specific to your needs.

### Sound too loud/quiet?

Adjust the `maakabhosraaagError.volume` setting (0.0 to 1.0).

## Development

### Project Structure

```
Maakabhosraaag extension/
├── extension.js          # Main extension code
├── package.json          # Extension manifest
├── sounds/
│   ├── makabhosda_aag.mp3         # Your sound file
│   └── README.txt       # Instructions
└── README.md            # This file
```

### Testing

1. Open the extension folder in VS Code
2. Press `F5` to start debugging
3. Test in the Extension Development Host window

## License

MIT License - Feel free to use and modify!

## Contributing

Contributions are welcome! Feel free to:
- Add new features
- Improve error detection
- Add support for more audio formats
- Report bugs or issues

## Changelog

### 1.1.3
- **Updated:** New error sound effect

### 1.1.2
- **New:** Added extension icon/logo
- **Improved:** Visual branding for marketplace listing

### 1.1.1
- **Fixed:** Added `terminalDataWriteEvent` to API proposals to resolve activation error
- **Fixed:** Extension now properly declares all required proposed APIs
- **Improved:** Better compatibility with VS Code stable releases

### 1.1.0
- **New:** Windows support added! Now works on Windows, macOS, and Linux
- **New:** Includes WAV audio file for Windows compatibility (PowerShell SoundPlayer requires WAV format)
- **Improved:** Automatically selects correct audio format based on platform (MP3 for Linux/Mac, WAV for Windows)
- **Fixed:** Resolved audio playback issues on Windows systems

### 1.0.0
- Initial release
- Terminal error detection
- Configurable error patterns
- Volume control
- Toggle command
- Test sound command

---

Made with ❤️ for developers who want audible error notifications!
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
