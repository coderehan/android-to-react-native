# 19. Permissions

## What are Permissions?

Permissions allow an application to access protected features or user data on the device.

Examples:

- Camera
- Location
- Microphone
- Storage
- Contacts
- Notifications

Without the required permission, the app cannot access these features.

---

# Android

Android permissions are declared in:

```
AndroidManifest.xml
```

Some permissions also require requesting the user's approval at runtime.

Example permissions:

- CAMERA
- ACCESS_FINE_LOCATION
- RECORD_AUDIO
- POST_NOTIFICATIONS
- READ_CONTACTS

---

# React Native

React Native also relies on the native Android and iOS permission systems.

Common libraries:

- react-native-permissions ⭐⭐⭐⭐⭐
- PermissionsAndroid (Android only)

Most production apps use:

```
react-native-permissions
```

because it supports both Android and iOS.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| AndroidManifest.xml | AndroidManifest.xml |
| requestPermissions() | request() |
| checkSelfPermission() | check() |
| Permission Callback | Promise |
| Activity Result API | request() Response |

---

# Permission Flow

```
Feature Requested

↓

Check Permission

↓

Granted?

↓

Yes

↓

Open Feature

↓

No

↓

Request Permission

↓

Granted?

↓

Yes

↓

Open Feature

↓

No

↓

Show Permission Denied Message
```

---

# Android Manifest

Example

```xml
<uses-permission android:name="android.permission.CAMERA"/>
```

---

# React Native

Permissions are still added inside

```
android/app/src/main/AndroidManifest.xml
```

Example

```xml
<uses-permission android:name="android.permission.CAMERA"/>
```

The native Android manifest is still used.

---

# Checking Permission

Android

```kotlin
ContextCompat.checkSelfPermission(...)
```

---

React Native

```typescript
const status = await check(
    PERMISSIONS.ANDROID.CAMERA
);
```

---

# Requesting Permission

Android

```kotlin
requestPermissions(...)
```

---

React Native

```typescript
const status = await request(
    PERMISSIONS.ANDROID.CAMERA
);
```

---

# Permission Result

Possible results

```
Granted

Denied

Blocked

Unavailable

Limited (iOS)
```

Always handle every possible result.

---

# Common Permissions

Camera

```
CAMERA
```

---

Location

```
ACCESS_FINE_LOCATION
```

---

Microphone

```
RECORD_AUDIO
```

---

Notifications

```
POST_NOTIFICATIONS
```

(Android 13+)

---

Contacts

```
READ_CONTACTS
```

---

Storage

```
READ_MEDIA_IMAGES

READ_MEDIA_VIDEO

READ_MEDIA_AUDIO
```

Modern Android versions use media-specific permissions instead of broad storage access.

---

# Best Practice Flow

```
User Clicks Camera

↓

Explain Why Permission Is Needed

↓

Request Permission

↓

Granted

↓

Open Camera

↓

Denied

↓

Show Friendly Message
```

Never request permissions without context.

---

# Folder Structure

```
src/

permissions/

    PermissionManager.ts

hooks/

    useCameraPermission.ts

utils/

services/
```

Keep permission logic separate from UI.

---

# Best Practices

✅ Request permission only when needed.

✅ Explain why the permission is required.

✅ Handle denied and blocked states.

✅ Avoid requesting unnecessary permissions.

✅ Test on both Android and iOS.

---

# Interview Questions

### Why do we need permissions?

To access protected device features such as Camera, Location, or Microphone.

---

### Which library is commonly used?

```
react-native-permissions
```

---

### Where are Android permissions declared?

```
AndroidManifest.xml
```

---

### Can permissions be denied?

Yes.

The application should handle denied and blocked states gracefully.

---

### Should permissions be requested at app startup?

No.

Request them only when the user performs an action that requires the permission.

---

# Real Project Example

Food Delivery App

```
User taps "Use Current Location"

↓

Check Location Permission

↓

Granted

↓

Open Google Maps

↓

Denied

↓

Show Permission Dialog
```

---

# Summary

React Native uses the same native Android and iOS permission systems. Android developers will find the process familiar: declare permissions in the manifest, check the current status, request permission when needed, and handle all possible outcomes. The `react-native-permissions` library provides a unified API for both Android and iOS.
