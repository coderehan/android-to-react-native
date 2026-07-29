# 27. Debugging

## What is Debugging?

Debugging is the process of identifying, analyzing, and fixing issues in an application.

Examples

- App Crash
- API Failure
- UI Bug
- Memory Leak
- Performance Issue
- Navigation Error

Every production application requires good debugging practices.

---

# Android

Popular debugging tools

- Logcat ⭐⭐⭐⭐⭐
- Android Studio Debugger ⭐⭐⭐⭐⭐
- Network Inspector ⭐⭐⭐⭐☆
- Layout Inspector ⭐⭐⭐⭐☆
- Profiler ⭐⭐⭐⭐⭐

---

# React Native

Popular debugging tools

- Metro Bundler Logs ⭐⭐⭐⭐⭐
- React Native DevTools ⭐⭐⭐⭐⭐
- Flipper ⭐⭐⭐⭐⭐
- Chrome DevTools ⭐⭐⭐⭐☆
- Reactotron ⭐⭐⭐⭐☆

Most production applications use

- React Native DevTools
- Flipper

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Logcat | Metro Logs |
| Android Studio Debugger | React Native DevTools |
| Network Inspector | Flipper Network Plugin |
| Layout Inspector | React DevTools |
| Android Profiler | Flipper Performance |
| Timber | console.log() / Logger |

---

# Debugging Flow

```
Bug Report

↓

Reproduce Issue

↓

Check Logs

↓

Identify Root Cause

↓

Fix Code

↓

Test Again
```

---

# Metro Logs

Metro Bundler displays

- Console Logs
- Errors
- Warnings
- Build Information

Example

```typescript
console.log("User Logged In");
```

---

# React Native DevTools

Allows developers to inspect

- Components
- Props
- State
- Hooks

Very similar to inspecting the UI hierarchy.

---

# Flipper

Flipper is a powerful debugging platform.

Supports

- Network Inspection
- Database Inspection
- Layout Inspection
- Logs
- Performance Monitoring

Most production teams use Flipper.

---

# Network Debugging

Flow

```
API Request

↓

Axios

↓

Flipper

↓

Response

↓

UI
```

Useful for checking

- Headers
- Request Body
- Response Body
- Status Codes

---

# Console Logging

Useful for debugging

```typescript
console.log()

console.warn()

console.error()
```

Avoid excessive logging in production builds.

---

# Error Boundaries

Error Boundaries prevent the entire application from crashing due to a component error.

Flow

```
Component Error

↓

Error Boundary

↓

Fallback UI
```

---

# Source Maps

Source Maps help developers trace production errors back to the original source code.

Useful for

- Crash Reports
- Production Debugging

---

# Common Errors

Examples

- Undefined Variable
- API Timeout
- Navigation Error
- Permission Denied
- Component Re-render Loop

---

# Debugging Architecture

```
Application

↓

Logs

↓

Debugger

↓

Identify Issue

↓

Fix

↓

Verify
```

---

# Folder Structure

```
src/

utils/

    Logger.ts

services/

hooks/

components/
```

---

# Best Practices

✅ Use meaningful log messages.

✅ Remove unnecessary logs before release.

✅ Use Flipper for network debugging.

✅ Handle errors gracefully.

✅ Test fixes on real devices.

---

# Interview Questions

### Which debugging tool is commonly used?

React Native DevTools.

---

### Which tool is similar to Logcat?

Metro Logs.

---

### Which tool is used for network debugging?

Flipper.

---

### Why use Error Boundaries?

To prevent the entire application from crashing due to component errors.

---

### Should console.log() be used in production?

No. Remove unnecessary logs before releasing the application.

---

# Real Project Example

Shopping App

```
User Reports Login Failure

↓

Check Metro Logs

↓

Inspect API

↓

Flipper Network

↓

401 Unauthorized

↓

Fix Token Issue

↓

Login Successful
```

---

# Summary

React Native provides several powerful debugging tools, including **Metro Logs**, **React Native DevTools**, and **Flipper**. Android developers can think of them as equivalents to **Logcat**, **Android Studio Debugger**, and **Network Inspector**, making it easier to diagnose crashes, API issues, and UI bugs.
