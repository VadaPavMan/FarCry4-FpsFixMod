# Changelog

All notable changes to this project will be documented in this file.

## [1.0.0] - 2026-07-25

### Added
- **Profile Configuration:** Automatically checks and updates `Documents\My Games\Far Cry 4` performance settings on startup.
- **`GamerProfile.xml` Tweaks:** Sets `DisableLoadingMip0="1"` and `GPUMaxBufferedFrames="1"` to improve frame pacing.
- **`GFXSettings.FarCry464.xml` Tweaks:** Caps the `GEOMETRY` option to `Value="high"`.
- **Automatic Backup:** Creates a one-time `.fc4fpsfix.backup` copy prior to modifying any XML files.
- **Process Management:** Detects `farcry4.exe`, waits for the configured initialization period, and applies High process priority.
- **CPU Affinity:** Assigns a four-logical-processor affinity profile (Intel: `0, 2, 4, 6`; AMD: `2, 4, 6, 8`).
- **Performance Enhancements:** Includes optional 1 ms timer resolution, memory working-set trimming, and High Performance power-plan switching while active.

### Changed
- **Visual Quality Trade-offs:** Reduced texture sharpness by disabling the highest mip level (`DisableLoadingMip0="1"`).
- **Geometry Cap:** Limited graphic geometry settings strictly to High to ensure smoother frame rates.

### Restored
- **System Defaults:** Automatically reverts the timer resolution and power plan back to original settings after `farcry4.exe` exits.
