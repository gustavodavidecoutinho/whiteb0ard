# whiteb0ard 

**whiteb0ard** is a lightweight, open-source rootless iOS tweak that completely disables **Screen Time** and **iCloud Screen Time Syncing** (hopefully) by safely modifying system preferences.
---

## How It Works

**whiteb0ard** toggles key flags inside the official Apple Screen Time configuration file:

`/var/mobile/Library/Preferences/com.apple.ScreenTimeAgent.plist`

During installation, the package automatically updates:
- `ScreenTimeEnabled` ➔ `false`
- `SyncEnabled` ➔ `false` (prevents iCloud from restoring restrictions)

After modifying the configuration, it performs a clean **userspace reboot** (`launchctl reboot userspace`) to apply changes immediately without breaking your jailbreak state.

---

## Installation Instructions

Using sileo or other APT package manager such as cydia

Add the official APT repository to your package manager of choice:

**Repository URL:**
```bash
https://gustavodavidecoutinho.github.io/whiteb0ard/
```
