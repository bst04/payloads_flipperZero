# USB Device Listing Script - by cybersleuth99

## Overview

This script is designed to list all USB devices connected to a system running macOS. It automatically opens a terminal, runs a system command to gather information about connected USB devices, and saves this information to a text file on the user's desktop.

## Features

- Opens the terminal on macOS.
- Executes a system command to list all connected USB devices.
- Saves the output to a text file (`usb_devices.txt`) on the user's Desktop.

## Requirements

- macOS operating system.
- The script uses the built-in `system_profiler` command, which is available on macOS by default.

## How It Works

1. **GUI Trigger**: The script simulates pressing the **Spacebar** (via `GUI SPACE`) to bring up the Spotlight search bar.
2. **Open Terminal**: The script types `terminal` and presses **Enter** to open the Terminal app.
3. **Delay**: The script introduces small delays (`DELAY 1000` and `DELAY 500`) to allow the system to respond between actions.
4. **Execute Command**: Once the Terminal is open, the script types the following command: 'system_profiler SPUSBDataType > ~/Desktop/usb_devices.txt' This command queries the system for USB device information and saves it to a file named `usb_devices.txt` on the user's Desktop.
5. **Close Terminal**: The terminal remains open after the command is executed, allowing the user to review the output.

