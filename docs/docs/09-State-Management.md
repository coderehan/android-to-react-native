# 9. State Management

## What is State Management?

State Management is the process of storing, updating, and managing data inside an application.

Whenever data changes, the UI should automatically update.

Examples:

- Login Status
- User Profile
- Shopping Cart
- Theme (Dark/Light)
- Loading State
- API Response

---

# Android

Android provides multiple ways to manage state.

- mutableStateOf (Jetpack Compose)
- LiveData
- StateFlow
- SharedFlow
- ViewModel

Modern Android applications mostly use:

- ViewModel
- StateFlow

---

# React Native

React Native provides multiple ways to manage state.

- useState
- useReducer
- Context API
- Zustand
- Redux Toolkit
- MobX
- Recoil

Most production applications use:

- Zustand ⭐⭐⭐⭐⭐
- Redux Toolkit ⭐⭐⭐⭐⭐

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| mutableStateOf | useState |
| ViewModel | Custom Hook |
| LiveData | Context API |
| StateFlow | Zustand |
| SharedFlow | Event Emitter |
| Repository | Service |

---

# Local State

Local State is used when data belongs only to a single screen.

Example

- Counter
- TextField
- Checkbox

---

## Android

```kotlin
var count by remember {
    mutableStateOf(0)
}
```

---

## React Native

```tsx
const [count, setCount] = useState(0);
```

Whenever the value changes, the UI updates automatically.

---

# Updating State

Android

```kotlin
count++
```

---

React Native

```tsx
setCount(count + 1)
```

---

# Global State

Global State is shared across multiple screens.

Examples

- Logged-in User
- Shopping Cart
- App Theme
- Language
- Authentication Token

---

## Android

Usually managed using:

- ViewModel
- StateFlow
- Repository

---

## React Native

Usually managed using:

- Context API
- Zustand
- Redux Toolkit

---

# Context API

Built into React.

Useful for:

- Theme
- User
- Language
- Authentication

Small to Medium projects use Context API.

---

# Zustand

A lightweight state management library.

Very easy to learn.

Example

```
Store

↓

Screen A

↓

Screen B

↓

Screen C
```

All screens can access the same data.

Most developers prefer Zustand because it is simple and fast.

---

# Redux Toolkit

Best for:

- Large Applications
- Enterprise Apps
- Complex Business Logic

Example

```
Store

↓

Reducers

↓

Actions

↓

UI
```

Redux Toolkit has more boilerplate than Zustand.

---

# ViewModel vs Hook

Android

```
UI

↓

ViewModel

↓

Repository
```

---

React Native

```
Screen

↓

Custom Hook

↓

Service
```

A Custom Hook is similar to a ViewModel because it contains reusable business logic.

---

# State Flow

Android

```
StateFlow

↓

Collector

↓

UI Updates
```

---

React Native

```
State

↓

Re-render

↓

Updated UI
```

---

# Data Flow

Android

```
ViewModel

↓

StateFlow

↓

Compose UI
```

---

React Native

```
Hook

↓

useState

↓

Component
```

---

# When to Use What?

| Situation | Android | React Native |
|------------|----------|--------------|
| Screen State | mutableStateOf | useState |
| Shared State | StateFlow | Zustand |
| Theme | ViewModel | Context API |
| User Login | StateFlow | Zustand |
| Shopping Cart | StateFlow | Zustand |
| Enterprise Apps | ViewModel | Redux Toolkit |

---

# Best Practices

✅ Keep UI state inside the screen.

✅ Keep business logic outside the UI.

✅ Use Custom Hooks.

✅ Use Zustand for shared state.

✅ Avoid storing everything in global state.

---

# Interview Questions

### What is State?

State is data that can change during the application's lifetime.

---

### Which Hook manages state?

```
useState()
```

---

### What is similar to mutableStateOf?

```
useState()
```

---

### What is similar to ViewModel?

Custom Hook.

---

### Which library is recommended?

Zustand.

---

### When should Redux Toolkit be used?

For large enterprise applications with complex state management.

---

# Summary

State Management keeps the UI synchronized with data changes.

Android developers commonly use ViewModel and StateFlow.

React Native developers commonly use useState for local state and Zustand or Redux Toolkit for shared application state.
