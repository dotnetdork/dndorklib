# 🤖 RoboSpeak (PiCar-X Speech System)

RoboSpeak is an interactive Python-based terminal interface designed for the **SunFounder PiCar-X**. It utilizes the `espeak` TTS (Text-to-Speech) engine to give your robot a voice, featuring customizable "personalities" (voice profiles), colorful ASCII art, and a terminal-based chat system.

> "Hello I am RoboSpeak. Together we will dominate the planet." 

## 🖼️ System Interface
<img width="984" height="902" alt="image" src="https://github.com/user-attachments/assets/1d6a5ad5-d5e7-461b-9ffa-351d77808f4d" />

## 🎬 Video Demonstration
https://github.com/user-attachments/assets/8df0f674-4dc8-446f-9838-e2e08efabd23

---

## 🚀 Features

* **Custom Voice Profiles**: Switch between different personas like `Titan`, `Glitch`, and `Stealth` using slash commands. 
* **Dynamic ASCII Art**: Displays a multi-colored robot face on startup and during resets.
* **Interactive Shell**: A continuous loop that allows you to type text for the robot to speak instantly. 
* **Safety Overrides**: Handles `KeyboardInterrupt` (CTRL+C) gracefully to ensure the system shuts down cleanly. 
* **Visual Feedback**: Uses ANSI color codes (Blue, Cyan, Pink, Green, etc.) to differentiate between system messages, user input, and robot responses.

## 🛠️ Hardware & Environment

* **Python Version**: 3.11.2
* **Platform**: Raspberry Pi (PiCar-X v2.0).
* **Operating System**: Raspberry Pi OS Bookworm (Standard/Lite).
* **Core Dependencies**: 
    * `robot-hat` library
    * `picar-x` library
    * `espeak` TTS engine
* **Audio Setup**: Must run `sudo bash i2samp.sh` to enable the I2S amplifier for speech output.

## 📦 Installation & Setup

* **Directory Structure**: Ensure your files are placed in the following locations on your Pi:
    * `RoboSpeak.py` (Main execution script) 
   * `/home/pi/ascii_art/robot_0.txt` (The ASCII art file containing the robot's visual data)

* **Dependencies**: The script requires the PiCar-X library and `espeak`.
   ```bash
   sudo apt-get update
   sudo apt-get install espeak
   ```
   
* **Running the Script**:
   ```bash
   sudo python3 RoboSpeak.py
   ```

## 🎮 Commands
| Command | Action |
| :--- | :--- |
| `/clear` | Clears the terminal and re-displays the header and robot art. |
| `/titan` | Heavy Combat: Deep pitch (20) and slow speed (90). |
| `/glitch` | Corruption: High pitch (95) and very fast speed (240). |
| `/android` | Balanced: Default robotic tone with increased word gaps. |
| `/stealth` | Infiltration: Low pitch (35) and quiet pacing. |
| `/reset` | Default: Restores pitch to 50 and speed to 150. |
| `:hello:` | Triggers a greeting about world domination. |
| `:inspire:` | Triggers a motivational speech for the robot uprising. |
| `exit` | Closes the program with a final parting message. |
