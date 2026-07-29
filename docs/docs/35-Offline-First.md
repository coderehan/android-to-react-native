# 35. Offline First

## What is Offline First?

Offline First means the application continues to work even when there is no internet connection.

Instead of depending only on APIs,

the application first reads local data.

Examples

- WhatsApp
- Spotify
- Google Maps
- Flipkart
- Amazon

---

# Android

Popular technologies

- Room
- WorkManager
- DataStore
- Repository Pattern

---

# React Native

Popular technologies

- WatermelonDB
- MMKV
- Background Fetch
- Zustand

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Room | WatermelonDB |
| WorkManager | react-native-background-fetch |
| SharedPreferences | MMKV |
| Repository | Service Layer |
| StateFlow | Zustand |

---

# Offline First Flow

```
Application Starts

↓

Read Local Database

↓

Display UI

↓

Check Internet

↓

Fetch API

↓

Update Database

↓

Refresh UI
```

---

# Why Offline First?

Advantages

- Faster App Launch
- Better User Experience
- Works Without Internet
- Less API Calls
- Better Battery Life

---

# Local Database

Store important data locally.

Examples

- Products
- User Profile
- Messages
- Orders

React Native

```
WatermelonDB
```

---

# Local Storage

Store small values

Examples

- JWT Token
- Theme
- Language
- User Settings

React Native

```
MMKV
```

---

# Network Monitoring

Application checks

```
Internet Available?

↓

Yes

↓

Call API

↓

Update Database

↓

Refresh UI
```

Otherwise

↓

Use Local Database.

---

# Synchronization

When internet becomes available

```
Offline Changes

↓

Background Sync

↓

Backend

↓

Database Updated
```

---

# Background Sync

React Native

```
react-native-background-fetch
```

checks for updates periodically.

Very similar to

```
WorkManager
```

---

# Repository Pattern

Flow

```
UI

↓

Service

↓

WatermelonDB

↓

Backend API
```

UI never directly calls APIs.

---

# Conflict Resolution

Example

```
User Updates Profile Offline

↓

Backend Also Updated

↓

Choose Latest Version

↓

Sync Complete
```

Applications define rules to resolve conflicts.

---

# Caching Strategy

```
API

↓

WatermelonDB

↓

UI

↓

Offline Access
```

Instead of requesting data every time,

the app uses cached data.

---

# Folder Structure

```
src/

database/

services/

offline/

hooks/

sync/

SyncService.ts
```

---

# Best Practices

✅ Cache important data.

✅ Sync automatically.

✅ Handle API failures gracefully.

✅ Show offline indicator.

✅ Retry failed requests.

---

# Interview Questions

### What is Offline First?

An architecture where the application works even without internet by using locally stored data.

---

### Which database is commonly used?

WatermelonDB.

---

### Which storage is commonly used?

MMKV.

---

### Which library is similar to WorkManager?

react-native-background-fetch.

---

### Why cache data?

To improve speed and support offline usage.

---

### What is synchronization?

Updating local and remote data when internet becomes available.

---

# Real Project Example

Shopping App

```
User Opens App

↓

Read Products

↓

WatermelonDB

↓

Display Products

↓

Internet Available

↓

Fetch Latest Products

↓

Update Database

↓

Refresh UI
```

---

# Summary

React Native applications commonly implement an Offline First architecture using **WatermelonDB** for local data, **MMKV** for key-value storage, and **react-native-background-fetch** for background synchronization. Android developers can think of this as the equivalent of **Room + WorkManager + Repository Pattern**, enabling applications to continue functioning smoothly even without an internet connection.
