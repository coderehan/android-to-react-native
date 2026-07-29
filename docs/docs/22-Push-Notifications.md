# 22. Push Notifications

## What are Push Notifications?

Push Notifications allow an application to send messages to users even when the application is closed.

Examples

- New Message
- Order Delivered
- Payment Successful
- Flash Sale
- Breaking News
- OTP Notification

Popular Apps

- WhatsApp
- Amazon
- Flipkart
- Swiggy
- Gmail

---

# Android

Popular notification technologies

- Firebase Cloud Messaging (FCM) ⭐⭐⭐⭐⭐
- NotificationManager ⭐⭐⭐⭐⭐
- Notification Channels ⭐⭐⭐⭐⭐

Most Android applications use:

- FCM

---

# React Native

Popular notification libraries

- @react-native-firebase/messaging ⭐⭐⭐⭐⭐
- Notifee ⭐⭐⭐⭐⭐

Most production applications use

- Firebase Messaging
- Notifee

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Firebase Cloud Messaging | @react-native-firebase/messaging |
| NotificationManager | Notifee |
| Notification Channel | Android Channel |
| PendingIntent | Deep Linking |
| BroadcastReceiver | Background Message Handler |

---

# Notification Flow

```
Backend

↓

Firebase Cloud Messaging

↓

Mobile Device

↓

Receive Notification

↓

Open App

↓

Navigate Screen
```

---

# Types of Notifications

### Push Notification

Sent from a backend server.

Example

```
Your order has been delivered.
```

---

### Local Notification

Created by the application itself.

Example

```
Medicine Reminder

10:00 AM
```

---

# Firebase Cloud Messaging

FCM sends notifications from the backend to Android and iOS devices.

Flow

```
Backend

↓

FCM

↓

Device

↓

Notification
```

---

# Device Token

Every device receives a unique FCM Token.

Flow

```
Install App

↓

Generate FCM Token

↓

Send Token

↓

Backend

↓

Save Database
```

The backend uses this token to send notifications.

---

# Foreground Notification

App is currently open.

```
User

↓

Notification Received

↓

Display Custom UI
```

---

# Background Notification

App is running in the background.

The operating system displays the notification automatically.

---

# Terminated App

Even if the app is completely closed,

FCM can still deliver notifications.

---

# Notification Channels (Android)

Android 8.0+

Notifications must belong to a channel.

Examples

```
Orders

Promotions

Messages

Payments
```

Users can enable or disable each channel separately.

---

# Deep Linking

Notification

↓

Tap Notification

↓

Open Specific Screen

Example

```
Order Delivered

↓

Order Details Screen
```

---

# Notification Permissions

Android 13+

Requires

```
POST_NOTIFICATIONS
```

permission.

---

# Local Notifications

Examples

- Daily Reminder
- Water Reminder
- Medicine Reminder
- Alarm

Notifee is commonly used.

---

# Notification Architecture

```
Backend

↓

Firebase

↓

Messaging Service

↓

Notification Handler

↓

Navigation

↓

Target Screen
```

---

# Folder Structure

```
src/

notifications/

    NotificationService.ts

hooks/

    useNotification.ts

navigation/

services/
```

---

# Best Practices

✅ Create notification channels.

✅ Save the FCM token on the backend.

✅ Refresh the token when required.

✅ Handle foreground and background notifications.

✅ Navigate users to the correct screen.

---

# Interview Questions

### Which library is commonly used?

@react-native-firebase/messaging

---

### Which library displays local notifications?

Notifee.

---

### What is an FCM Token?

A unique identifier used by Firebase to send notifications to a specific device.

---

### Why are Notification Channels required?

To categorize notifications and allow users to control notification settings.

---

### What happens when the user taps a notification?

The application can open a specific screen using Deep Linking.

---

# Real Project Example

E-Commerce App

```
Backend

↓

Order Shipped

↓

Firebase

↓

Push Notification

↓

User Taps Notification

↓

Order Details Screen
```

---

# Summary

React Native applications commonly use **Firebase Cloud Messaging (FCM)** for receiving push notifications and **Notifee** for displaying and managing local notifications. Android developers can think of this as the equivalent of using Firebase Cloud Messaging together with NotificationManager and Notification Channels to build a complete notification system.
