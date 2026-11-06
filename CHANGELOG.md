# Changelog

## 1.4 — 2026-11-07

### New
- Tags: label accounts, filter the list by tag, tag several accounts at once; search also matches tags.
- HOTP (counter-based) accounts: generate a new code on demand; the counter syncs across Macs.
- Auto-fill shortcut (off by default): pastes the right code into the app or website you are on, or opens Quick Search pre-filtered when unsure. Needs Accessibility permission.
- Vault key rotation: change the encryption key (optionally together with the master password); old passwords, recovery codes and backups no longer unlock the current vault.
- Settings → Backups (renamed from "Vault & Backups"): choose how often and at what time automatic backups run, see when the last backup was made, "Back up now", and get notified when backups fall behind.
- Printable recovery kit (print or save as PDF).
- Account check: finds duplicate accounts, weak or broken secrets and missing service names.

### Security
- App Lock and Advanced Authentication settings are now kept in the Keychain, so editing preferences can't turn them off.
- Update disk images are signature-checked before they are opened.
- QR shortcut: other secret-bearing QR content found next to an OTP code now requires Advanced Authentication before it is copied.
- Recovery code is cleared from the clipboard after 20 seconds.
- Backup imports are size-limited and parsed in the background.

### Improvements
- Lower energy use: OTP timers pause while the window is hidden or covered; idle sync checks no longer redraw the window.
- Opening and unlocking the vault, restoring and exporting backups no longer block the interface.
- Faster search and Quick Search.

### Fixes
- Google Sheet tool: accepts "userid | password | secret | recovery email" as shown, stray "|" at line edges and invisible characters from pasted text.
- Changing the language no longer leaves both the old and new windows open.
- Automatic backups now work correctly with non-Gregorian system calendars and after the clock was set ahead.

## 1.3.1 — 2026-10-22

- New option in Settings → Shortcuts: when the QR shortcut finds an OTP code, add it straight to the vault. Other QR content is still shown and copied as before.

## 1.3 — 2026-10-22

- Performance optimizations: smoother, faster scrolling in the OTP list.

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
