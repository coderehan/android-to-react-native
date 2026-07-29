# 30. Best Libraries

This document lists the most popular libraries used in React Native and compares them with their Android equivalents.

---

# Networking

| Android | React Native |
|----------|--------------|
| Retrofit | Axios |
| Ktor | Fetch API / Axios |
| OkHttp | Fetch API |
| Gson | JSON.parse() |
| Moshi | JSON.parse() |

---

# Dependency Injection

| Android | React Native |
|----------|--------------|
| Hilt | React Context API |
| Dagger | InversifyJS |
| Koin | React Context API |

---

# Navigation

| Android | React Native |
|----------|--------------|
| Navigation Component | React Navigation |
| Safe Args | React Navigation Params |

---

# UI

| Android | React Native |
|----------|--------------|
| XML | JSX |
| Jetpack Compose | React Native Components |
| Material Components | React Native Paper |

---

# Image Loading

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
| EncryptedSharedPreferences | react-native-encrypted-storage |

---

# Database

| Android | React Native |
|----------|--------------|
| Room | WatermelonDB |
| SQLite | react-native-sqlite-storage |
| Realm | Realm |

---

# API State

| Android | React Native |
|----------|--------------|
| Repository | Service Layer |
| ViewModel | Zustand Store |
| LiveData | Zustand |
| StateFlow | Zustand |

---

# State Management

| Android | React Native |
|----------|--------------|
| ViewModel | Zustand |
| LiveData | Zustand |
| StateFlow | Zustand |
| SavedStateHandle | Zustand Persist |

---

# Background Tasks

| Android | React Native |
|----------|--------------|
| WorkManager | react-native-background-fetch |
| Foreground Service | react-native-background-actions |
| AlarmManager | Background Fetch |

---

# Camera

| Android | React Native |
|----------|--------------|
| CameraX | Vision Camera |
| Camera2 API | Vision Camera |
| ML Kit | Vision Camera + Frame Processors |

---

# Maps

| Android | React Native |
|----------|--------------|
| Google Maps SDK | react-native-maps |
| Fused Location Provider | react-native-geolocation-service |

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

# Push Notifications

| Android | React Native |
|----------|--------------|
| Firebase Cloud Messaging | @react-native-firebase/messaging |
| NotificationManager | Notifee |

---

# Animations

| Android | React Native |
|----------|--------------|
| MotionLayout | Reanimated |
| Property Animation | Animated API |
| Lottie | Lottie React Native |

---

# Gestures

| Android | React Native |
|----------|--------------|
| GestureDetector | Gesture Handler |

---

# Performance

| Android | React Native |
|----------|--------------|
| RecyclerView | FlatList |
| LazyColumn | FlatList |
| DiffUtil | React.memo |
| Paging 3 | FlatList Pagination |
| ProGuard / R8 | Hermes |

---

# Testing

| Android | React Native |
|----------|--------------|
| JUnit | Jest |
| Mockito | Jest Mock |
| Espresso | React Native Testing Library |
| Instrumentation Tests | Detox |
| JaCoCo | Jest Coverage |

---

# Debugging

| Android | React Native |
|----------|--------------|
| Logcat | Metro Logs |
| Android Studio Debugger | React Native DevTools |
| Network Inspector | Flipper |
| Layout Inspector | React DevTools |

---

# File Handling

| Android | React Native |
|----------|--------------|
| File API | react-native-fs |
| DownloadManager | react-native-fs |

---

# Deep Linking

| Android | React Native |
|----------|--------------|
| Intent Filter | React Navigation Linking |

---

# Environment Variables

| Android | React Native |
|----------|--------------|
| BuildConfig | react-native-config |

---

# Build System

| Android | React Native |
|----------|--------------|
| Gradle | Gradle + Xcode |
| APK | APK |
| AAB | AAB |
| ProGuard | Hermes |

---

# CI/CD

| Android | React Native |
|----------|--------------|
| GitHub Actions | GitHub Actions |
| Jenkins | Jenkins |
| Fastlane | Fastlane |
| Bitrise | Bitrise |
| GitLab CI | GitLab CI |
| CircleCI | CircleCI |
| Codemagic | Codemagic |

---

# Useful React Native Libraries

| Purpose | Library |
|----------|---------|
| Networking | Axios |
| Navigation | React Navigation |
| State Management | Zustand |
| API Caching | TanStack Query |
| Local Storage | MMKV |
| Database | WatermelonDB |
| Image Loading | FastImage |
| Camera | Vision Camera |
| Maps | react-native-maps |
| Permissions | react-native-permissions |
| Notifications | Notifee |
| Firebase | React Native Firebase |
| Animations | Reanimated |
| Gestures | Gesture Handler |
| Bottom Sheet | @gorhom/bottom-sheet |
| Icons | react-native-vector-icons |
| Charts | react-native-svg-charts |
| Date Picker | react-native-date-picker |
| File Handling | react-native-fs |
| PDF | react-native-pdf |
| WebView | react-native-webview |
| QR Scanner | Vision Camera |
| Environment Variables | react-native-config |

---

# Recommended Stack for Production Apps

Frontend

- React Native
- TypeScript

State Management

- Zustand

Networking

- Axios

API Caching

- TanStack Query

Navigation

- React Navigation

Dependency Injection

- React Context API

Image Loading

- FastImage

Database

- WatermelonDB

Local Storage

- MMKV

Notifications

- Firebase + Notifee

Camera

- Vision Camera

Maps

- react-native-maps

Animations

- Reanimated

Permissions

- react-native-permissions

Testing

- Jest
- React Native Testing Library
- Detox

CI/CD

- GitHub Actions
- Fastlane

---

# Summary

If you already know Android development, React Native will feel very familiar because almost every Android concept has an equivalent library or framework. This guide serves as a quick reference for choosing the right libraries when building production-ready React Native applications.
