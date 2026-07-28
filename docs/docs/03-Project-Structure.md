# 3. Project Structure

## What is Project Structure?

Project Structure is the way source code is organized into folders and files.

A good project structure makes the application:

- Easy to understand
- Easy to maintain
- Easy to scale
- Easy for teams to work together

---

# Android Project Structure

A typical Android project looks like this:

```
app/
├── src/
│   ├── main/
│   │   ├── java/
│   │   ├── res/
│   │   └── AndroidManifest.xml
│   │
│   ├── test/
│   └── androidTest/
│
├── build.gradle
└── proguard-rules.pro
```

---

# Android (MVVM + Clean Architecture)

```
app/
│
├── presentation/
│   ├── screens/
│   ├── viewmodel/
│   └── components/
│
├── domain/
│   ├── model/
│   ├── repository/
│   └── usecase/
│
├── data/
│   ├── remote/
│   ├── local/
│   ├── repository/
│   └── mapper/
│
├── di/
├── utils/
└── core/
```

This structure is commonly used in production Android applications.

---

# React Native Project Structure

When you create a React Native project, you'll see:

```
MyApp/

├── android/
├── ios/
├── node_modules/
├── App.tsx
├── index.js
├── package.json
└── metro.config.js
```

---

## What do these folders mean?

### android/

Contains the complete native Android project.

Used for:

- Gradle
- Android Manifest
- Native Kotlin/Java code
- Permissions
- Signing
- APK/AAB Generation

---

### ios/

Contains the native iOS project.

Used for:

- Swift
- Objective-C
- Xcode
- iOS Build

---

### node_modules/

Contains all installed libraries.

Similar to Gradle dependencies in Android.

---

### package.json

Contains:

- Project Information
- Dependencies
- Scripts

Similar to:

```
build.gradle
```

in Android.

---

### App.tsx

This is the main screen of the application.

Similar to:

```
MainActivity
```

or

```
HomeScreen
```

in Android.

---

### index.js

Application Entry Point.

Similar to:

```
Application Class
```

or

```
MainActivity Launcher
```

---

# Recommended React Native Folder Structure

For production applications:

```
src/

├── assets/
│
├── components/
│
├── screens/
│
├── navigation/
│
├── services/
│
├── repository/
│
├── hooks/
│
├── context/
│
├── models/
│
├── constants/
│
├── utils/
│
├── theme/
│
└── types/
```

---

# Folder Explanation

## assets/

Stores:

- Images
- Icons
- Fonts
- JSON Files

---

## components/

Reusable UI components.

Example:

- Primary Button
- Toolbar
- Card
- Loader

Similar to:

Reusable Compose Components.

---

## screens/

Every application screen.

Example:

- Home Screen
- Login Screen
- Profile Screen

Similar to:

Activities or Fragments.

---

## navigation/

Contains navigation setup.

Example:

- Stack Navigation
- Bottom Tabs
- Drawer

Similar to:

Navigation Component.

---

## services/

Handles:

- API Calls
- Axios
- Business Services

Similar to:

Retrofit Service.

---

## repository/

Acts as a bridge between API and UI.

Similar to:

Repository Layer in Android.

---

## hooks/

Contains custom React Hooks.

Similar to:

ViewModel + Reusable Business Logic.

---

## context/

Global application state.

Similar to:

Shared ViewModel.

---

## models/

Contains data models.

Similar to:

data class.

---

## constants/

Stores:

- API URLs
- Keys
- App Constants

---

## utils/

Utility functions.

Example:

- Date Formatter
- Validators
- Extensions

---

## theme/

Stores:

- Colors
- Fonts
- Spacing

Similar to:

colors.xml

themes.xml

Typography

---

## types/

Contains:

- Interfaces
- Type Aliases

Similar to:

Model Interfaces.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Activity | Screen |
| Fragment | Screen |
| ViewModel | Hook |
| Repository | Repository |
| Retrofit | Service |
| Navigation Component | React Navigation |
| data class | Interface |
| build.gradle | package.json |
| AndroidManifest | app.json + AndroidManifest |
| Drawable | assets/images |

---

# Best Practices

✅ Keep business logic outside UI.

✅ Reuse components.

✅ Separate screens and components.

✅ Keep API code inside services.

✅ Keep reusable logic inside hooks.

✅ Store constants separately.

---

# Interview Questions

### Where should API calls be placed?

Inside the services layer.

---

### Where should reusable UI be placed?

Inside the components folder.

---

### Where should screens be placed?

Inside the screens folder.

---

### Where should reusable business logic be placed?

Inside custom hooks.

---

# Summary

A well-organized folder structure makes React Native projects easier to understand, maintain, and scale. Android developers will notice that most concepts have direct equivalents, even though the folder names may differ.
