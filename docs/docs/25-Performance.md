# 25. Performance

## What is Performance?

Performance refers to how fast, smooth, and responsive an application feels.

A high-performance application should:

- Launch quickly
- Scroll smoothly
- Use less memory
- Consume less battery
- Avoid unnecessary re-renders

Popular Apps

- WhatsApp
- Instagram
- Amazon
- Flipkart
- Google Maps

---

# Android

Popular performance techniques

- RecyclerView ⭐⭐⭐⭐⭐
- DiffUtil ⭐⭐⭐⭐⭐
- Paging 3 ⭐⭐⭐⭐⭐
- ProGuard / R8 ⭐⭐⭐⭐⭐
- Baseline Profiles ⭐⭐⭐⭐☆

---

# React Native

Popular performance techniques

- FlatList ⭐⭐⭐⭐⭐
- React.memo ⭐⭐⭐⭐⭐
- useMemo ⭐⭐⭐⭐⭐
- useCallback ⭐⭐⭐⭐⭐
- Hermes Engine ⭐⭐⭐⭐⭐

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| RecyclerView | FlatList |
| LazyColumn | FlatList |
| DiffUtil | React.memo |
| Paging 3 | FlatList Pagination |
| ProGuard / R8 | Hermes |
| remember {} | useMemo |
| rememberUpdatedState | useCallback |

---

# Performance Flow

```
User Action

↓

Render UI

↓

Optimize Rendering

↓

Reduce Re-renders

↓

Smooth UI
```

---

# FlatList

FlatList renders only visible items.

Instead of loading

1000 Items

↓

Only visible items are rendered.

Very similar to RecyclerView.

---

# React.memo

React.memo prevents unnecessary component re-rendering.

Example

```
Parent Updated

↓

Child Props Same

↓

No Re-render
```

---

# useMemo

Caches expensive calculations.

Example

```
Filter List

↓

Cache Result

↓

Reuse Cached Data
```

Useful for

- Sorting
- Filtering
- Large Lists

---

# useCallback

Caches function references.

Useful when passing callbacks to child components.

Example

```
Button Click

↓

Same Function Reference

↓

Avoid Re-render
```

---

# Hermes

Hermes is the JavaScript engine optimized for React Native.

Advantages

- Faster App Startup
- Lower Memory Usage
- Smaller APK Size
- Better Performance

Most production applications enable Hermes.

---

# Image Optimization

Best Practices

- Compress Images
- Lazy Load Images
- Cache Images

Popular library

```
react-native-fast-image
```

---

# List Optimization

Use

```
FlatList
```

instead of

```
ScrollView
```

for long lists.

Why?

FlatList renders only visible items.

---

# Pagination

Instead of loading

```
1000 Products
```

Load

```
20 Products

↓

Next 20

↓

Next 20
```

Very similar to Paging 3 in Android.

---

# Avoid Unnecessary Re-renders

Bad

```
Parent Updated

↓

Every Child Re-render
```

Good

```
Parent Updated

↓

Only Changed Child Re-render
```

---

# Memory Optimization

Avoid

- Large Objects
- Unused Timers
- Memory Leaks
- Unused Event Listeners

Always clean up resources.

---

# Performance Architecture

```
Screen

↓

FlatList

↓

Memoized Components

↓

Optimized Rendering

↓

Smooth UI
```

---

# Folder Structure

```
src/

components/

hooks/

screens/

utils/

performance/
```

---

# Best Practices

✅ Use FlatList for large lists.

✅ Enable Hermes.

✅ Use React.memo.

✅ Use useMemo for expensive calculations.

✅ Use useCallback for callbacks.

✅ Compress and cache images.

✅ Remove unused listeners.

✅ Profile performance regularly.

---

# Interview Questions

### Which list component is commonly used?

FlatList.

---

### What is similar to RecyclerView?

FlatList.

---

### What is React.memo?

It prevents unnecessary component re-renders.

---

### What is useMemo?

It caches expensive calculations.

---

### What is useCallback?

It caches function references.

---

### Why use Hermes?

To improve startup time, memory usage, and overall application performance.

---

# Real Project Example

E-Commerce App

```
Product List

↓

FlatList

↓

Pagination

↓

React.memo

↓

Fast Image

↓

Smooth Scrolling
```

---

# Summary

React Native performance can be significantly improved by using FlatList for large datasets, React.memo to reduce unnecessary re-renders, useMemo and useCallback for memoization, and Hermes for faster JavaScript execution. Android developers can think of these optimizations as the React Native equivalents of RecyclerView, DiffUtil, Paging 3, and ProGuard/R8.
