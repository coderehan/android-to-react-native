# 11. Networking

## What is Networking?

Networking is the process of communicating with a server over the internet.

Applications use networking to:

- Login
- Register
- Fetch Users
- Upload Images
- Download Files
- Update Profile
- Make Payments

Most mobile apps communicate with REST APIs.

---

# Android

Popular networking libraries:

- Retrofit ⭐⭐⭐⭐⭐
- Ktor ⭐⭐⭐⭐☆
- OkHttp ⭐⭐⭐⭐⭐
- Volley ⭐⭐☆☆☆

Modern Android applications mostly use:

- Retrofit
- OkHttp
- Coroutines

---

# React Native

Popular networking libraries:

- Axios ⭐⭐⭐⭐⭐
- Fetch API ⭐⭐⭐⭐☆
- TanStack Query ⭐⭐⭐⭐⭐

Most production applications use:

- Axios
- TanStack Query

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Retrofit | Axios |
| Ktor Client | Fetch API |
| OkHttp | Fetch / Axios |
| Repository | Service |
| API Interface | Axios Instance |
| Interceptor | Axios Interceptor |
| Coroutine | async / await |
| StateFlow | TanStack Query |

---

# Networking Flow

Android

```
UI

↓

ViewModel

↓

Repository

↓

Retrofit

↓

Server
```

---

React Native

```
Screen

↓

Hook

↓

Service

↓

Axios

↓

Server
```

---

# Retrofit Example

```kotlin
interface UserApi {

    @GET("users")
    suspend fun getUsers(): List<User>

}
```

---

# Axios Example

```typescript
const response = await axios.get("/users");
```

Very simple and easy to use.

---

# Fetch API Example

```typescript
const response = await fetch("/users");

const data = await response.json();
```

Fetch is built into JavaScript.

No additional library is required.

---

# Axios Instance

Instead of writing:

```typescript
axios.get(...)
```

everywhere,

Create a reusable instance.

Example

```typescript
const api = axios.create({

    baseURL: "https://api.example.com"

});
```

Now use

```typescript
api.get("/users")
```

This is similar to creating one Retrofit instance.

---

# Interceptors

Interceptors modify requests and responses automatically.

Common uses:

- Add Token
- Logging
- Refresh Token
- Error Handling

---

Android

```kotlin
OkHttp Interceptor
```

---

React Native

```typescript
axios.interceptors.request.use(...)
```

---

# Repository vs Service

Android

```
Repository
```

contains API logic.

---

React Native

```
Service
```

contains API logic.

Example

```
UserService.ts
```

---

# Async Operations

Android

```kotlin
suspend fun
```

---

React Native

```typescript
async function
```

Example

```typescript
async function loadUsers() {

}
```

---

# Await

Android

```kotlin
val users = api.getUsers()
```

---

React Native

```typescript
const users = await api.get("/users");
```

await waits until the network request completes.

---

# Error Handling

Android

```kotlin
try {

}catch(e:Exception){

}
```

---

React Native

```typescript
try{

}catch(error){

}
```

Always handle errors gracefully.

---

# API Folder Structure

```
src/

services/

    api.ts

    UserService.ts

    AuthService.ts

    ProductService.ts
```

Each service handles one feature.

---

# Authentication Token

Store token after login.

Every request should automatically send:

```
Authorization

Bearer Token
```

Axios Interceptors make this easy.

---

# Loading State

Typical flow

```
Loading

↓

API Call

↓

Success

↓

Update UI
```

Always show a loading indicator while waiting for the server.

---

# Best Practices

✅ Create one Axios instance.

✅ Use Services for API calls.

✅ Handle errors properly.

✅ Use async / await.

✅ Use Axios Interceptors.

✅ Keep API URLs in constants.

---

# Interview Questions

### Which networking library is most popular?

Axios.

---

### What is similar to Retrofit?

Axios.

---

### What is similar to OkHttp Interceptor?

Axios Interceptor.

---

### What is similar to suspend?

async function.

---

### What is similar to Coroutines?

async / await.

---

### Where should API calls be written?

Inside the Service layer.

---

# Summary

Networking in React Native is commonly implemented using Axios together with async/await. Android developers can think of Axios as the equivalent of Retrofit, while Services replace the Repository layer for making API requests.
