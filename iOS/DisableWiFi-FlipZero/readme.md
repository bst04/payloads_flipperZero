# 🛜 DisableWiFi-FlipZero by bst04

## ℹ️ Description

This payload, created by bst04, is designed to turn off the Wi-Fi on a macOS system. To turn the Wi-Fi back on, simply modify the script to replace "off" with "on".

---

## 📖 Technical Explanation

1. **Initialization**:
    - `DELAY 1000`: Waits for 1 second to ensure the system is ready.
    - `GUI SPACE`: Simulates pressing "Command" + "Space" to open Spotlight Search.
    - `DELAY 250`: Waits for 0.25 seconds to ensure Spotlight is open.
    - `STRING TERMINAL`: Types "TERMINAL" to search for the Terminal application.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `ENTER`: Opens the Terminal application.

2. **Turn Off Wi-Fi**:
    - `DELAY 250`: Waits for 0.25 seconds to ensure Terminal is fully opened.
    - `STRING networksetup -setnetworkserviceenabled Wi-Fi off`: Types the command to turn off Wi-Fi.
    - `DELAY 500`: Waits for 0.5 seconds.
    - `ENTER`: Executes the command to turn off Wi-Fi.

3. **Close Terminal**:
    - `DELAY 250`: Waits for 0.25 seconds.
    - `GUI q`: Simulates pressing "Command" + "q" to quit the Terminal application.

---

## 📜 Usage

1. Copy the payload script to your DuckyScript-enabled device.
2. Ensure the device is connected to a macOS system.
3. Execute the payload to turn off the Wi-Fi.

---

## 🛠️ Modification

To turn the Wi-Fi back on, replace `"off"` with `"on"` in the following line of the script:

```plaintext
STRING networksetup -setnetworkserviceenabled Wi-Fi on
