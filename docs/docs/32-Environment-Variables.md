# 32. Environment Variables

## What are Environment Variables?

Environment Variables allow us to store configuration values outside the source code.

Examples

- API Base URL
- API Keys
- Firebase Project ID
- App Name
- Feature Flags

Instead of hardcoding values, we read them from environment files.

---

# Android

Common approach

- BuildConfig
- build.gradle
- Product Flavors

Example

```
BuildConfig.BASE_URL
```

---

# React Native

Popular library

- react-native-config ⭐⭐⭐⭐⭐

This library reads values from `.env` files.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| BuildConfig | react-native-config |
| Product Flavors | Multiple .env Files |
| build.gradle | .env |
| BuildConfig.BASE_URL | Config.BASE_URL |

---

# Why Use Environment Variables?

Instead of

```
https://api.production.com
```

inside your code,

store it in

```
.env
```

Benefits

- Easy to change
- More secure
- Different environments
- Cleaner code

---

# Common Environment Files

```
.env

.env.development

.env.qa

.env.staging

.env.production
```

Each file contains different configuration values.

---

# Example

Development

```
API_URL=https://dev-api.example.com

APP_NAME=MyApp Dev
```

---

Production

```
API_URL=https://api.example.com

APP_NAME=MyApp
```

---

# Folder Structure

```
project/

.env

.env.development

.env.qa

.env.staging

.env.production
```

---

# Accessing Variables

React Native

```typescript
import Config from "react-native-config";

Config.API_URL

Config.APP_NAME
```

---

# Typical Flow

```
Application Starts

↓

Read .env File

↓

Load Variables

↓

Use Configuration
```

---

# Common Variables

```
API_URL

APP_NAME

GOOGLE_MAPS_API_KEY

FIREBASE_PROJECT_ID

SENTRY_DSN

VERSION_NAME
```

---

# Multiple Environments

Development

↓

QA

↓

Staging

↓

Production

Each environment has

- Different API
- Different Database
- Different Firebase Project

---

# Example Architecture

```
.env.production

↓

Config

↓

Axios

↓

Backend
```

---

# Security

Environment variables are useful for configuration.

Do NOT store

- Passwords
- Private Keys
- Secrets

inside `.env` files that are bundled with the app.

Sensitive values should remain on the backend or use secure platform-specific solutions.

---

# Folder Structure

```
src/

config/

    Config.ts

services/

    ApiService.ts
```

---

# Best Practices

✅ Create separate .env files for each environment.

✅ Keep configuration centralized.

✅ Do not hardcode API URLs.

✅ Ignore local environment files in Git when appropriate.

✅ Keep secrets on the backend.

---

# Interview Questions

### Which library is commonly used?

react-native-config.

---

### What is similar to BuildConfig?

react-native-config.

---

### Why use environment variables?

To manage different configurations without changing source code.

---

### Can you have multiple .env files?

Yes.

For Development, QA, Staging, and Production.

---

### Should passwords be stored in .env?

No.

Keep sensitive secrets on the backend.

---

# Real Project Example

Shopping App

```
Development Build

↓

.env.development

↓

Dev API

↓

Testing
```

```
Production Build

↓

.env.production

↓

Production API

↓

Users
```

---

# Summary

React Native commonly uses **react-native-config** to manage environment variables. Similar to Android's **BuildConfig** and Product Flavors, it allows applications to switch between Development, QA, Staging, and Production environments without changing application code.
