# 1. Programming Language

## What is a Programming Language?

A programming language is used to write the logic of an application.

In Android, we mainly use **Kotlin**.

In React Native, we mainly use **JavaScript** or **TypeScript**.

---

# Android

Android development officially supports:

- Kotlin ⭐⭐⭐⭐⭐ (Recommended)
- Java

Example:

```kotlin
fun greet() {
    println("Hello Android")
}
```

---

# React Native

React Native supports:

- JavaScript
- TypeScript ⭐⭐⭐⭐⭐ (Recommended)

Example:

```typescript
function greet() {
    console.log("Hello React Native");
}
```

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Kotlin | TypeScript |
| Java | JavaScript |
| Strongly Typed | Strongly Typed (TypeScript) |
| Compiled | Transpiled to JavaScript |

---

# Why TypeScript instead of JavaScript?

If you already know Kotlin, TypeScript will feel much more familiar.

Both support:

- Classes
- Interfaces
- Generics
- Type Checking
- Auto-completion
- Better compile-time error detection

Example:

Kotlin

```kotlin
data class User(
    val id: Int,
    val name: String
)
```

TypeScript

```typescript
interface User {
    id: number;
    name: string;
}
```

---

# Similarities

| Kotlin | TypeScript |
|----------|------------|
| data class | interface / type |
| val | const |
| var | let |
| fun | function |
| class | class |
| enum class | enum |
| null safety | optional chaining (?.) |
| suspend | async |

---

# Best Choice

✅ Android

- Kotlin

✅ React Native

- TypeScript

---

# Key Points

- Kotlin is the official language for Android development.
- TypeScript is the preferred language for React Native projects.
- TypeScript provides type safety similar to Kotlin.
- Most production React Native applications use TypeScript.

---

# Interview Questions

### Why is TypeScript preferred over JavaScript?

Because TypeScript provides:

- Type Safety
- Better IntelliSense
- Easier Refactoring
- Better Code Maintainability

---

### Can React Native be developed using JavaScript?

Yes.

However, TypeScript is recommended for medium and large projects.

---

# Summary

Android Developers should learn **TypeScript** instead of plain JavaScript because its syntax and development experience are much closer to Kotlin.
