# 2. IDE (Integrated Development Environment)

## What is an IDE?

An IDE (Integrated Development Environment) is the software developers use to write, build, run, debug, and test applications.

---

# Android

The official IDE for Android development is:

- Android Studio ⭐⭐⭐⭐⭐

It is built on IntelliJ IDEA and provides everything needed to develop Android applications.

Features:

- Kotlin & Java support
- XML Editor
- Jetpack Compose Preview
- Layout Inspector
- Logcat
- Device Manager
- Profiler
- APK Analyzer
- Gradle Integration
- Emulator

---

# React Native

The most commonly used editor is:

- Visual Studio Code (VS Code) ⭐⭐⭐⭐⭐

VS Code is lightweight, fast, and highly customizable through extensions.

Features:

- JavaScript & TypeScript support
- IntelliSense
- Integrated Terminal
- Debugger
- Git Integration
- Extension Marketplace
- React Native Support

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Android Studio | VS Code |
| IntelliJ | VS Code |
| Gradle Integration | npm Integration |
| Logcat | Metro Logs |
| Device Manager | Android Studio Emulator |
| Profiler | Flipper / React DevTools |

---

# Recommended Extensions for React Native

## 1. React Native Tools

Used for:

- Running apps
- Debugging
- Launch Configuration

⭐⭐⭐⭐⭐ Recommended

---

## 2. ESLint

Used for:

- Finding code issues
- Maintaining clean code

⭐⭐⭐⭐⭐ Recommended

---

## 3. Prettier

Used for:

- Auto formatting code
- Maintaining consistent coding style

⭐⭐⭐⭐⭐ Recommended

---

## 4. Error Lens

Displays errors directly inside the editor.

⭐⭐⭐⭐⭐ Recommended

---

## 5. GitLens

Provides advanced Git features.

Useful for:

- Blame
- Commit History
- Code Authors

⭐⭐⭐⭐⭐ Recommended

---

## 6. Material Icon Theme

Provides beautiful folder and file icons.

⭐⭐⭐⭐⭐ Recommended

---

## 7. Path Intellisense

Auto-completes file paths while importing files.

⭐⭐⭐⭐⭐ Recommended

---

# Android Studio vs VS Code

## Android Studio

Pros

- Complete Android Development Environment
- Excellent Debugging
- Compose Preview
- Profiler
- Emulator

Cons

- Heavy Memory Usage
- Slower Startup

---

## VS Code

Pros

- Lightweight
- Fast
- Highly Customizable
- Huge Extension Ecosystem

Cons

- Requires installing extensions
- Native Android debugging is more limited

---

# Keyboard Shortcuts

| Action | Android Studio | VS Code |
|----------|---------------|---------|
| Search Everywhere | Shift Shift | Ctrl + P |
| Find in Project | Ctrl + Shift + F | Ctrl + Shift + F |
| Rename Symbol | Shift + F6 | F2 |
| Quick Fix | Alt + Enter | Ctrl + . |
| Format Code | Ctrl + Alt + L | Shift + Alt + F |
| Terminal | Alt + F12 | Ctrl + ` |

---

# Terminal

Android Studio

Uses Gradle commands.

Example

```bash
./gradlew assembleDebug
```

VS Code

Uses Node.js commands.

Example

```bash
npm install

npx react-native run-android
```

---

# Debugging

Android

- Breakpoints
- Logcat
- Profiler
- Layout Inspector

React Native

- VS Code Debugger
- React Native DevTools
- Flipper
- Console Logs

---

# Best Choice

## Android Development

✅ Android Studio

---

## React Native Development

✅ VS Code

---

# Key Points

- Android Studio is the official IDE for Android development.
- VS Code is the most popular editor for React Native.
- Both support debugging, Git integration, and extensions.
- VS Code becomes very powerful with the right extensions.

---

# Interview Questions

### Which IDE is commonly used for React Native development?

Visual Studio Code.

---

### Can Android Studio be used for React Native?

Yes.

Android Studio is commonly used for:

- Android Emulator
- Logcat
- Gradle
- Native Android Code

while VS Code is used for writing React Native code.

---

### Why is VS Code preferred for React Native?

Because it is lightweight, fast, and has excellent support for JavaScript and TypeScript through extensions.

---

# Summary

Android developers mainly use **Android Studio**, while React Native developers primarily use **VS Code**. In real-world React Native development, it's common to use **both**:

- VS Code → Write React Native code
- Android Studio → Emulator, Logcat, Gradle, Native Android code
