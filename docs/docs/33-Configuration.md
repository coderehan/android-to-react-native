# 33. Configuration

## What is Configuration?

Configuration defines how an application behaves during development and production.

Examples

- App Name
- Package Name
- App Icon
- Splash Screen
- Firebase
- Permissions
- Build Settings

Without proper configuration, the application cannot run correctly.

---

# Android

Important configuration files

- AndroidManifest.xml
- build.gradle
- settings.gradle
- gradle.properties
- google-services.json

---

# React Native

Important configuration files

- package.json
- app.json
- android/
- ios/
- babel.config.js
- metro.config.js
- react-native.config.js

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| AndroidManifest.xml | AndroidManifest.xml (inside android folder) |
| build.gradle | build.gradle |
| settings.gradle | settings.gradle |
| google-services.json | google-services.json |
| Info.plist (iOS equivalent) | Info.plist |

---

# package.json

This is one of the most important files.

Contains

- Project Name
- Scripts
- Dependencies
- Versions

Example

```
npm install

↓

Updates package.json
```

---

# app.json

Stores application information.

Examples

- App Name
- Display Name

---

# Android Folder

Contains all Android native code.

```
android/

    app/

    gradle/

    build.gradle

    AndroidManifest.xml
```

---

# iOS Folder

Contains all iOS native code.

```
ios/

    AppDelegate

    Info.plist

    Xcode Project
```

---

# AndroidManifest.xml

Used for

- Permissions
- Activities
- Deep Links
- Services

Exactly the same as Android development.

---

# build.gradle

Used for

- SDK Version
- Dependencies
- Build Types
- Signing
- Build Variants

Exactly the same as Android.

---

# babel.config.js

Babel converts modern JavaScript into code supported by different JavaScript engines.

Typical Flow

```
Modern JavaScript

↓

Babel

↓

Compatible JavaScript
```

---

# metro.config.js

Metro is the JavaScript bundler.

Used for

- Bundling
- Asset Configuration
- Custom Transformers

Very similar to Gradle's build process for JavaScript assets.

---

# react-native.config.js

Used for configuring native modules.

Examples

- Fonts
- Assets
- Native Libraries

---

# Firebase Configuration

Android

```
google-services.json
```

iOS

```
GoogleService-Info.plist
```

Required for

- Firebase Auth
- Crashlytics
- Analytics
- Cloud Messaging

---

# Application Icons

Android

```
mipmap/
```

iOS

```
Assets.xcassets
```

---

# Splash Screen

Common libraries

- react-native-bootsplash
- react-native-splash-screen

Used to display a loading screen while the app starts.

---

# Build Variants

Common environments

```
Development

QA

Staging

Production
```

Each can have

- Different API URL
- Different App Icon
- Different App Name

---

# Configuration Flow

```
Project Starts

↓

Read Config Files

↓

Initialize App

↓

Load Services

↓

Application Ready
```

---

# Folder Structure

```
project/

package.json

app.json

babel.config.js

metro.config.js

react-native.config.js

android/

ios/
```

---

# Best Practices

✅ Keep configuration organized.

✅ Separate Development and Production settings.

✅ Use environment variables.

✅ Store Firebase configuration securely.

✅ Keep dependencies updated.

---

# Interview Questions

### Which file contains project dependencies?

package.json.

---

### Which file bundles JavaScript?

metro.config.js.

---

### Which file transpiles JavaScript?

babel.config.js.

---

### Where is AndroidManifest.xml?

Inside the android module.

---

### Which file stores Firebase configuration?

google-services.json.

---

### Where are Android native files located?

Inside the android folder.

---

# Real Project Example

Shopping App

```
package.json

↓

Install Dependencies

↓

Read Environment Variables

↓

Initialize Firebase

↓

Load Navigation

↓

Launch Home Screen
```

---

# Summary

React Native applications use configuration files such as **package.json**, **app.json**, **babel.config.js**, **metro.config.js**, and the native Android and iOS project files to control application behavior. Android developers will find many of these concepts familiar because the Android-specific configuration files remain part of every React Native project.
