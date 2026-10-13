# Fire TV Native Configurator v1.2.0

## Changes

- Simplified Remote Buttons: each APP row now has only a Select App button.
- Unselected assignments are preserved automatically; Apply changes only selected assignments that differ from the current configuration.
- Applying zero changes leaves settings and the backup untouched.
- Fixed an EPIPE failure caused by a shell function-name collision on Fire OS.
- Improved diagnostics for root process failures.
- Improved D-pad focus stability during operations.
- Info now displays the installed version from PackageManager.
- Device settings remain the source of truth after application reinstallation.

## Supported Environment

Root access is required. Validated device: Fire TV Stick 4K Max (2nd Generation), AFTKRT / karat, Fire OS 8.1.8.2. Other models and Fire OS versions remain unverified.

## Installation and Basic Use

Download Native-Configurator-v1.2.0.apk and verify the SHA-256 below. Use `adb install Native-Configurator-v1.2.0.apk` for a new installation, or `adb install -r Native-Configurator-v1.2.0.apk` for an existing installation signed with the same certificate. Do not bypass a signature mismatch by uninstalling. Grant root permission when prompted.

Open Remote Buttons, run Read Current, choose Select App for the buttons to change, then review and confirm Apply. Unselected buttons keep their assignments. A Fire TV restart may be required for changes to affect the physical remote.

Restore restores the latest P backup (the state immediately before the most recent Apply), then removes that backup after success. Finalize deletes the backup and keeps the current settings. Restore and Finalize do not delete A/G/N registrations.

## Artifact Verification

- Package: com.nativeconfigurator
- versionName: 1.2.0
- versionCode: 6
- Release certificate SHA-256: 4846a5a3b61450dc37308f11ffbc21c1372bfa019d66d6c0bf0a8b26df381d31
- APK: Native-Configurator-v1.2.0.apk
- APK SHA-256: 342f55a3f403ddd5d145abc9ea07b7b3db4e0718670d3dc6dc38669c04b2c937

## Validation

Debug and Release unit tests: 431 passed per variant; zero failures, errors or skipped tests. Debug and Release APK builds: successful.
