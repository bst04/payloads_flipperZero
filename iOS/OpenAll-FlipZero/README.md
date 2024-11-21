# OpenALL by bst04

## Overview

The **OpenALL** script is designed to automatically open all applications located in the `/Applications` directory on a macOS system. The script uses a simple loop to open each `.app` file it finds in the specified folder.

## Script Information

- **Title**: OpenALL
- **Author**: bst04
- **Version**: 1.0
- **Category**: Execution
- **Target OS**: macOS

## Features

- Opens all applications in the `/Applications` directory on a macOS system.
- Uses a loop to open every `.app` file in the system's Applications folder.

## Requirements

- macOS operating system.
- The script relies on the macOS terminal and the `open` command, which are available by default on macOS.

## How It Works

1. **GUI Trigger**: The script simulates pressing **Spacebar** (via `GUI SPACE`) to bring up the Spotlight search bar.
2. **Open Terminal**: The script types `terminal` and presses **Enter** to open the Terminal app.
3. **Delay**: The script includes delays (`DELAY 1000` and `DELAY 500`) to allow the system to respond between actions.
4. **Execute Command**: Once the Terminal is open, the script types the following command: `for app in /Applications/*.app; do open "$app"; done`. This command loops through every `.app` file found in the `/Applications` folder and opens each one using the `open` command.
5. **Result**: After executing the script, all applications in the `/Applications` folder will be launched.

