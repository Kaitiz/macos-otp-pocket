# Changelog

## 1.2 — 2026-10-22

### Security
- Vault header is now authenticated, so tampering with the key information in the synced vault file is detected and ignored.
- Updates are only installed when signed by the same developer certificate, and the installed app is replaced in a single atomic step.
- Loosening App Lock settings now requires Touch ID or your Mac password.
- PIN attempt limits are stored in the Keychain; old Keychain items are cleaned up after migration.
- Warnings when saving exports or the recovery code to a cloud-synced folder (iCloud Desktop & Documents, Dropbox).

### Improvements
- Fewer redundant syncs and faster screen QR window selection.
- Clearer messages when updating from a DMG or a temporary location, and when GitHub rate-limits requests.
- Screen Recording permission flow and Quick Search hover behavior fixed.
- Vietnamese wording: "Kho dữ liệu" and "OTP kế tiếp".

## 1.1 — 2026-10-21

First public release.

- TOTP codes with SHA1/SHA256/SHA512, 6–8 digits and custom periods.
- Add accounts by scanning a QR code on screen, from images, or by importing backups from Aegis, 2FAS, Bitwarden, Proton, Raivo and more.
- Quick search from a global shortcut or the menu bar icon; press Enter to copy the code.
- Sort by name, recently added or recently used.
- One AES-256 encrypted vault in a hidden iCloud Drive folder (or a folder you choose), synced across your Macs.
- Automatic daily backups and optional encrypted backups to Google Drive.
- App Lock with Touch ID or your Mac password.
- Light and dark appearance, English and Vietnamese.
- In-app updates from GitHub.
- Restore default settings from Settings → General.
