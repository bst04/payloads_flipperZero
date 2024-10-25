# 🔋 CheckBateryWin-FlipZero

## ℹ️ Description

This script, created by bst04, is designed to work on Windows devices. It generates a battery report and opens the report file using PowerShell.

---

## 📖 Technical Explanation

1. **Initialization**:
    - `DELAY 1000`: Waits for 1 second to ensure the system is ready.
    - `GUI r`: Simulates pressing "Windows" + "R" to open the Run dialog.
    - `DELAY 750`: Waits for 0.75 seconds to ensure the Run dialog is open.

2. **Generate Battery Report**:
    - `STRING powershell -w h -NoP powercfg /batteryreport /output /Desktop/battery-report.html`: Types a PowerShell command to generate a battery report and save it to the desktop.
    - `DELAY 750`: Waits for 0.75 seconds to ensure the command is fully typed.
    - `ENTER`: Executes the PowerShell command.

3. **Open Battery Report**:
    - `GUI r`: Simulates pressing "Windows" + "R" again to open the Run dialog.
    - `DELAY 850`: Waits for 0.85 seconds to ensure the Run dialog is open.
    - `STRING battery-report.html`: Types the name of the battery report file.
    - `DELAY 750`: Waits for 0.75 seconds.
    - `ENTER`: Opens the battery report file.

---

## 📜 Usage

1. Copy the payload script to your DuckyScript-enabled device.
2. Ensure the device is connected to a Windows system.
3. Execute the payload to generate a battery report and open the report file.

---
