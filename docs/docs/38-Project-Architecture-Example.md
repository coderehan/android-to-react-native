# 38. Project Architecture Example

## Goal

Build a scalable, maintainable, and production-ready React Native application.

This architecture is suitable for

- E-Commerce
- Banking
- Food Delivery
- Social Media
- Healthcare
- Travel Apps

---

# Recommended Tech Stack

Programming Language

- TypeScript

UI

- React Native

Navigation

- React Navigation

State Management

- Zustand

Networking

- Axios

API Caching

- TanStack Query

Database

- WatermelonDB

Local Storage

- MMKV

Image Loading

- FastImage

Dependency Injection

- React Context API

Notifications

- Firebase + Notifee

Maps

- react-native-maps

Camera

- Vision Camera

Animations

- Reanimated

Testing

- Jest
- React Native Testing Library
- Detox

CI/CD

- GitHub Actions
- Fastlane

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Activity | Screen |
| Fragment | Screen |
| ViewModel | Zustand Store |
| Repository | Service |
| Retrofit | Axios |
| Room | WatermelonDB |
| SharedPreferences | MMKV |
| Navigation Component | React Navigation |

---

# Recommended Folder Structure

```
src/

    assets/

        images/

        icons/

        fonts/

    components/

        Button/

        Toolbar/

        Loader/

        Card/

    navigation/

        AppNavigator.tsx

        AuthNavigator.tsx

    screens/

        Home/

        Login/

        Product/

        Cart/

        Profile/

    services/

        ApiService.ts

        AuthService.ts

        ProductService.ts

    store/

        authStore.ts

        productStore.ts

        cartStore.ts

    database/

    hooks/

    utils/

    constants/

    config/

    theme/

    types/
```

---

# High-Level Architecture

```
UI (Screens)

↓

Navigation

↓

Zustand Store

↓

Service Layer

↓

Axios API

↓

Backend
```

---

# Offline Data Flow

```
UI

↓

Zustand

↓

WatermelonDB

↓

API

↓

Backend

↓

Update Database

↓

Refresh UI
```

---

# Authentication Flow

```
Login Screen

↓

Axios

↓

Backend

↓

JWT Token

↓

MMKV

↓

Home Screen
```

---

# Product Loading Flow

```
Home Screen

↓

Product Store

↓

Product Service

↓

Axios

↓

Backend

↓

WatermelonDB

↓

UI
```

---

# Cart Flow

```
Add To Cart

↓

Cart Store

↓

MMKV

↓

Cart Screen
```

---

# Profile Flow

```
Profile Screen

↓

Profile Service

↓

API

↓

Backend

↓

Update UI
```

---

# Notification Flow

```
Firebase

↓

Notifee

↓

Notification

↓

Open Screen
```

---

# Deep Link Flow

```
User Clicks Link

↓

React Navigation

↓

Product Screen
```

---

# Error Handling

```
API Error

↓

Service Layer

↓

Store

↓

UI

↓

Error Message
```

---

# Loading State

```
API Request

↓

Loading

↓

Success

↓

Display Data
```

---

# Build Flow

```
Developer

↓

GitHub

↓

CI/CD

↓

Tests

↓

Build

↓

Play Store

↓

Users
```

---

# Project Layers

## Presentation Layer

Contains

- Screens
- Components
- Navigation

Responsible for displaying UI.

---

## State Layer

Contains

- Zustand Stores

Responsible for managing application state.

---

## Service Layer

Contains

- API Calls
- Business Logic

Responsible for communicating with backend services.

---

## Data Layer

Contains

- WatermelonDB
- MMKV

Responsible for local storage and caching.

---

## Utilities

Contains

- Helpers
- Constants
- Validators
- Extensions

---

# Best Practices

✅ Keep screens simple.

✅ Move API calls to Service layer.

✅ Keep business logic outside UI.

✅ Use reusable components.

✅ Store tokens securely.

✅ Cache important data.

✅ Follow feature-based folder structure.

---

# Interview Questions

### Why use this architecture?

It keeps the project modular, scalable, and easy to maintain.

---

### Where should API calls be placed?

Inside the Service layer.

---

### Where should UI state be managed?

Inside Zustand Stores.

---

### Where should JWT tokens be stored?

MMKV (or encrypted secure storage if higher security is required).

---

### Where should cached data be stored?

WatermelonDB.

---

### Why avoid API calls inside UI?

To separate presentation from business logic, making the code easier to test and maintain.

---

# Real Project Example

Shopping App

```
Home Screen

↓

Product Store

↓

Product Service

↓

Axios

↓

Backend

↓

WatermelonDB

↓

Refresh Store

↓

Update UI
```

---

# Complete Architecture

```
                UI

                 ↓

          React Navigation

                 ↓

            Zustand Store

                 ↓

           Service Layer

        ↙               ↘

WatermelonDB         Axios API

        ↘               ↙

             Backend

                 ↓

          Refresh Store

                 ↓

                 UI
```

---

# Summary

A production React Native application is typically organized into Presentation, State, Service, and Data layers. Screens communicate with Zustand stores, which interact with services. Services fetch data using Axios, cache it in WatermelonDB when appropriate, and update the UI. This architecture is scalable, testable, and closely resembles Android's Clean Architecture with MVVM.
