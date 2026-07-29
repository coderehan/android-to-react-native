# 29. Build and Release

## What is Build and Release?

Building an application converts the source code into an installable application.

Release is the process of publishing the application to users.

Android

- APK
- AAB

iOS

- IPA

---

# Android

Build System

- Gradle

Build Types

- Debug
- Release

Artifacts

- APK
- AAB

---

# React Native

Build System

- Gradle (Android)
- Xcode (iOS)

Build Types

- Debug
- Release

Artifacts

- APK
- AAB
- IPA

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Gradle | Gradle + Xcode |
| APK | APK |
| AAB | AAB |
| Debug Build | Debug Build |
| Release Build | Release Build |
| Keystore | Keystore + Apple Certificate |

---

# Build Flow

```
Write Code

↓

Run Tests

↓

Build Release

↓

Generate APK / AAB / IPA

↓

Upload Store
```

---

# Debug Build

Used during development.

Advantages

- Fast Build
- Debugging Enabled
- Metro Connected
- Hot Reload

Not suitable for production.

---

# Release Build

Optimized for production.

Advantages

- Smaller Size
- Better Performance
- Optimized Code
- No Debugging

Ready for Play Store and App Store.

---

# APK

Android Package

Suitable for

- Testing
- Internal Sharing
- Manual Installation

Example

```
app-release.apk
```

---

# AAB

Android App Bundle

Recommended by Google Play.

Advantages

- Smaller Download Size
- Optimized for Each Device
- Dynamic Delivery

Most production applications upload AAB files.

---

# IPA

iOS application package.

Used for

- TestFlight
- App Store

Example

```
MyApp.ipa
```

---

# Build Variants

Common variants

```
Debug

QA

Staging

Production
```

Each environment can use different

- API URL
- App Name
- App Icon
- Firebase Project

---

# Versioning

Every release contains

Version Name

Example

```
1.2.0
```

Version Code

Example

```
120
```

Increase the version before every release.

---

# App Signing

Android

Uses

```
Keystore
```

Without signing,

↓

Cannot publish to Play Store.

---

# iOS Signing

Uses

- Apple Certificate
- Provisioning Profile

Required for App Store release.

---

# Hermes

Enable Hermes in Release builds.

Advantages

- Faster Startup
- Lower Memory
- Better Performance

---

# Build Commands

Android Debug

```bash
npx react-native run-android
```

---

Android Release APK

```bash
cd android

gradlew assembleRelease
```

---

Android Release AAB

```bash
cd android

gradlew bundleRelease
```

---

iOS Release

```bash
npx react-native run-ios --configuration Release
```

---

# Build Output

Android APK

```
android/app/build/outputs/apk/release/
```

---

Android AAB

```
android/app/build/outputs/bundle/release/
```

---

# Release Checklist

Before releasing

✅ Update Version

✅ Run Tests

✅ Remove Debug Logs

✅ Enable Hermes

✅ Verify Environment Variables

✅ Test Release Build

✅ Sign Application

---

# Release Pipeline

```
Developer

↓

GitHub

↓

CI/CD

↓

Run Tests

↓

Generate Release Build

↓

Sign App

↓

Play Store

↓

Users
```

---

# Folder Structure

```
android/

ios/

fastlane/

.github/

workflows/
```

---

# Best Practices

✅ Always test Release builds.

✅ Upload AAB instead of APK.

✅ Keep Keystore secure.

✅ Increment version before release.

✅ Remove debug code.

✅ Automate releases using Fastlane.

---

# Interview Questions

### What is the difference between Debug and Release?

Debug builds are for development and include debugging tools.

Release builds are optimized for production.

---

### What is an APK?

An Android application package used for installation.

---

### What is an AAB?

Android App Bundle used for Play Store distribution.

---

### Why is app signing required?

To verify the authenticity of the application before publishing.

---

### Why use Hermes?

To improve startup time and reduce memory usage.

---

# Real Project Example

Shopping App

```
Developer

↓

GitHub Actions

↓

Run Tests

↓

Generate AAB

↓

Fastlane

↓

Google Play

↓

Users
```

---

# Summary

React Native applications are built using Gradle for Android and Xcode for iOS. Production releases typically generate an Android App Bundle (AAB) for Google Play and an IPA for the Apple App Store. Release builds should be signed, optimized with Hermes, tested thoroughly, and deployed using automated CI/CD pipelines whenever possible.
