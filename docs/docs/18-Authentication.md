# 18. Authentication

## What is Authentication?

Authentication is the process of verifying the identity of a user.

Examples

- Login
- Signup
- OTP Verification
- Social Login
- Fingerprint Login
- Face ID

After successful authentication, the server usually returns an Access Token.

---

# Android

Authentication is usually implemented using

- Retrofit
- ViewModel
- Repository
- DataStore
- EncryptedSharedPreferences
- Navigation

---

# React Native

Authentication is usually implemented using

- Axios
- Custom Hook
- Service
- MMKV
- react-native-keychain
- React Navigation

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| ViewModel | Custom Hook |
| Repository | Service |
| Retrofit | Axios |
| DataStore | MMKV |
| EncryptedSharedPreferences | react-native-keychain |
| Navigation Component | React Navigation |

---

# Authentication Flow

```
Login Screen

↓

Enter Email & Password

↓

Login Button

↓

Axios API Call

↓

Backend

↓

Validate Credentials

↓

Access Token

↓

Save Token

↓

Navigate Home
```

---

# Login API

Android

```kotlin
repository.login(email,password)
```

---

React Native

```typescript
await AuthService.login(
    email,
    password
);
```

---

# Login Request

Example

```json
{
    "email":"john@gmail.com",
    "password":"123456"
}
```

---

# Login Response

Example

```json
{
    "accessToken":"abc123",
    "refreshToken":"xyz789",
    "user":{
        "id":1,
        "name":"John"
    }
}
```

---

# Access Token

The Access Token is sent with every authenticated request.

Example

```
Authorization

Bearer access_token
```

---

# Axios Interceptor

Automatically attach the token.

```typescript
axios.interceptors.request.use(config => {

    config.headers.Authorization =
        `Bearer ${token}`;

    return config;

});
```

No need to manually add the token to every API call.

---

# Token Storage

Store

- Access Token
- Refresh Token

Use

```
react-native-keychain
```

or

```
MMKV
```

depending on security requirements.

---

# Auto Login

Application starts

↓

Check Token

↓

Token Exists?

↓

Yes

↓

Home Screen

↓

No

↓

Login Screen

---

# Logout Flow

```
Logout

↓

Delete Token

↓

Clear User Data

↓

Navigate Login
```

---

# Protected APIs

Some APIs require authentication.

Example

```
GET /profile

Authorization

Bearer Token
```

Without a valid token

↓

401 Unauthorized

---

# Refresh Token

Sometimes an Access Token expires.

Flow

```
API Call

↓

401

↓

Refresh Token API

↓

New Access Token

↓

Retry Original API
```

Axios Interceptors are commonly used for this.

---

# Authentication Folder Structure

```
src/

services/

    AuthService.ts

hooks/

    useLogin.ts

storage/

    SessionManager.ts

models/

    LoginRequest.ts

    LoginResponse.ts

navigation/

    AuthNavigator.tsx
```

---

# Login Architecture

```
Login Screen

↓

useLogin()

↓

AuthService

↓

Axios

↓

Backend

↓

Token

↓

Keychain

↓

Navigate Home
```

---

# Secure Storage

Never store

- Password
- OTP
- Banking PIN

Use secure storage for tokens.

---

# Best Practices

✅ Store tokens securely.

✅ Use Axios Interceptors.

✅ Handle token expiry.

✅ Clear data on logout.

✅ Never hardcode credentials.

✅ Validate user input before API calls.

---

# Interview Questions

### What is Authentication?

Verifying the identity of a user.

---

### Where should login API be written?

Inside AuthService.

---

### Where should Access Token be stored?

react-native-keychain.

---

### What is the purpose of Axios Interceptors?

Automatically attach tokens and handle responses.

---

### What happens when the token expires?

Use the Refresh Token to obtain a new Access Token, then retry the original request.

---

### Which screen should open after successful login?

Home Screen.

---

# Real Project Example

Food Delivery App

```
Login Screen

↓

useLogin()

↓

AuthService

↓

Axios

↓

Backend

↓

Access Token

↓

Keychain

↓

Home Screen
```

---

# Summary

Authentication in React Native is commonly implemented using **Axios**, **Custom Hooks**, **AuthService**, and **React Navigation**. Access and Refresh Tokens should be stored securely using **react-native-keychain**, while Axios Interceptors automatically attach tokens to authenticated API requests.
