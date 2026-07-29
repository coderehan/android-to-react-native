# 10. Lifecycle

## What is Lifecycle?

Lifecycle defines the different stages a screen or component goes through from the moment it is created until it is destroyed.

Examples:

- Screen opens
- User navigates to another screen
- Screen comes back
- Screen closes

---

# Android

Android provides lifecycle methods inside an Activity or Fragment.

Common lifecycle methods are:

- onCreate()
- onStart()
- onResume()
- onPause()
- onStop()
- onDestroy()

These methods help us initialize resources, load data, and clean up when the screen is destroyed.

---

# React Native

React Native does not have Activity or Fragment lifecycle methods.

Instead, it uses:

- useEffect()
- useFocusEffect()
- Component Mount
- Component Unmount

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| onCreate() | useEffect() |
| onStart() | Component Mount |
| onResume() | useFocusEffect() |
| onPause() | useFocusEffect() Cleanup |
| onStop() | Component Unmount |
| onDestroy() | useEffect() Cleanup |

---

# Component Lifecycle

React Native Component Lifecycle

```

Component Created

↓

Component Mounted

↓

State Updates

↓

Component Re-renders

↓

Component Unmounts

```

---

# useEffect()

useEffect() is one of the most important Hooks in React Native.

It is used for:

- API Calls
- Database Calls
- Event Listeners
- Timers
- Initial Setup

---

## Android

```kotlin
override fun onCreate() {
    super.onCreate()

    loadUsers()
}
```

---

## React Native

```tsx
useEffect(() => {
    loadUsers();
}, []);
```

The empty dependency array (`[]`) means the code runs only once when the component is mounted.

---

# Cleanup

Cleanup is used to release resources when the component is removed.

Examples:

- Remove Listeners
- Stop Timers
- Cancel API Requests
- Close Connections

---

Android

```kotlin
override fun onDestroy() {

}
```

---

React Native

```tsx
useEffect(() => {

    return () => {

    }

}, []);
```

The function returned by `useEffect()` is called when the component unmounts.

---

# Running on Every State Change

Android

```kotlin
StateFlow.collect {

}
```

---

React Native

```tsx
useEffect(() => {

}, [count]);
```

Whenever `count` changes, the effect runs again.

---

# Component Re-render

A component re-renders when:

- State changes
- Props change
- Context changes

Example

```tsx
setCount(count + 1)
```

Changing state automatically updates the UI.

---

# Screen Focus

Sometimes a screen stays in memory but becomes hidden.

When the user returns, we may want to refresh data.

React Navigation provides:

```
useFocusEffect()
```

This is similar to:

```
onResume()
```

in Android.

---

# Example

Android

```kotlin
override fun onResume() {

    loadData()

}
```

---

React Native

```tsx
useFocusEffect(

    React.useCallback(() => {

        loadData();

    }, [])

);
```

---

# Lifecycle Comparison

| Android | React Native |
|----------|--------------|
| onCreate() | useEffect() |
| onResume() | useFocusEffect() |
| onDestroy() | Cleanup Function |
| finish() | Component Unmount |
| ViewModel Cleared | Cleanup |

---

# Common Use Cases

## API Call

Android

```
onCreate()
```

React Native

```
useEffect()
```

---

## Remove Listener

Android

```
onDestroy()
```

React Native

```
Cleanup Function
```

---

## Refresh Screen

Android

```
onResume()
```

React Native

```
useFocusEffect()
```

---

# Best Practices

✅ Keep useEffect() focused on one responsibility.

✅ Always clean up listeners and timers.

✅ Avoid unnecessary re-renders.

✅ Use useFocusEffect() only when screen focus matters.

---

# Interview Questions

### What is useEffect()?

A Hook used to perform side effects like API calls, timers, and event listeners.

---

### What is similar to onCreate()?

```
useEffect(() => {}, [])
```

---

### What is similar to onResume()?

```
useFocusEffect()
```

---

### What is similar to onDestroy()?

The cleanup function returned from useEffect().

---

### When does a component re-render?

When:

- State changes
- Props change
- Context changes

---

# Summary

React Native uses Hooks instead of traditional lifecycle methods.

The most commonly used lifecycle Hooks are:

- useEffect()
- useFocusEffect()

Understanding these Hooks helps Android developers map familiar lifecycle concepts to React Native.
