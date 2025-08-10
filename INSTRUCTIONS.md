# Android Studio Setup Instructions for Flappy Butterfly

## 📱 Quick Start Guide

This guide will help you open and run the Flappy Butterfly game in Android Studio.

## Prerequisites

### 1. Install Android Studio
- Download from: https://developer.android.com/studio
- During installation, make sure to install:
  - Android SDK
  - Android SDK Platform
  - Android Virtual Device (AVD)

### 2. System Requirements
- **Windows**: Windows 7/8/10 (64-bit)
- **Mac**: macOS 10.14 or higher
- **Linux**: 64-bit distribution with GNU C Library 2.19+
- **RAM**: Minimum 8GB (16GB recommended)
- **Disk Space**: 4GB + 1GB for Android SDK

## Step-by-Step Setup

### Step 1: Clone the Repository

#### Option A: Using Git Command Line
```bash
git clone https://github.com/DataandAI1/Flappy_Butterfly.git
```

#### Option B: Download ZIP
1. Go to https://github.com/DataandAI1/Flappy_Butterfly
2. Click the green "Code" button
3. Select "Download ZIP"
4. Extract the ZIP file to your desired location

### Step 2: Open in Android Studio

1. **Launch Android Studio**
2. **Open the Project**:
   - If you see the Welcome screen: Click "Open"
   - If you have a project open: Go to File → Open
3. **Navigate** to the `Flappy_Butterfly` folder you cloned/extracted
4. **Select** the folder and click "OK"
5. **Wait** for Android Studio to load and index the project

### Step 3: Configure SDK (if needed)

If you see an error about missing SDK:

1. Click "File" → "Project Structure" (or press `Ctrl+Alt+Shift+S`)
2. Under "SDK Location", set your Android SDK path
3. Click "OK"

### Step 4: Sync the Project

1. Look for a banner saying "Gradle files have changed"
2. Click "Sync Now"
3. Wait for the sync to complete (see progress bar at bottom)

**If sync fails:**
- Check your internet connection
- Try: File → Invalidate Caches and Restart
- Update Gradle if prompted

### Step 5: Run the Game

#### Option A: Using Physical Device

1. **Enable Developer Options on your Android device**:
   - Go to Settings → About Phone
   - Tap "Build Number" 7 times
   - Go back to Settings → Developer Options
   - Enable "USB Debugging"

2. **Connect your device** via USB cable

3. **Run the app**:
   - Click the green Run button (▶️) in toolbar
   - Select your device from the list
   - Click "OK"

#### Option B: Using Emulator

1. **Create an AVD (Android Virtual Device)**:
   - Click "AVD Manager" icon in toolbar
   - Click "Create Virtual Device"
   - Select a device (e.g., Pixel 4)
   - Download a system image (recommended: API 30+)
   - Click "Finish"

2. **Run the app**:
   - Click the green Run button (▶️)
   - Select the emulator
   - Click "OK"

## 🎮 Game Controls

- **Tap/Click**: Make butterfly fly upward
- **Speed Selection**: Choose difficulty at game start
- **Escape Mechanic**: Tap 3 times when caught in web

## 🛠️ Troubleshooting

### Common Issues and Solutions

#### "SDK location not found"
1. Create a file named `local.properties` in project root
2. Add: `sdk.dir=YOUR_SDK_PATH`
   - Windows: `sdk.dir=C:\\Users\\Username\\AppData\\Local\\Android\\Sdk`
   - Mac: `sdk.dir=/Users/Username/Library/Android/sdk`
   - Linux: `sdk.dir=/home/Username/Android/Sdk`

#### "Gradle sync failed"
- Update Gradle: File → Project Structure → Project → Gradle Version
- Clear cache: File → Invalidate Caches and Restart

#### "Cannot resolve dependencies"
- Check internet connection
- Try: Build → Clean Project, then Build → Rebuild Project

#### "Emulator won't start"
- Enable virtualization in BIOS
- Install Intel HAXM (for Intel CPUs)
- Try a different system image

#### "App crashes on launch"
- Check Logcat for errors (View → Tool Windows → Logcat)
- Ensure minimum SDK is 21 or higher
- Try: Build → Clean Project

## 📦 Building APK for Distribution

### Debug APK (for testing)
1. Build → Build Bundle(s) / APK(s) → Build APK(s)
2. Find APK at: `app/build/outputs/apk/debug/app-debug.apk`

### Release APK (for distribution)
1. Build → Generate Signed Bundle / APK
2. Select "APK"
3. Create or choose a keystore
4. Fill in the key details
5. Select "release" build variant
6. Find APK at: `app/build/outputs/apk/release/app-release.apk`

## 📁 Project Structure Overview

```
Flappy_Butterfly/
├── app/                          # Application module
│   ├── src/main/
│   │   ├── java/                # Java source code
│   │   ├── res/                 # Resources (layouts, images, etc.)
│   │   ├── assets/               # Game HTML file
│   │   └── AndroidManifest.xml  # App configuration
│   └── build.gradle              # App-level dependencies
├── gradle/                       # Gradle wrapper
├── build.gradle                  # Project-level configuration
└── settings.gradle               # Project settings
```

## 🔧 Customization Tips

### Change App Name
Edit `app/src/main/res/values/strings.xml`:
```xml
<string name="app_name">Your Game Name</string>
```

### Change App Icon
1. Right-click on `app/res` in Android Studio
2. New → Image Asset
3. Choose your icon image
4. Generate all sizes

### Modify Game Settings
Edit `app/src/main/assets/flappy_butterfly.html` to adjust:
- Game speed
- Colors
- Enemy spawn rates
- Power-up frequency

## 📚 Additional Resources

- [Android Developer Documentation](https://developer.android.com/docs)
- [Android Studio User Guide](https://developer.android.com/studio/intro)
- [WebView Documentation](https://developer.android.com/reference/android/webkit/WebView)

## 💡 Tips for Beginners

1. **Start with the emulator** before using a physical device
2. **Keep Android Studio updated** for best performance
3. **Use Logcat** to debug issues (bottom toolbar)
4. **Save your work** frequently (Ctrl+S)
5. **Read error messages carefully** - they often tell you exactly what's wrong

## 🆘 Need Help?

1. Check the [Issues](https://github.com/DataandAI1/Flappy_Butterfly/issues) section
2. Create a new issue with:
   - Your Android Studio version
   - Error messages (screenshots help!)
   - Steps you've tried

## 🎉 Success Checklist

- [ ] Android Studio installed
- [ ] Project opened successfully
- [ ] Gradle sync completed
- [ ] Emulator/device connected
- [ ] Game running
- [ ] High score achieved! 🦋

---

**Happy Gaming!** 🎮✨

If this guide helped you, consider giving the repository a ⭐!