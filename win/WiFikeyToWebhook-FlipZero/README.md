# Wi-Fi key To Webhook by bst04

- This is a DuckyScript payload that collects Wi-Fi credentials from a Windows machine and sends them to a specified Discord webhook via a PowerShell script. The payload executes a series of commands on the target machine to extract the Wi-Fi password, then sends this information to a webhook for collection.

## Important:

This is a malicious payload. It is illegal and unethical to use this script on any system that you do not have explicit permission to access. Misuse of this script can result in severe legal consequences.
Features
Extracts Wi-Fi passwords stored in the system using netsh wlan export profile.
Sends the password data to a Discord webhook via an HTTP request.
Uses PowerShell to process and upload the extracted file (Wi-Fi profile) to the specified Discord webhook.

## Instructions:

- **Change the Webhook URL:** You need to replace `https://webhook` with your actual Discord webhook URL.
Example: `https://discord.com/api/webhooks/123456789012345678/abcdefghijklmnopqrstuvwxyz`.

## Payload Execution:

- The payload uses the Flipper Zero to execute the script on the target machine.
Upon execution, it:
1. Opens the cmd terminal.
2. Runs a PowerShell command to extract Wi-Fi credentials.
3. Sends the credentials (extracted as XML) to the specified webhook as an attachment.

## How It Works:

1. It executes the command to extract the Wi-Fi profiles and saves the result in a .xml file.

2. Then, it uploads this file to the webhook using a POST request with multipart form-data (including a message and the file).
