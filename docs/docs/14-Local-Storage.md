# 14. Dependency Injection

## What is Dependency Injection?

Dependency Injection (DI) is a technique where objects receive their dependencies from outside instead of creating them internally.

This makes code:

- Easier to test
- Easier to maintain
- Easier to replace implementations
- Easier to scale

---

# Android

Popular DI frameworks:

- Hilt ⭐⭐⭐⭐⭐
- Dagger ⭐⭐⭐⭐☆
- Koin ⭐⭐⭐⭐☆

Modern Android applications mostly use **Hilt**.

---

# React Native

Common approaches:

- Context API ⭐⭐⭐⭐⭐
- Custom Hooks ⭐⭐⭐⭐⭐
- InversifyJS ⭐⭐⭐☆☆
- tsyringe ⭐⭐⭐☆☆

Most production React Native apps **do not use a heavy DI framework**.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Hilt | Context API |
| Dagger | InversifyJS |
| Koin | tsyringe |
| @Inject | Constructor Parameters |
| @Singleton | Singleton JS Module |
| Module | Provider / Factory |
| Component | Context Provider |

---

# Without Dependency Injection

## Android

```kotlin
class UserRepository {
    private val api = Retrofit.Builder().build()
}
```

Problem:

- Hard to test
- Hard to replace API implementation
- Tight coupling

---

## React Native

```typescript
class UserService {
    private api = axios.create()
}
```

Same problem.

---

# Constructor Injection

## Android

```kotlin
class UserRepository @Inject constructor(
    private val api: UserApi
)
```

---

## React Native

```typescript
class UserService {
    constructor(private api: AxiosInstance) {}
}
```

The dependency is passed from outside.

This is the same core DI principle.

---

# Singleton

## Android

```kotlin
@Singleton
class UserRepository
```

---

## React Native

```typescript
export const api = axios.create({
    baseURL: BASE_URL
});
```

A JavaScript module is loaded once and shared across the app.

This behaves like a Singleton.

---

# Hilt Module

Android

```kotlin
@Module
@InstallIn(SingletonComponent::class)
object NetworkModule {

    @Provides
    fun provideApi(): UserApi = ...
}
```

---

# React Native Provider

```typescript
export const ApiContext = createContext(api);
```

The provider supplies the dependency to the component tree.

---

# Injecting into UI

Android

```kotlin
@HiltViewModel
class UserViewModel @Inject constructor(
    private val repository: UserRepository
)
```

---

React Native

```typescript
function useUsers() {
    const api = useContext(ApiContext);
}
```

The Hook receives the dependency from Context.

---

# Scopes

## Android

- SingletonComponent
- ActivityRetainedComponent
- ViewModelComponent
- ActivityComponent
- FragmentComponent

---

## React Native

React Native does not have built-in DI scopes.

Common equivalents:

| Android Scope | React Native |
|----------------|--------------|
| Singleton | Module Singleton |
| Activity | Screen State |
| ViewModel | Custom Hook |
| Fragment | Component |
| Application | Root Context |

---

# Recommended Architecture

```
Screen
    ↓
Custom Hook
    ↓
Service
    ↓
Axios Instance
```

This is the closest equivalent to:

```
UI
    ↓
ViewModel
    ↓
Repository
    ↓
Retrofit
```

---

# Context API

Best for:

- Authentication
- Theme
- User Session
- Language
- Feature Flags

Example:

```typescript
<AuthProvider>
    <App />
</AuthProvider>
```

Any screen can access authentication state.

---

# Custom Hooks

Example:

```typescript
function useLogin() {
    const login = async () => {

    };

    return { login };
}
```

Think of this as a lightweight ViewModel.

---

# InversifyJS

A full-featured DI container.

Provides:

- Registration
- Resolution
- Scopes
- Interfaces
- Decorators

Very similar to Dagger/Hilt.

Usually used only in very large enterprise projects.

---

# tsyringe

A lightweight DI library from Microsoft.

Much simpler than InversifyJS.

Closer to Koin in terms of developer experience.

---

# When to Use What?

| Project Size | Recommendation |
|---------------|----------------|
| Small | Custom Hooks |
| Medium | Context + Hooks |
| Large | Context + Hooks + Services |
| Enterprise | InversifyJS / tsyringe |

---

# Real Project Example

## Android

```
LoginScreen
    ↓
LoginViewModel
    ↓
AuthRepository
    ↓
Retrofit
```

---

## React Native

```
LoginScreen
    ↓
useLogin()
    ↓
AuthService
    ↓
Axios
```

Notice how the layers are almost identical.

---

# Best Practices

✅ Create one Axios instance.

✅ Keep API logic inside Services.

✅ Keep business logic inside Hooks.

✅ Use Context only for truly global state.

✅ Avoid over-engineering with a DI framework unless the app is very large.

---

# Interview Questions

### Does React Native have Hilt?

No.

React Native does not have an official Hilt-like framework.

---

### What is the most common DI approach?

Context API + Custom Hooks.

---

### What is similar to @Inject?

Passing dependencies through constructor parameters.

---

### What is similar to @Singleton?

A module-level exported object.

---

### When should InversifyJS be used?

For large enterprise applications that require a formal DI container.

---

# Summary

Android developers commonly use Hilt or Dagger for dependency injection.

React Native applications usually rely on **Context API, Custom Hooks, and singleton service modules**.

The mental mapping is:

- Hilt → Context API
- ViewModel → Custom Hook
- Repository → Service
- Retrofit → Axios
- @Singleton → Module Singleton

For most real-world React Native apps, **Context + Hooks + Services** is the sweet spot.
