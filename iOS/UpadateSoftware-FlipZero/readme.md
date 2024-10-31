# 🔄 UpdateSoftware-MacOS by bst04

## ℹ️ Description

This payload, created by bst04, is designed to initiate a system software update on a macOS device. It uses Terminal commands to update all available software and then restart the computer.

---

## 📖 Technical Explanation

1. **Initialization**:
    - `DELAY 2000`: Waits for 2 seconds to ensure the system is ready.
    - `GUI SPACE`: Simulates pressing "Command" + "Space" to open Spotlight Search.
    - `DELAY 250`: Waits for 0.25 seconds to ensure Spotlight is open.
    - `STRING TERMINAL`: Types "TERMINAL" to search for the Terminal application.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `ENTER`: Opens the Terminal application.

2. **Execute Software Update**:
    - `DELAY 250`: Waits for 0.25 seconds to ensure Terminal is fully opened.
    - `STRING sudo softwareupdate -i -a -R`: Types the command to update all available software and restart the computer.
    - `DELAY 500`: Waits for 0.5 seconds.
    - `ENTER`: Executes the software update command.

---

## 📜 Usage

1. Copy the payload script to your DuckyScript-enabled device.
2. Ensure the device is connected to a macOS system.
3. Execute the payload to initiate the system software update and restart.

---
