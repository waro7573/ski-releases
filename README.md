# SKI — Releases & downloads

**Voice for your coding agent.** Talk to Claude Code, Cursor, Codex, Gemini CLI and more — out loud — and hear them answer in a natural voice. Everything runs on your machine; nothing you say ever leaves it.

→ **[heyski.io](https://heyski.io)**

This repository hosts the **official SKI downloads and the auto‑update feed** for macOS and Windows. It contains release binaries only — not the app source.

---

## Download

Get the newest build from the **[Releases](../../releases/latest)** page:

| Platform | File | Requirements |
|---|---|---|
| **macOS** (Apple Silicon) | `SKI_<version>_aarch64.dmg` | macOS 14.4 (Sonoma) or newer · M1 or later |
| **Windows** | `SKI_<version>_x64-setup.exe` | Windows 10 / 11 · x64 / ARM |

## Install

**macOS**
1. If SKI is already installed, **delete `/Applications/SKI.app` first** — old copies can stay Gatekeeper‑blocked and a fresh download won't heal them.
2. Open the DMG and drag **SKI** to Applications.
3. First launch shows the standard "downloaded from the Internet" prompt → **Open**.
4. Verify: **SKI → Preferences → About** shows the version.

**Windows**
1. Run the installer. Windows may show a SmartScreen **“Windows protected your PC”** notice (the build isn’t code‑signed yet) → click **More info → Run anyway**.
2. Follow the prompts, then launch **SKI** from the Start menu.

## Verify your download
```bash
shasum -a 256 SKI_<version>_aarch64.dmg     # macOS
```
The expected hash is printed in each release's notes.

## Automatic updates
Once installed, **SKI checks for new releases automatically**. On macOS the update downloads in the background and applies when you relaunch; on Windows you click **Restart now** in Preferences → About and the signed installer runs. Every update is **cryptographically signed**, and SKI verifies the signature before applying it — so even a compromised download host can never push a tampered build to you.

## Make your agent talk — the SKI skill
The app gives you the widget; the **[SKI skill](https://github.com/pattern-ai-labs/ski)** gives your coding agent ears and a voice. Install it once per agent — instructions are in that repo.

## Security & privacy
macOS builds are **Developer‑ID signed and notarized**. Windows builds aren’t code‑signed yet, so Windows may warn on first install — but every auto‑update is **cryptographically signed and verified** before it’s applied. Speech‑to‑text and the voice both run **on‑device** — your voice is never uploaded. Details at [heyski.io](https://heyski.io).

## Support
**support@heyski.io**
