# 17. Architecture

## What is Architecture?

Architecture defines how different parts of an application communicate with each other.

A good architecture makes an application:

- Easy to maintain
- Easy to test
- Easy to scale
- Easy to understand

---

# Android

Most modern Android applications use:

- MVVM
- Clean Architecture

Layers

- Presentation
- Domain
- Data

---

# React Native

React Native does not enforce any architecture.

The most common architecture is:

- Component-Based Architecture
- MVVM-like Architecture
- Feature-Based Architecture

Large production apps usually combine all three.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Activity | Screen |
| Fragment | Screen |
| ViewModel | Custom Hook |
| Repository | Service |
| Retrofit | Axios |
| Room | SQLite / WatermelonDB |
| Hilt | Context / DI Library |
| StateFlow | Zustand |

---

# Android Architecture

```
UI

↓

ViewModel

↓

Repository

↓

Remote API / Local Database
```

---

# React Native Architecture

```
Screen

↓

Custom Hook

↓

Service

↓

Axios / Database

↓

Backend API
```

---

# Recommended Folder Structure

```
src/

├── assets/
│
├── components/
│
├── screens/
│
├── hooks/
│
├── services/
│
├── repository/
│
├── navigation/
│
├── models/
│
├── storage/
│
├── database/
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

# Presentation Layer

Responsible for:

- UI
- User Interaction
- Showing Data

Contains

- Screens
- Components

Android

```
Activity

Fragment

Compose
```

React Native

```
Screen

Component
```

---

# Business Logic Layer

Responsible for:

- Business Rules
- Validation
- UI State

Android

```
ViewModel
```

React Native

```
Custom Hook
```

Example

```
useLogin()

useProducts()

useProfile()
```

---

# Data Layer

Responsible for:

- API Calls
- Database
- Local Storage

Contains

- Services
- Repository
- Database

---

# Networking Layer

```
Axios

↓

REST API

↓

JSON

↓

Models
```

---

# Local Storage Layer

```
MMKV

↓

User Settings

↓

Theme

↓

Language

↓

Token
```

---

# Database Layer

```
SQLite

↓

Repository

↓

Offline Data
```

---

# Complete Flow

```
User Click

↓

Screen

↓

Hook

↓

Service

↓

Axios

↓

Backend

↓

Response

↓

Hook

↓

State Update

↓

UI Re-render
```

---

# Offline Flow

```
Internet Available

↓

Fetch API

↓

Save Database

↓

Display UI

↓

Offline

↓

Load Database

↓

Display Cached Data
```

---

# Login Flow

```
Login Screen

↓

useLogin()

↓

AuthService

↓

Axios

↓

Backend

↓

Receive Token

↓

MMKV

↓

Home Screen
```

---

# Product Listing Flow

```
Home Screen

↓

useProducts()

↓

ProductService

↓

Axios

↓

Backend

↓

Product List

↓

FlatList
```

---

# Folder Responsibilities

## screens/

Contains application screens.

Examples

- HomeScreen
- LoginScreen
- ProfileScreen

---

## components/

Reusable UI.

Examples

- Button
- Toolbar
- Loader
- Card

---

## hooks/

Business logic.

Examples

- useLogin
- useProducts
- useCart

---

## services/

API calls.

Examples

- UserService
- AuthService
- ProductService

---

## repository/

Combines

- API
- Database
- Cache

---

## models/

TypeScript interfaces.

---

## database/

SQLite

WatermelonDB

---

## storage/

MMKV

AsyncStorage

Keychain

---

## navigation/

React Navigation

---

## utils/

Utility functions.

---

## constants/

App constants.

---

## theme/

Colors

Typography

Spacing

---

# Architecture Comparison

| Layer | Android | React Native |
|--------|----------|--------------|
| UI | Compose | Components |
| Screen | Activity / Fragment | Screen |
| Business Logic | ViewModel | Custom Hook |
| State | StateFlow | Zustand |
| API | Retrofit | Axios |
| Local Storage | DataStore | MMKV |
| Database | Room | SQLite / WatermelonDB |
| Dependency Injection | Hilt | Context / DI Library |

---

# Best Practices

✅ Keep UI free from business logic.

✅ Keep API calls inside Services.

✅ Use Custom Hooks for business logic.

✅ Reuse Components.

✅ Keep folder structure feature-based.

✅ Use TypeScript.

✅ Use Zustand for shared state.

✅ Keep storage and database separate.

---

# Interview Questions

### Which architecture is commonly used in React Native?

Component-Based Architecture with a clear separation of UI, business logic, and data.

---

### What is similar to ViewModel?

Custom Hook.

---

### What is similar to Repository?

Service or Repository.

---

### Where should API calls be written?

Inside the Service layer.

---

### Where should business logic be written?

Inside Custom Hooks.

---

### Why should UI and business logic be separated?

To improve maintainability, testing, and scalability.

---

# Real Project Example

Flipkart Cricket World Cup App

```
PointsTableScreen

↓

usePointsTable()

↓

PointsService

↓

Axios

↓

API

↓

Response

↓

FlatList
```

If offline support is required:

```
PointsTableScreen

↓

usePointsTable()

↓

Repository

↓

SQLite

↓

Cached Data
```

---

# Summary

A production-ready React Native application separates UI, business logic, and data access into independent layers. Android developers can think of this architecture as a simplified version of MVVM + Clean Architecture, where **Screens** replace Activities, **Custom Hooks** replace ViewModels, **Services** replace Repositories for network operations, and **Axios** replaces Retrofit.
