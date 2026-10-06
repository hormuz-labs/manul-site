---
name: install-manul
description: Install Manul, the free open-source video editor you talk to, on macOS (Homebrew) or Debian/Ubuntu (apt), or with an AppImage on other Linux. Use when the user asks to install, set up or update Manul.
---

# Install Manul

Manul is a desktop video editor for macOS 12+ and Linux. Detect the system, then run the matching steps. Ask before using `sudo`.

## macOS

```bash
brew install hormuz-labs/tap/manul
```

No Homebrew: download the `.dmg` for this Mac (`arm64` for Apple silicon, `x64` for Intel) from https://github.com/hormuz-labs/manul/releases/latest. Until notarization is done, the first launch needs right-click → Open.

## Debian and Ubuntu

```bash
curl -fsSL https://apt.manul.si/manul.gpg | sudo gpg --dearmor -o /usr/share/keyrings/manul.gpg
echo "deb [signed-by=/usr/share/keyrings/manul.gpg] https://apt.manul.si stable main" | sudo tee /etc/apt/sources.list.d/manul.list
sudo apt update && sudo apt install manul
```

## Other Linux

Download `manul_<version>_x86_64.AppImage` or `manul_<version>_arm64.AppImage` from https://github.com/hormuz-labs/manul/releases/latest, `chmod +x` it, and run it.

## After installing

Open Manul. It asks for a Claude, Gemini or OpenAI API key, kept in the system keychain. Updates install themselves (Homebrew and apt also update it).
