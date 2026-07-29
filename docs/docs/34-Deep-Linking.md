# 34. Deep Linking

## What is Deep Linking?

Deep Linking allows an application to open a specific screen directly using a URL.

Examples

- Open Product Page
- Open Chat
- Open Order Details
- Open Payment Screen
- Reset Password

Popular Apps

- WhatsApp
- Amazon
- Flipkart
- Instagram
- Gmail

---

# Android

Deep Linking is implemented using

- Intent Filters
- App Links

---

# React Native

Deep Linking is implemented using

- React Navigation Linking
- Linking API

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Intent Filter | Linking API |
| App Links | Deep Linking |
| Intent | Linking |
| NavController.navigate() | navigation.navigate() |

---

# Deep Link Flow

```
User Clicks URL

↓

Operating System

↓

Open App

↓

Read URL

↓

Navigate Screen
```

---

# Example URL

```
myshop://product/1001
```

or

```
https://myshop.com/product/1001
```

Both URLs can open

```
Product Details Screen
```

---

# Common Use Cases

- Product Details
- Chat Screen
- Payment Screen
- User Profile
- Offers Page
- Password Reset
- Email Verification

---

# React Native Linking API

React Native provides

```
Linking
```

for handling incoming links.

Example

```typescript
import { Linking } from "react-native";
```

---

# React Navigation Linking

React Navigation supports Deep Linking.

Flow

```
Incoming URL

↓

Navigation Container

↓

Screen Mapping

↓

Open Screen
```

---

# Android Intent Filters

AndroidManifest.xml

```
URL

↓

Intent Filter

↓

Launch Activity
```

Very similar to Android native development.

---

# Universal Links

Used on iOS.

Advantages

- Opens App Directly
- Falls back to Website if App is not installed

---

# Android App Links

Used on Android.

Advantages

- Opens App Directly
- Verified Domain
- Better User Experience

---

# Notification Deep Linking

Flow

```
Push Notification

↓

User Taps Notification

↓

Read Payload

↓

Navigate Screen
```

Example

```
Order Delivered

↓

Order Details Screen
```

---

# Authentication Callback

Commonly used with

- Google Login
- Facebook Login
- OAuth Login

Flow

```
Browser

↓

Login Success

↓

Redirect URL

↓

Application

↓

Home Screen
```

---

# QR Code Deep Linking

Flow

```
Scan QR

↓

URL

↓

Open App

↓

Target Screen
```

---

# Deep Link Architecture

```
URL

↓

Linking

↓

Navigation

↓

Target Screen
```

---

# Folder Structure

```
src/

navigation/

services/

utils/

LinkingService.ts
```

---

# Best Practices

✅ Support both App Links and Universal Links.

✅ Validate incoming URLs.

✅ Handle invalid links gracefully.

✅ Test links on both Android and iOS.

✅ Support notifications and authentication callbacks.

---

# Interview Questions

### What is Deep Linking?

Opening a specific screen in the application using a URL.

---

### Which API handles Deep Linking?

Linking API.

---

### Which navigation library supports Deep Linking?

React Navigation.

---

### What is similar to Android Intent Filters?

React Native Linking.

---

### What is Universal Link?

An iOS feature that opens the app directly from a verified web link.

---

### What is Android App Link?

A verified Android URL that opens the app directly.

---

# Real Project Example

Shopping App

```
Email

↓

Click Product Link

↓

Open App

↓

Product Details Screen
```

---

# Summary

React Native supports Deep Linking using the **Linking API** together with **React Navigation**. Android developers can think of this as the equivalent of **Intent Filters** and **App Links**, allowing users to open specific screens directly from URLs, notifications, QR codes, emails, and authentication callbacks.
