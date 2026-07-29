# 23. Background Tasks

## What are Background Tasks?

Background Tasks allow an application to perform work even when the application is not actively being used.

Examples

- Sync Data
- Upload Images
- Download Files
- Backup Data
- Location Tracking
- Refresh Content

Popular Apps

- WhatsApp
- Gmail
- Google Photos
- Swiggy
- Uber

---

# Android

Popular background task APIs

- WorkManager ⭐⭐⭐⭐⭐
- Foreground Service ⭐⭐⭐⭐⭐
- AlarmManager ⭐⭐⭐⭐☆

Most production applications use

- WorkManager

---

# React Native

Popular libraries

- react-native-background-fetch ⭐⭐⭐⭐⭐
- Headless JS ⭐⭐⭐⭐☆
- react-native-background-actions ⭐⭐⭐⭐☆

Most production applications use

- react-native-background-fetch

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| WorkManager | react-native-background-fetch |
| Foreground Service | react-native-background-actions |
| Background Service | Headless JS |
| Coroutine Worker | Background Task |
| Periodic Work | Scheduled Background Fetch |

---

# Background Task Flow

```
User Action

↓

Schedule Task

↓

Application Goes Background

↓

Background Task Executes

↓

API Call

↓

Database Update

↓

Next Scheduled Execution
```

---

# Common Background Tasks

- Sync API Data
- Upload Images
- Download Files
- Backup Messages
- Refresh News
- Location Tracking

---

# Background Fetch

Background Fetch periodically wakes the application.

Typical Flow

```
Operating System

↓

Background Fetch

↓

API Request

↓

Update Database

↓

Finish Task
```

---

# Headless JS

Headless JS allows JavaScript code to execute even when the application UI is not active.

Common use cases

- Background Sync
- Upload Logs
- Process Notifications

---

# Foreground Tasks

Some tasks must continue while the user is aware.

Examples

- Music Player
- Navigation
- Fitness Tracking
- Call Recording

These usually require a persistent notification on Android.

---

# Periodic Sync

```
Every 15 Minutes

↓

Background Fetch

↓

Check Server

↓

Download Updates

↓

Save Database
```

---

# Background Upload

Example

```
Capture Image

↓

Compress Image

↓

Background Upload

↓

Success Notification
```

Useful when uploading large files.

---

# Background Download

Example

```
Download PDF

↓

Background Task

↓

Save Storage

↓

Notification
```

---

# Background Location

Flow

```
GPS

↓

Location Updates

↓

Backend

↓

Map Updates
```

Used by

- Uber
- Ola
- Swiggy

---

# Architecture

```
Screen

↓

Background Task

↓

API

↓

SQLite

↓

Update UI
```

---

# Folder Structure

```
src/

background/

    BackgroundTask.ts

services/

    SyncService.ts

hooks/

    useBackgroundSync.ts

database/

storage/
```

---

# Best Practices

✅ Keep background tasks lightweight.

✅ Schedule work only when necessary.

✅ Handle network failures gracefully.

✅ Save progress locally.

✅ Respect battery optimization policies.

---

# Interview Questions

### What is a Background Task?

A task that continues to execute even when the application is in the background or not actively being used.

---

### Which library is commonly used?

react-native-background-fetch

---

### What is similar to WorkManager?

react-native-background-fetch

---

### What is Headless JS?

A React Native feature that allows JavaScript code to run without the application's UI being active.

---

### When should Foreground Services be used?

For long-running tasks such as navigation, fitness tracking, or music playback that must remain active while the user is aware.

---

# Real Project Example

News App

```
Background Fetch

↓

Fetch Latest News

↓

Update SQLite

↓

User Opens App

↓

Latest News Available
```

---

# Summary

React Native supports background processing using libraries such as **react-native-background-fetch**, **Headless JS**, and **react-native-background-actions**. Android developers can think of these as equivalents to WorkManager, Background Services, and Foreground Services for implementing periodic sync, uploads, downloads, and other long-running tasks.
