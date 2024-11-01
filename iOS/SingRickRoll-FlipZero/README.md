# SingRickRoll-FlipZero by bst04

## ℹ️ Description

This payload, created by bst04, is designed to maximize the system volume, play a text-to-speech rendition of Rick Astley's "Never Gonna Give You Up," and then open a photo of Rick Astley in the web browser on a macOS device.

---

## 📖 Technical Explanation

1. **Initialization**:
    - `DELAY 1000`: Waits for 1 second to ensure the system is ready.
    - `GUI SPACE`: Simulates pressing "Command" + "Space" to open Spotlight Search.
    - `DELAY 250`: Waits for 0.25 seconds to ensure Spotlight is open.

2. **Open Terminal**:
    - `STRING TERMINAL`: Types "TERMINAL" to search for the Terminal application.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `ENTER`: Opens the Terminal application.

3. **Set Volume to Max**:
    - `DELAY 250`: Waits for 0.25 seconds to ensure Terminal is fully opened.
    - `STRING VOL=$(osascript -e 'Set Volume 100')`: Types the AppleScript command to set the system volume to 100%.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `ENTER`: Executes the command to set the volume.

4. **Text-to-Speech**:
    - `DELAY 250`: Waits for 0.25 seconds.
    - `STRING say Never gonna give you up Never gonna let you down. Never gonna run around and desert you. Never gonna make you cry. Never gonna say goodbye. Never gonna tell a lie and hurt you`: Types the command to use text-to-speech to play the specified text.
    - `DELAY 500`: Waits for 0.5 seconds.
    - `ENTER`: Executes the text-to-speech command.

5. **Open Rick Astley Photo**:
    - `DELAY 250`: Waits for 0.25 seconds.
    - `GUI SPACE`: Simulates pressing "Command" + "Space" to open Spotlight Search again.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `STRING https://149367133.v2.pressablecdn.com/wp-content/uploads/2021/02/rick-astley-never-gonna-give-you-up-4k-1000x600.jpg`: Types the URL of the Rick Astley photo.
    - `DELAY 250`: Waits for 0.25 seconds.
    - `ENTER`: Opens the photo in the default web browser.

---

## 📜 Usage

1. Copy the payload script to your DuckyScript-enabled device.
2. Ensure the device is connected to a macOS system.
3. Execute the payload to maximize the volume, play the text-to-speech rendition of the song, and open the Rick Astley photo.

---
