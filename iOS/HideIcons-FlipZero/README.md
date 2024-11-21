# Hide Icons - by Cybersleuth99

## Overview

This script is designed to hide all desktop icons on a macOS system. It opens the terminal, runs a system command to disable desktop icons, and then restarts the Finder to apply the changes.

## Features

- Opens the terminal on macOS.
- Executes a system command to hide desktop icons.
- Restarts the Finder to apply the changes immediately.

## Requirements

- macOS operating system.
- The script uses the built-in `defaults` and `killall` commands, which are available on macOS by default.

## How It Works

1. **GUI Trigger**: The script simulates pressing **Command + Space** (via `COMMAND SPACE`) to open the Spotlight search bar.
2. **Open Terminal**: The script types `terminal` and presses **Enter** to open the Terminal app.
3. **Delay**: The script introduces small delays (`DELAY 1000` and `DELAY 500`) to allow the system to respond between actions.
4. **Execute Command**: Once the Terminal is open, the script types the following command: `defaults write com.apple.finder CreateDesktop false; killall Finder`. This command disables desktop icons by modifying the Finder settings and then restarts Finder to apply the changes.
5. **Result**: After the command executes, all desktop icons will be hidden. To show them again, the script can be reversed by changing `false` to `true` in the `defaults` command.


