# 14. Local Storage

## What is Local Storage?

Local Storage is used to store small amounts of data on the device.

Unlike a database, Local Storage is meant for simple key-value pairs.

Examples:

- Login Token
- Dark Mode
- Language Preference
- User Settings
- Onboarding Status

---

# Android

Popular local storage options:

- SharedPreferences ⭐⭐⭐⭐⭐
- DataStore ⭐⭐⭐⭐⭐
- EncryptedSharedPreferences ⭐⭐⭐⭐☆

Modern Android applications prefer:

- DataStore

---

# React Native

Popular local storage options:

- AsyncStorage ⭐⭐⭐⭐⭐
- MMKV ⭐⭐⭐⭐⭐
- react-native-keychain ⭐⭐⭐⭐⭐

Most production applications use:

- MMKV
- react-native-keychain

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| SharedPreferences | AsyncStorage |
| DataStore | MMKV |
| EncryptedSharedPreferences | react-native-keychain |
| putString() | setItem() |
| getString() | getItem() |
| remove() | removeItem() |
| clear() | clear() |

---

# Storage Flow

Android

```
UI

↓

ViewModel

↓

DataStore

↓

Device Storage
```

---

React Native

```
Screen

↓

Hook

↓

MMKV

↓

Device Storage
```

---

# AsyncStorage

AsyncStorage is a simple key-value storage.

Useful for:

- Theme
- Language
- First Launch
- User Preferences

Example

```typescript
import AsyncStorage from "@react-native-async-storage/async-storage";
```

---

# Save Data

```typescript
await AsyncStorage.setItem(

    "username",

    "Mohammed"

);
```

---

# Read Data

```typescript
const username = await AsyncStorage.getItem(

    "username"

);
```

---

# Remove Data

```typescript
await AsyncStorage.removeItem(

    "username"

);
```

---

# Clear Storage

```typescript
await AsyncStorage.clear();
```

---

# MMKV

MMKV is a high-performance key-value storage library.

Advantages

- Very Fast
- Synchronous API
- Better Performance
- Recommended for production

Example

```typescript
import { MMKV } from "react-native-mmkv";

const storage = new MMKV();
```

---

# Save Data (MMKV)

```typescript
storage.set(

    "username",

    "Mohammed"

);
```

---

# Read Data (MMKV)

```typescript
const username = storage.getString(

    "username"

);
```

---

# Delete Data (MMKV)

```typescript
storage.delete(

    "username"

);
```

---

# Secure Storage

Sensitive information should never be stored in AsyncStorage.

Examples:

- Password
- Access Token
- Refresh Token
- Banking PIN

Use:

```
react-native-keychain
```

instead.

---

# Login Flow

```
Login API

↓

Receive Token

↓

Save Token

↓

Navigate to Home

↓

Reuse Token for Future Requests
```

---

# Common Storage Items

Store

- Theme
- Language
- User Preferences
- Onboarding Completed

Do NOT Store

- Password
- Banking PIN
- Sensitive Secrets

---

# Folder Structure

```
src/

storage/

    Storage.ts

    SessionManager.ts

services/

models/
```

---

# Best Practices

✅ Use MMKV for production apps.

✅ Use Keychain for sensitive data.

✅ Store only small amounts of data.

✅ Clear user data during logout.

✅ Keep storage logic separate from UI.

---

# Interview Questions

### What is similar to SharedPreferences?

AsyncStorage.

---

### What is similar to DataStore?

MMKV.

---

### Where should login tokens be stored?

Prefer react-native-keychain for secure storage.

---

### Is AsyncStorage encrypted?

No.

---

### Which storage library is faster?

MMKV.

---

# Real Project Example

Android

Banking App

↓

DataStore

↓

Theme + Language

↓

EncryptedSharedPreferences

↓

Access Token

---

React Native

Banking App

↓

MMKV

↓

Theme + Language

↓

react-native-keychain

↓

Access Token

---

# Summary

React Native provides multiple options for local storage. AsyncStorage is simple and widely used, MMKV offers better performance for production apps, and react-native-keychain should be used for storing sensitive information securely.
