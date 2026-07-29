# 15. Database

## What is a Database?

A database is used to store data locally on the device.

It allows an application to:

- Work offline
- Cache API responses
- Store user information
- Save app settings
- Improve performance

Examples:

- Notes App
- WhatsApp Messages
- Offline News
- Shopping Cart
- Banking Apps

---

# Android

Popular local databases:

- Room ⭐⭐⭐⭐⭐
- SQLite ⭐⭐⭐⭐☆
- Realm ⭐⭐⭐⭐☆

Most modern Android applications use:

- Room

---

# React Native

Popular local databases:

- SQLite ⭐⭐⭐⭐⭐
- WatermelonDB ⭐⭐⭐⭐⭐
- Realm ⭐⭐⭐⭐☆
- MMKV (Key-Value Storage)

Most production applications use:

- SQLite
- WatermelonDB

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Room | SQLite |
| SQLite | SQLite |
| Entity | Table |
| DAO | Database Functions |
| Repository | Repository / Service |
| Room Database | SQLite Database |
| Flow | Database Subscription |

---

# Database Flow

Android

```
UI

↓

ViewModel

↓

Repository

↓

DAO

↓

Room Database
```

---

React Native

```
Screen

↓

Hook

↓

Repository / Service

↓

SQLite

↓

Database
```

---

# Entity

Android

```kotlin
@Entity
data class User(

    @PrimaryKey
    val id:Int,

    val name:String

)
```

---

React Native

TypeScript Interface

```typescript
export interface User{

    id:number;

    name:string;

}
```

The database table contains the same fields.

---

# DAO

Android

```kotlin
@Dao

interface UserDao{

    @Query("SELECT * FROM user")
    suspend fun getUsers()

}
```

---

React Native

```typescript
async function getUsers(){

}
```

Database queries are written inside repository/service files.

---

# Insert Data

Android

```kotlin
userDao.insert(user)
```

---

React Native

```typescript
db.executeSql(

    "INSERT INTO users(name) VALUES(?)"

)
```

---

# Read Data

Android

```kotlin
userDao.getUsers()
```

---

React Native

```typescript
db.executeSql(

    "SELECT * FROM users"

)
```

---

# Update Data

Android

```kotlin
userDao.update(user)
```

---

React Native

```typescript
db.executeSql(

    "UPDATE users SET name=?"

)
```

---

# Delete Data

Android

```kotlin
userDao.delete(user)
```

---

React Native

```typescript
db.executeSql(

    "DELETE FROM users"

)
```

---

# Offline First

One of the biggest advantages of local databases.

Flow

```
API

↓

Save to Database

↓

Display Database Data

↓

Offline Supported
```

Very similar to Android Offline-First Architecture.

---

# API Caching

Typical Flow

```
Server

↓

Axios

↓

Repository

↓

SQLite

↓

UI
```

Even without internet, users can still see previously downloaded data.

---

# Database Folder Structure

```
src/

database/

    Database.ts

    UserRepository.ts

    ProductRepository.ts

models/

services/
```

---

# When to Use a Database?

Use a database for:

- Offline Apps
- Chat Apps
- News Apps
- Banking Apps
- Notes Apps
- E-commerce Apps

---

# When NOT to Use a Database?

Do not use a database for:

- Temporary Loading State
- Theme
- Token Storage
- Small Settings

Use:

- AsyncStorage
- MMKV

instead.

---

# Best Practices

✅ Store API responses locally.

✅ Keep SQL queries inside repository files.

✅ Use transactions for multiple operations.

✅ Keep UI independent from the database.

✅ Support offline mode whenever possible.

---

# Interview Questions

### Which database is commonly used?

SQLite.

---

### What is similar to Room?

SQLite or WatermelonDB.

---

### What is similar to Entity?

A database table represented by a TypeScript interface.

---

### Where should database queries be written?

Inside Repository or Service.

---

### Why use a local database?

- Offline Support
- Faster Loading
- Reduced Network Calls

---

# Real Project Example

Android

Flipkart App

↓

Room Database

↓

Cached Product List

---

React Native

Shopping App

↓

SQLite

↓

Cached Product List

---

# Summary

React Native supports several local database solutions such as SQLite, WatermelonDB, and Realm. Android developers can think of SQLite or WatermelonDB as the equivalent of Room. Using a local database enables offline support, API response caching, and better application performance.
