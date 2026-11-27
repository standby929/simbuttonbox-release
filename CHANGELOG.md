# Changelog

Published versions and their changes are also documented on the [GitHub Releases page](https://github.com/standby929/simbuttonbox-release/releases).

## [0.1.0-alpha.3] - 2026-11-27

### Added

- WebSocket support for removing unused custom keyboard action registrations.

### Fixed

- Improved cleanup of custom keyboard actions when buttons or button groups are deleted.
- Improved handling of modified keyboard shortcuts.
- Safe release of active keyboard inputs before removing custom action registrations.

### Improved

- Custom action lifecycle and resource management.
- Isolation of custom keyboard actions between connected Android devices.

### Compatibility

- Existing Android clients remain compatible.
- Immediate custom action cleanup requires an updated Android client.

## [0.1.0-alpha.2] - 2026-11-27

### Added

- LMU green flag detection at race start.
- Player-specific chequered flag detection.
- Drive Through (DT) penalty detection, including penalty reason.
- Stop & Go (SG) penalty detection, including penalty duration and reason.
- Automatic penalty clearance detection.
- Race Control information on the Windows server's Game tab.
- Extended WebSocket telemetry for Race Control events.

### Improved

- Race Control state management.
- Extended LMU telemetry diagnostics.

### Compatibility

- Existing Android clients remain compatible.
- Android visualization of the new Race Control signals will be introduced in a future mobile update.

## [0.1.0-alpha.1]

### Added

- Initial public alpha release of SimButtonbox Server.
- Wireless Android connectivity, secure QR and manual pairing, PIN authentication and automatic reconnection.
- Simultaneous connections from multiple Android devices.
- vJoy virtual joystick integration and Windows keyboard shortcuts.
- Configurable action mappings.
- Le Mans Ultimate telemetry and supported flag feedback.
- English and Hungarian localization, built-in help and startup splash screen.
- Centralized versioning and automatic and manual GitHub release checks.
- Offline-safe update error handling.
- Third-party license documentation.
- Self-contained Windows x64 distribution and SHA-256 checksum.

### Known limitations

- The Android application is not yet publicly available on Google Play.
- Windows 11 x64 has been tested; other Windows versions have not been verified.
- The Windows executable is not digitally signed.
- Updates require manual download and installation.
- This is an early alpha release and may contain undiscovered issues.
