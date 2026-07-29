# 39. Useful Commands

This document contains the most commonly used React Native CLI, npm, Android, and Git commands.

---

# Node.js

Check Node Version

```bash
node -v
```

Check npm Version

```bash
npm -v
```

Check npx Version

```bash
npx -v
```

---

# React Native CLI

Create New Project

```bash
npx @react-native-community/cli init MyApp
```

Run Android App

```bash
npx react-native run-android
```

Run iOS App

```bash
npx react-native run-ios
```

Start Metro Bundler

```bash
npx react-native start
```

Check Development Environment

```bash
npx react-native doctor
```

---

# npm Commands

Install All Dependencies

```bash
npm install
```

Install a Package

```bash
npm install axios
```

Install Development Dependency

```bash
npm install --save-dev jest
```

Remove Package

```bash
npm uninstall axios
```

Update Packages

```bash
npm update
```

List Installed Packages

```bash
npm list
```

---

# Android Commands

Check Connected Devices

```bash
adb devices
```

Install APK

```bash
adb install app-release.apk
```

Uninstall App

```bash
adb uninstall com.myapp
```

View Connected Device

```bash
adb devices -l
```

View Logs

```bash
adb logcat
```

Restart ADB

```bash
adb kill-server

adb start-server
```

---

# Gradle Commands

Go to Android Folder

```bash
cd android
```

Generate Debug APK

```bash
gradlew assembleDebug
```

Generate Release APK

```bash
gradlew assembleRelease
```

Generate Release AAB

```bash
gradlew bundleRelease
```

Clean Project

```bash
gradlew clean
```

---

# Metro Commands

Start Metro

```bash
npx react-native start
```

Reset Metro Cache

```bash
npx react-native start --reset-cache
```

---

# Cache Cleaning

Delete node_modules

```bash
rm -rf node_modules
```

Windows

```cmd
rmdir /s /q node_modules
```

Install Again

```bash
npm install
```

Clean Android Build

```bash
cd android

gradlew clean
```

---

# Git Commands

Clone Repository

```bash
git clone <repository-url>
```

Check Status

```bash
git status
```

Create Branch

```bash
git checkout -b feature/login
```

Switch Branch

```bash
git checkout main
```

Add Files

```bash
git add .
```

Commit

```bash
git commit -m "Add login screen"
```

Push Code

```bash
git push origin main
```

Pull Latest Changes

```bash
git pull
```

---

# Emulator Commands

List Devices

```bash
adb devices
```

Reconnect Device

```bash
adb reconnect
```

Reverse Port

```bash
adb reverse tcp:8081 tcp:8081
```

---

# Useful npm Commands

Show Outdated Packages

```bash
npm outdated
```

Update Specific Package

```bash
npm install axios@latest
```

Install Exact Version

```bash
npm install axios@1.11.0
```

---

# Useful React Native Commands

Start Metro

```bash
npx react-native start
```

Run Android

```bash
npx react-native run-android
```

Run Android on Specific Device

```bash
npx react-native run-android --deviceId=<device-id>
```

Run Release Build

```bash
npx react-native run-android --mode=release
```

---

# Environment Commands

Check Java Version

```bash
java -version
```

Check ADB Version

```bash
adb version
```

Check Android SDK

```bash
echo %ANDROID_HOME%
```

---

# Useful Folder Commands

Go to Project

```bash
cd MyApp
```

Go to Android Folder

```bash
cd android
```

Go Back

```bash
cd ..
```

---

# Build Flow

```
Clone Project

↓

npm install

↓

Start Metro

↓

Connect Device

↓

Run Android

↓

Application Installed
```

---

# Best Practices

✅ Run `npm install` after cloning a project.

✅ Run `npx react-native doctor` if setup issues occur.

✅ Clean Gradle build if build errors occur.

✅ Reset Metro cache when JavaScript changes are not reflected.

✅ Commit code frequently using Git.

---

# Interview Questions

### Which command creates a new React Native project?

```bash
npx @react-native-community/cli init MyApp
```

---

### Which command runs the Android app?

```bash
npx react-native run-android
```

---

### Which command starts Metro?

```bash
npx react-native start
```

---

### Which command checks connected Android devices?

```bash
adb devices
```

---

### Which command generates a Release AAB?

```bash
gradlew bundleRelease
```

---

### Which command checks the development environment?

```bash
npx react-native doctor
```

---

# Summary

These commands cover the most common tasks in React Native development, including project creation, dependency management, Android builds, Metro Bundler, debugging, Git, and environment verification. Keeping these commands handy will save time during daily development.
