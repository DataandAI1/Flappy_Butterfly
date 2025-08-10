# Flappy Butterfly Android Game 🦋

A fun and colorful butterfly adventure game where you dodge spiders, frogs, and bats while collecting power-ups! This Android app version brings the excitement of web gaming to your mobile device.

## Game Features

- **Multiple Enemies**: Dodge spiders, frogs, and bats
- **Power-ups**: Collect shields and star power for protection
- **Dynamic Difficulty**: Game gets harder as your score increases
- **Speed Settings**: Choose from Slow, Medium, or Fast gameplay
- **Escape Mechanic**: Tap 3 times to escape spider webs
- **High Score Tracking**: Beat your best score

## How to Open in Android Studio

### Prerequisites
- Android Studio (latest version recommended)
- Android SDK (API Level 21 or higher)
- Java Development Kit (JDK) 8 or higher

### Step-by-Step Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/DataandAI1/Flappy_Butterfly.git
   cd Flappy_Butterfly
   ```

2. **Open in Android Studio**
   - Launch Android Studio
   - Click "Open" or "File" → "Open"
   - Navigate to the cloned `Flappy_Butterfly` folder
   - Select the folder and click "OK"
   - Android Studio will automatically import the project

3. **Sync the Project**
   - Android Studio will prompt you to sync the project with Gradle files
   - Click "Sync Now" in the notification bar
   - Wait for the sync to complete

4. **Run the Game**
   - Connect an Android device via USB (with USB debugging enabled) OR
   - Create an Android Virtual Device (AVD) in Android Studio
   - Click the green "Run" button (▶️) or press `Shift + F10`
   - Select your device/emulator
   - The game will build and install automatically

## Project Structure

```
Flappy_Butterfly/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/flappybutterfly/
│   │   │   │   └── MainActivity.java       # Main Android activity
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   └── activity_main.xml   # Layout file
│   │   │   │   ├── values/
│   │   │   │   │   ├── colors.xml          # Color resources
│   │   │   │   │   ├── strings.xml         # String resources
│   │   │   │   │   └── themes.xml          # App themes
│   │   │   ├── assets/
│   │   │   │   └── flappy_butterfly.html   # Game HTML file
│   │   │   └── AndroidManifest.xml         # App manifest
│   │   └── build.gradle                    # App-level build config
├── gradle/                                  # Gradle wrapper files
├── build.gradle                             # Project-level build config
├── settings.gradle                          # Project settings
├── gradle.properties                        # Gradle properties
└── README.md                                # This file
```

## Technical Details

- **Min SDK Version**: 21 (Android 5.0 Lollipop)
- **Target SDK Version**: 34 (Android 14)
- **Programming Language**: Java
- **UI Technology**: WebView displaying HTML5/JavaScript game

## Gameplay Instructions

1. **Tap to Fly**: Tap the screen to make the butterfly fly upward
2. **Avoid Enemies**:
   - Spiders shoot webs at score 20+
   - Frogs appear at score 100+ with sticky tongues
   - Bats appear at score 150+ and chase you
3. **Collect Power-ups**:
   - 🌼 Golden Flowers: Shield protection
   - ⭐ Stars: Invincibility and enemy knockout ability
4. **Escape Webs**: If caught, tap 3 times quickly to escape

## Building the APK

1. In Android Studio, go to "Build" → "Build Bundle(s) / APK(s)" → "Build APK(s)"
2. Wait for the build to complete
3. Find the APK in `app/build/outputs/apk/debug/app-debug.apk`

## Troubleshooting

- **Gradle Sync Issues**: Try "File" → "Invalidate Caches and Restart"
- **Build Errors**: Ensure you have the latest Android SDK tools installed
- **Game Not Loading**: Check that the HTML file is in `app/src/main/assets/`
- **Performance Issues**: Enable hardware acceleration in AndroidManifest.xml (already configured)

## License

This project is open source. Feel free to modify and distribute.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

## Contact

For questions or support, please open an issue on GitHub.

Enjoy playing Flappy Butterfly! 🦋✨