# Windows setup

## Requirements

- Windows 11 x64 (other Windows versions not yet verified).
- Compatible vJoy driver for virtual joystick controls.
- Compatible SimButtonbox Android app and a shared local network.

## Install and connect

1. Download the Windows ZIP from the [Releases page](https://github.com/standby929/simbuttonbox-release/releases) when available. Extract the entire archive into a dedicated folder; keep all included files together.
2. Install a compatible vJoy driver from https://vjoy.pro/. Restart if requested. In Configure vJoy, enable device 1 and configure 128 buttons. Check the device with `joy.cpl`.
3. Start `SimButtonbox.NativeHelper.exe`. If Windows shows a security warning, verify the origin and published checksum before proceeding. Do not disable security protections.
4. Connect your PC and Android device to the same local network. Allow the server through the firewall on trusted private networks only; do not expose it to the internet.
5. Scan the QR code in the Android app, or enter the server address manually and compare verification codes. Enter the PIN displayed on Windows. Keep the server running.
6. In Advanced / Action Mapping, configure actions. In the game's controls menu, select a binding and press the corresponding Android button. Server mappings do not automatically configure the game.

## Troubleshooting

Check vJoy device 1, network address, private-network firewall rules and the connected-device counter. For LMU telemetry, enter a driving session and check the Game tab. Diagnostic logs can be enabled in Advanced and are stored under `%LOCALAPPDATA%\SimButtonbox\logs`. Review and redact sensitive information before sharing logs.

## Updating

Close the server before extracting a new release. Keep a backup of the previous installation and settings. Follow version-specific release notes.

