# Sorin

**Use your Windows PC's keyboard and mouse on your iPad — and on your iPhone, Android phone or tablet, over Bluetooth.**
Nothing to install on the other device: your PC simply appears to it as a Bluetooth keyboard and mouse.

**[⬇ Download the latest Sorin.exe](https://github.com/Jadtz/Sorin/releases/latest)**

---

## Getting started

1. Download **Sorin.exe** from the [latest release](https://github.com/Jadtz/Sorin/releases/latest) and run it.
   Sorin installs itself for your Windows user (no admin rights needed) and adds a Start-menu shortcut.
2. On your device, open its Bluetooth settings and tap your PC's name:
   - **iPad / iPhone:** Settings → Bluetooth
   - **Android:** Settings → Connected devices → Pair new device
3. Confirm the pairing on both devices.
4. Press **Ctrl + Alt + I** to control the device. Press **Ctrl + Alt + Q**, or **Esc three times**, to come back to the PC.

With more than one device connected, press **Ctrl + Alt + I** again to move to the next one.

**iPhone:** the keyboard works straight away. To see a mouse pointer, turn on **Settings → Accessibility → Touch → AssistiveTouch**.

**Android:** the keyboard and the mouse pointer both work straight away.

**Non-US keyboard?** If the device types the wrong characters, set it to the same layout as your PC:
- **iPad / iPhone:** Settings → General → Keyboard → Hardware Keyboard
- **Android:** Settings → System → Keyboard → Physical keyboard

## Works with

| Device | Status |
|---|---|
| **iPad** | ✅ Tested, keyboard and mouse |
| **iPhone** | ✅ Tested; keyboard, plus mouse with AssistiveTouch |
| **Android phones and tablets** | ✅ Expected to work: the Bluetooth keyboard code Sorin builds on is confirmed on Android |
| **Mac, ChromeOS, Linux, other Windows PCs** | Should work: anything that accepts a standard Bluetooth keyboard and mouse |
| **Smart TVs, consoles** | Varies by model |

Tried Sorin with something not listed? [Open an issue](https://github.com/Jadtz/Sorin/issues) and let us know how it went.

## "Windows protected your PC"

When you open Sorin for the first time, Windows will probably show a blue **"Windows protected your PC"** window. This is expected, and here is why.

Windows shows this warning for programs that are **new** and **not code-signed**. Code signing is a paid certificate, renewed every year, that comes with an identity-verification process. Sorin is a new, independent app and isn't signed yet. The warning doesn't mean Windows found anything wrong with Sorin. It means Windows doesn't know Sorin yet.

**To continue:** click **More info**, then **Run anyway**. You only need to do this once.

Signing is planned. Even after Sorin is signed, Windows shows the warning to new apps until enough people have downloaded them.

### Check the file yourself

You don't have to take our word for it.

- **Make sure you downloaded the right file.** Each release lists a SHA-256 checksum in `SHA256SUMS.txt`. In PowerShell, run:
  ```powershell
  Get-FileHash .\Sorin.exe
  ```
  The result should match the checksum for that release.
- **Scan it.** Upload `Sorin.exe` to [VirusTotal](https://www.virustotal.com) to check it with dozens of antivirus engines.

Some antivirus programs are cautious about any app that reads the keyboard, because keyloggers do too. Sorin needs to read the keyboard so it can pass your typing to your device.

## Privacy

- Your key presses and mouse movements go **only to the device you're controlling**, directly over Bluetooth.
- Nothing you type is stored or logged, and nothing is sent over the internet.
- Sorin connects to the internet only to check this page for updates. You can turn that off in **Settings → Updates**.

## Requirements

- **Windows 11** (64-bit).
- A Bluetooth adapter that supports the **LE peripheral role**. Most recent built-in adapters do. If yours doesn't, Sorin tells you.
- **iPadOS / iOS 13.4** or later, **Android**, or any device that supports Bluetooth keyboards.

Only one app at a time can act as a Bluetooth keyboard. If another one is running, close it first; Sorin tells you which one it is.

## Updating

Sorin updates itself. You can also open **Settings → Updates → Check for updates**.
If an update ever fails to start, Sorin automatically goes back to the previous version.

## Uninstalling

Open **Settings**, scroll to the bottom and click **Uninstall Sorin…**. This removes the app, its settings, the Start-menu shortcut and the startup entry.
Your Bluetooth pairings stay; forget the device in Bluetooth settings if you like.

## Open-source software

Sorin is built on open-source projects, including Universal Bridge, windows-ble-hid, Win2Pad and Avalonia. Their licences are in `THIRD_PARTY_NOTICES.txt`, attached to each release and also under **Open-source licenses** at the bottom of Settings.
