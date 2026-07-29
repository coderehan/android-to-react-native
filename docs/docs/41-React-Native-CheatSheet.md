# React Native Cheat Sheet (Android Developer Edition)

> A quick reference for Android developers transitioning to React Native.

---

# Tech Stack

| Android | React Native |
|----------|--------------|
| Kotlin | TypeScript |
| Android Studio | VS Code |
| XML | JSX |
| Jetpack Compose | React Native Components |
| Activity | Screen |
| Fragment | Screen |

---

# Architecture

| Android | React Native |
|----------|--------------|
| MVVM | Component + Hooks + Zustand |
| Repository | Service Layer |
| ViewModel | Zustand Store |
| LiveData | Zustand |
| StateFlow | Zustand |
| Hilt | React Context API |
| Clean Architecture | Feature-Based Architecture |

---

# UI

| Android | React Native |
|----------|--------------|
| TextView | Text |
| EditText | TextInput |
| Button | Button / Pressable |
| ImageView | Image |
| RecyclerView | FlatList |
| ConstraintLayout | View + Flexbox |
| ScrollView | ScrollView |
| Toolbar | Header |
| Snackbar | Toast |
| BottomSheetDialog | @gorhom/bottom-sheet |

---

# Navigation

| Android | React Native |
|----------|--------------|
| Navigation Component | React Navigation |
| Safe Args | Route Params |
| Intent | navigation.navigate() |
| BackStack | Navigation Stack |

---

# Networking

| Android | React Native |
|----------|--------------|
| Retrofit | Axios |
| Ktor | Fetch / Axios |
| OkHttp | Fetch API |
| Gson | JSON.parse() |
| Moshi | JSON.parse() |

---

# Images

| Android | React Native |
|----------|--------------|
| Coil | FastImage |
| Glide | FastImage |
| Picasso | FastImage |

---

# Local Storage

| Android | React Native |
|----------|--------------|
| SharedPreferences | AsyncStorage |
| DataStore | MMKV |
| EncryptedSharedPreferences | Encrypted Storage |

---

# Database

| Android | React Native |
|----------|--------------|
| Room | WatermelonDB |
| SQLite | react-native-sqlite-storage |
| Realm | Realm |

---

# Authentication

| Android | React Native |
|----------|--------------|
| Firebase Auth | Firebase Auth |
| Google Sign In | Google Sign In |
| BiometricPrompt | react-native-biometrics |

---

# Permissions

| Android | React Native |
|----------|--------------|
| Permission APIs | react-native-permissions |

---

# Camera

| Android | React Native |
|----------|--------------|
| CameraX | Vision Camera |
| Camera2 | Vision Camera |

---

# Maps

| Android | React Native |
|----------|--------------|
| Google Maps SDK | react-native-maps |
| Fused Location | react-native-geolocation-service |

---

# Notifications

| Android | React Native |
|----------|--------------|
| Firebase Cloud Messaging | React Native Firebase |
| NotificationManager | Notifee |

---

# Background Work

| Android | React Native |
|----------|--------------|
| WorkManager | Background Fetch |
| Foreground Service | Background Actions |

---

# Animations

| Android | React Native |
|----------|--------------|
| MotionLayout | Reanimated |
| Property Animation | Animated API |
| Lottie | Lottie React Native |

---

# Testing

| Android | React Native |
|----------|--------------|
| JUnit | Jest |
| Mockito | Jest Mock |
| Espresso | React Native Testing Library |
| Instrumentation Test | Detox |

---

# Debugging

| Android | React Native |
|----------|--------------|
| Logcat | Metro Logs |
| Android Studio Debugger | React Native DevTools |
| Network Inspector | Flipper |
| Layout Inspector | React DevTools |

---

# Build

| Android | React Native |
|----------|--------------|
| Gradle | Gradle + Xcode |
| APK | APK |
| AAB | AAB |
| IPA | IPA |

---

# CI/CD

| Android | React Native |
|----------|--------------|
| GitHub Actions | GitHub Actions |
| Jenkins | Jenkins |
| Fastlane | Fastlane |
| Bitrise | Bitrise |
| Codemagic | Codemagic |

---

# Environment

| Android | React Native |
|----------|--------------|
| BuildConfig | react-native-config |
| Product Flavors | Multiple .env Files |

---

# Deep Linking

| Android | React Native |
|----------|--------------|
| Intent Filter | Linking API |
| App Links | Deep Linking |
| Intent | Linking |

---

# Offline First

| Android | React Native |
|----------|--------------|
| Room | WatermelonDB |
| WorkManager | Background Fetch |
| Repository | Service Layer |

---

# File Handling

| Android | React Native |
|----------|--------------|
| File API | react-native-fs |
| DownloadManager | react-native-fs |
| Storage Access Framework | Document Picker |
| Share Intent | react-native-share |

---

# Dependency Management

| Android | React Native |
|----------|--------------|
| Gradle | npm / Yarn |
| build.gradle | package.json |
| implementation() | npm install |

---

# Project Structure

```
src/

components/

screens/

navigation/

store/

services/

database/

hooks/

utils/

constants/

config/

theme/

assets/
```

---

# Production Stack

Programming Language

✔ TypeScript

Navigation

✔ React Navigation

State Management

✔ Zustand

Networking

✔ Axios

Caching

✔ TanStack Query

Image Loading

✔ FastImage

Database

✔ WatermelonDB

Local Storage

✔ MMKV

Camera

✔ Vision Camera

Maps

✔ react-native-maps

Animations

✔ Reanimated

Notifications

✔ React Native Firebase

✔ Notifee

Testing

✔ Jest

✔ React Native Testing Library

✔ Detox

CI/CD

✔ GitHub Actions

✔ Fastlane

---

# Most Used Commands

Create Project

```bash
npx @react-native-community/cli init MyApp
```

Run Android

```bash
npx react-native run-android
```

Start Metro

```bash
npx react-native start
```

Install Package

```bash
npm install axios
```

Check Environment

```bash
npx react-native doctor
```

Check Devices

```bash
adb devices
```

Generate Release APK

```bash
cd android

gradlew assembleRelease
```

Generate Release AAB

```bash
cd android

gradlew bundleRelease
```

---

# Interview Revision

Retrofit
→ Axios

Room
→ WatermelonDB

SharedPreferences
→ MMKV

RecyclerView
→ FlatList

ViewModel
→ Zustand

LiveData
→ Zustand

StateFlow
→ Zustand

Navigation Component
→ React Navigation

WorkManager
→ Background Fetch

Coil
→ FastImage

CameraX
→ Vision Camera

Google Maps
→ react-native-maps

JUnit
→ Jest

Espresso
→ React Native Testing Library

Logcat
→ Metro Logs

Hilt
→ React Context API

MotionLayout
→ Reanimated

BuildConfig
→ react-native-config

Gradle
→ npm + Gradle

APK
→ APK

AAB
→ AAB

---

# Learning Order

JavaScript

↓

TypeScript

↓

React

↓

React Native

↓

Components

↓

Navigation

↓

State Management

↓

Networking

↓

Storage

↓

Database

↓

Authentication

↓

Performance

↓

Testing

↓

CI/CD

↓

Build & Release

↓

System Design
