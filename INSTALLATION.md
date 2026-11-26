# Windows setup

## Requirements

- Windows 11 x64 (other Windows versions not yet verified).
- No separate .NET runtime installation required.
- Compatible vJoy driver for virtual joystick controls.
- Compatible SimButtonbox Android app and a shared local network.

## Install and connect

1. Download `SimButtonbox-Windows-x64.zip` and `SHA256SUMS.txt` from the [Releases page](https://github.com/standby929/simbuttonbox-release/releases). Verify the checksum as described below, then extract the entire archive into a dedicated folder; keep all included files together.
2. Install a compatible vJoy driver from https://vjoy.pro/. Restart if requested. In Configure vJoy, enable device 1 and configure 128 buttons. Check the device with `joy.cpl`.
3. Start `SimButtonbox.NativeHelper.exe`. If Windows shows a security warning, verify the origin and published checksum before proceeding. Do not disable security protections.
4. Connect your PC and Android device to the same local network. Allow the server through the firewall on trusted private networks only; do not expose it to the internet.
5. Scan the QR code in the Android app, or enter the server address manually and compare verification codes. Enter the PIN displayed on Windows. Keep the server running.
6. In Advanced / Action Mapping, configure actions. In the game's controls menu, select a binding and press the corresponding Android button. Server mappings do not automatically configure the game.

## Verify the download

In PowerShell, from the folder containing both downloaded files, run:

```powershell
$actual = (Get-FileHash .\SimButtonbox-Windows-x64.zip -Algorithm SHA256).Hash
$expected = ((Get-Content .\SHA256SUMS.txt -Raw).Trim() -split '\s+')[0]
$actual -eq $expected
```

The result should be `True`. If it is not, do not run the downloaded application. Download the files again from the official release page. The executable is currently unsigned; checksum verification confirms consistency with the published checksum, not a digital signature.

## Troubleshooting

Check vJoy device 1, network address, private-network firewall rules and the connected-device counter. For LMU telemetry, enter a driving session and check the Game tab. Diagnostic logs can be enabled in Advanced and are stored under `%LOCALAPPDATA%\SimButtonbox\logs`. Review and redact sensitive information before sharing logs.

## Updating

The server checks for compatible updates at startup when an internet connection is available. You can also use **Check for updates** in the Help tab. An unavailable internet connection does not prevent normal server startup.

Updates are not installed automatically. If a newer release is available, open its release page, download the new ZIP and checksum, and verify the download. Close the server before extracting the new release into a separate folder. Keep a backup of the previous installation and settings. Follow version-specific release notes.

Third-party license documents are included in the distribution and accessible from the Help tab.
