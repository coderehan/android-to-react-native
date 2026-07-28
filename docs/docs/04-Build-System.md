# 4. Project Setup

## What is Project Setup?

Project setup means installing and configuring all the tools required to build and run a React Native application.

Unlike Android development, React Native requires both JavaScript and Android development tools.

---

# Android Setup

To start Android development, we usually install:

- Android Studio
- Android SDK
- JDK (Java Development Kit)
- Gradle

Once installed, we can create and run Android applications.

---

# React Native Setup

To start React Native development, we need:

- Node.js
- npm
- npx
- React Native CLI
- Android Studio
- Android SDK
- Java (JDK)
- Android SDK Platform Tools (ADB)

---

# Required Tools

## Node.js

Used to run JavaScript outside the browser.

Website:

https://nodejs.org

Example

```
node -v
```

---

## npm

Node Package Manager.

Used to install JavaScript libraries.

Example

```
npm install
```

---

## npx

Used to run packages without installing them globally.

Example

```
npx react-native run-android
```

---

## React Native CLI

Used to create and run React Native applications.

Create Project

```
npx @react-native-community/cli init MyApp
```

Run App

```
npx react-native run-android
```

---

## Android Studio

Used for

- Emulator
- Android SDK
- Logcat
- Native Android Code

---

## Android SDK

Contains

- Build Tools
- Platform Tools
- SDK Platforms
- Emulator

Typical Location

```
C:\Users\<Username>\AppData\Local\Android\Sdk
```

---

## ADB (Android Debug Bridge)

Used for communicating with Android devices.

Useful Commands

Check Version

```
adb version
```

Connected Devices

```
adb devices
```

Install APK

```
adb install app.apk
```

---

## Java (JDK)

React Native requires Java for building Android applications.

Check Version

```
java -version
```

---

# Metro Bundler

Metro is the JavaScript bundler used by React Native.

Responsibilities

- Bundles JavaScript
- Watches file changes
- Reloads the app automatically

Start Metro

```
npm start
```

or

```
npx react-native start
```

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Android Studio | VS Code |
| Gradle | npm |
| Gradle Dependencies | npm Packages |
| Java/Kotlin | TypeScript |
| APK Build | Metro + Gradle |
| Logcat | Metro Logs |

---

# Project Creation

Create a New Project

```
npx @react-native-community/cli init MyApp
```

Go Inside Project

```
cd MyApp
```

Run Android App

```
npx react-native run-android
```

Start Metro

```
npm start
```

---

# Environment Variables

React Native commonly uses:

ANDROID_HOME

Example

```
ANDROID_HOME=C:\Users\<Username>\AppData\Local\Android\Sdk
```

Useful Commands

```
echo %ANDROID_HOME%
```

```
adb version
```

```
node -v
```

```
npm -v
```

```
java -version
```

---

# Common Errors

## adb is not recognized

Reason

Platform Tools are not added to PATH.

Solution

Add

```
platform-tools
```

to Environment Variables.

---

## SDK location not found

Reason

Android SDK path is missing.

Solution

Set

```
ANDROID_HOME
```

or

```
local.properties
```

---

## npm or npx not recognized

Reason

Node.js is not installed correctly.

Solution

Reinstall Node.js and restart the terminal.

---

## PowerShell Execution Policy Error

Reason

PowerShell blocks script execution.

Solution

Use Command Prompt or change the PowerShell execution policy.

---

# Best Practices

✅ Install the latest LTS version of Node.js.

✅ Use TypeScript.

✅ Keep Android Studio updated.

✅ Verify ADB before running the app.

✅ Test on a real device whenever possible.

---

# Interview Questions

### Why do we need Node.js?

Node.js runs JavaScript outside the browser and powers the React Native development environment.

---

### What is npm?

npm is the package manager used to install JavaScript libraries.

---

### What is npx?

npx runs packages without requiring a global installation.

---

### What is Metro?

Metro is the JavaScript bundler used by React Native.

---

### Why is Android Studio still required?

Because React Native still builds a native Android application using Gradle, the Android SDK, and ADB.

---

# Summary

React Native development combines JavaScript tooling (Node.js, npm, Metro) with native Android tooling (Android Studio, SDK, Gradle, and ADB). Both environments work together to build and run Android applications.
