# 31. React Native Interview Questions

This document contains commonly asked React Native interview questions for Beginner, Intermediate, and Senior developers.

---

# Beginner Level

## 1. What is React Native?

React Native is a framework developed by Meta for building cross-platform mobile applications using JavaScript or TypeScript and React.

---

## 2. Why use React Native?

- Single codebase
- Android + iOS support
- Faster development
- Large community
- Hot Reload

---

## 3. React Native vs Native Android?

Android

- Kotlin
- Java

React Native

- JavaScript
- TypeScript

Android

Separate codebase.

React Native

Single codebase.

---

## 4. What languages are used?

- JavaScript
- TypeScript

---

## 5. What is JSX?

JSX is a syntax that allows writing UI using JavaScript.

Similar to XML in Android.

---

## 6. What is a Component?

A reusable UI block.

Examples

- Button
- Card
- Toolbar
- Product Item

---

## 7. Difference between Functional and Class Components?

Today almost all React Native applications use Functional Components.

---

## 8. What is State?

State stores data that changes during runtime.

---

## 9. What are Props?

Props are values passed from a parent component to a child component.

---

## 10. What is Hot Reload?

It updates UI instantly without rebuilding the application.

---

# Intermediate Level

## 11. Which navigation library is commonly used?

React Navigation.

---

## 12. Which networking library is commonly used?

Axios.

---

## 13. Which state management library do you prefer?

Zustand.

---

## 14. Which database is commonly used?

WatermelonDB.

---

## 15. Which local storage is commonly used?

MMKV.

---

## 16. Which image loading library is commonly used?

FastImage.

---

## 17. Which camera library is commonly used?

Vision Camera.

---

## 18. Which maps library is commonly used?

react-native-maps.

---

## 19. Which notification library is commonly used?

Firebase Messaging + Notifee.

---

## 20. Which animation library is commonly used?

Reanimated.

---

## 21. Which permission library is commonly used?

react-native-permissions.

---

## 22. What is FlatList?

A high-performance list component that renders only visible items.

Similar to RecyclerView.

---

## 23. Why use React.memo?

To avoid unnecessary component re-renders.

---

## 24. Difference between useMemo and useCallback?

useMemo

Caches values.

useCallback

Caches functions.

---

## 25. What is Hermes?

A JavaScript engine optimized for React Native.

---

## 26. What is AsyncStorage?

Simple key-value storage.

---

## 27. What is MMKV?

A high-performance key-value storage library.

---

## 28. What is WatermelonDB?

A high-performance offline database.

---

## 29. What is Deep Linking?

Opening a specific screen using a URL or notification.

---

## 30. What is Context API?

A built-in way to share data across components.

---

# Senior Level

## 31. Explain React Native Architecture.

A production application is generally organized into:

- UI
- Navigation
- State Management
- Business Logic
- Networking
- Local Database
- Storage

---

## 32. How do you optimize performance?

- FlatList
- React.memo
- useMemo
- useCallback
- Hermes
- Image Caching

---

## 33. How do you handle API failures?

- Retry
- Error UI
- Timeout
- Offline Support
- Logging

---

## 34. How do you implement authentication?

- JWT Token
- Secure Storage
- Refresh Token
- Auto Login

---

## 35. How do you secure sensitive data?

- MMKV Encryption
- Secure Storage
- HTTPS
- Token Expiry

---

## 36. How do you support offline mode?

- WatermelonDB
- MMKV
- Cached API
- Background Sync

---

## 37. How do you reduce app startup time?

- Enable Hermes
- Lazy Loading
- Optimize Images
- Reduce Bundle Size

---

## 38. Explain CI/CD.

Automatically

- Build
- Test
- Deploy

using GitHub Actions, Fastlane, or Codemagic.

---

## 39. Which debugging tools do you use?

- Flipper
- React Native DevTools
- Metro Logs

---

## 40. Which testing libraries do you use?

- Jest
- React Native Testing Library
- Detox

---

# Scenario-Based Questions

## 41. How would you build an E-Commerce app?

- React Navigation
- Zustand
- Axios
- TanStack Query
- FastImage
- WatermelonDB

---

## 42. How would you build WhatsApp?

- WebSockets
- Zustand
- MMKV
- Vision Camera
- Push Notifications

---

## 43. How would you build Uber?

- react-native-maps
- Geolocation
- Background Tasks
- Push Notifications

---

## 44. How would you build Instagram?

- FastImage
- FlatList
- Reanimated
- Camera
- Infinite Scroll

---

## 45. How would you build a Banking App?

- Secure Storage
- Biometric Authentication
- HTTPS
- JWT
- Certificate Pinning

---

# Android Developer Questions

## 46. What is Retrofit in React Native?

Axios.

---

## 47. What is Room in React Native?

WatermelonDB.

---

## 48. What is SharedPreferences in React Native?

AsyncStorage or MMKV.

---

## 49. What is RecyclerView in React Native?

FlatList.

---

## 50. What is ViewModel in React Native?

Usually Zustand or Context API manages application state.

---

# Quick Revision

| Android | React Native |
|----------|--------------|
| Retrofit | Axios |
| Room | WatermelonDB |
| SharedPreferences | MMKV |
| RecyclerView | FlatList |
| ViewModel | Zustand |
| LiveData | Zustand |
| StateFlow | Zustand |
| Hilt | Context API |
| Coil | FastImage |
| CameraX | Vision Camera |
| Google Maps | react-native-maps |
| WorkManager | Background Fetch |
| MotionLayout | Reanimated |
| JUnit | Jest |
| Espresso | React Native Testing Library |
| Logcat | Metro Logs |

---

# Summary

React Native interviews usually focus on components, hooks, navigation, state management, networking, performance optimization, architecture, testing, debugging, and production best practices. If you already have Android experience, understanding the equivalent React Native concepts makes interview preparation much easier.
