# 12. JSON Parsing

## What is JSON?

JSON (JavaScript Object Notation) is the most common format used to exchange data between a mobile application and a server.

Example

```json
{
    "id": 1,
    "name": "Mohammed",
    "age": 25
}
```

Almost every REST API returns JSON.

---

# Android

Android applications usually use:

- Gson ⭐⭐⭐⭐⭐
- Moshi ⭐⭐⭐⭐☆
- Kotlin Serialization ⭐⭐⭐⭐⭐

These libraries convert JSON into Kotlin objects.

---

# React Native

React Native uses:

- JSON.parse()
- Axios (Automatic Parsing)
- Fetch API

No external JSON parsing library is required in most cases.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Gson | JSON.parse() |
| Moshi | JSON.parse() |
| Kotlin Serialization | JSON.parse() |
| Data Class | TypeScript Interface |
| Serialized Object | JavaScript Object |

---

# JSON Object

Example

```json
{
    "id":101,
    "name":"John",
    "email":"john@gmail.com"
}
```

---

# Kotlin Data Class

Android

```kotlin
data class User(
    val id:Int,
    val name:String,
    val email:String
)
```

---

# TypeScript Interface

React Native

```typescript
export interface User {

    id:number;

    name:string;

    email:string;

}
```

TypeScript interfaces describe the shape of an object.

---

# Parsing JSON

Android (Retrofit + Gson)

```kotlin
val users = api.getUsers()
```

Retrofit automatically converts JSON into Kotlin objects.

---

React Native (Axios)

```typescript
const response = await axios.get("/users");

const users = response.data;
```

Axios automatically parses JSON into JavaScript objects.

---

# Fetch API

```typescript
const response = await fetch(url);

const data = await response.json();
```

The `json()` method converts the response into a JavaScript object.

---

# JSON.parse()

Sometimes JSON is received as a string.

Example

```typescript
const json = '{"name":"John"}';

const user = JSON.parse(json);
```

Output

```
{
    name:"John"
}
```

---

# Nested JSON

Example

```json
{
    "id":1,
    "name":"John",
    "address":{
        "city":"Chennai",
        "country":"India"
    }
}
```

---

TypeScript Interface

```typescript
interface Address{

    city:string;

    country:string;

}

interface User{

    id:number;

    name:string;

    address:Address;

}
```

---

# JSON Array

Example

```json
[
    {
        "id":1,
        "name":"John"
    },
    {
        "id":2,
        "name":"Alice"
    }
]
```

---

TypeScript

```typescript
const users:User[] = response.data;
```

Very similar to:

```kotlin
List<User>
```

in Android.

---

# Optional Fields

Sometimes an API may not return all fields.

Android

```kotlin
val name:String?
```

---

React Native

```typescript
name?: string;
```

The `?` means the field is optional.

---

# Null Values

Android

```kotlin
String?
```

---

React Native

```typescript
string | null
```

Example

```typescript
email:string | null;
```

---

# API Response

Android

```kotlin
data class ApiResponse(

    val data:List<User>

)
```

---

React Native

```typescript
interface ApiResponse{

    data:User[];

}
```

---

# Folder Structure

```
src/

models/

    User.ts

    Product.ts

    LoginResponse.ts

    ApiResponse.ts
```

Keep all interfaces inside the `models` folder.

---

# Best Practices

✅ Use TypeScript interfaces.

✅ Keep models inside a dedicated folder.

✅ Avoid using `any`.

✅ Handle optional fields properly.

✅ Validate API responses when needed.

---

# Interview Questions

### Which format is commonly used for APIs?

JSON.

---

### What is similar to Kotlin data class?

TypeScript Interface.

---

### Which method converts JSON string into an object?

```
JSON.parse()
```

---

### Does Axios automatically parse JSON?

Yes.

The response is available in:

```typescript
response.data
```

---

### What is similar to List<User>?

```typescript
User[]
```

---

# Summary

React Native works primarily with JSON data returned from APIs. Axios automatically converts JSON into JavaScript objects, while TypeScript interfaces provide type safety similar to Kotlin data classes in Android.
