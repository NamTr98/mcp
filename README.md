# Everfit App Automation: Simulator & Agent Setup

## Prerequisites
- macOS
- Android Studio (with Android Emulator)
- Everfit app installed on the emulator
- Agent environment (this project)

## 1. Start the Android Emulator
1. Open Android Studio.
2. Go to **Tools > Device Manager**.
3. Start the `Pixel 9` (or your desired) emulator.

Alternatively, from the terminal:
```zsh
# List available emulators
emulator -list-avds
# Start the Pixel 9 emulator (replace with your AVD name if different)
emulator -avd "Pixel_9_Pro_XL"
```

## 2. Install the Everfit App (if not already installed)
- Drag and drop the Everfit APK onto the emulator, or run:
```zsh
adb install path/to/everfit.apk
```

## 3. Connect the Agent to the Emulator
- Ensure the emulator is running.
- The agent will automatically detect and connect to the running emulator (e.g., `emulator-5554`).
- To verify connection:
```zsh
adb devices
```
You should see the emulator listed.

## 4. Run Automation/Verification Tasks
- Use the agent's interface or scripts to:
  - Launch the Everfit app
  - Take screenshots
  - Compare UI with reference images (e.g., `img/test.png`)

## 5. Troubleshooting
- If the emulator is not detected, restart it and ensure `adb` is running.
- For UI comparison, ensure your reference image is in the `img/` directory.

---

For further automation or custom agent commands, refer to the project documentation or scripts provided in this workspace.
