# 8. Navigation

## What is Navigation?

Navigation allows users to move from one screen to another inside an application.

Examples:

- Login → Home
- Home → Profile
- Profile → Settings

Every mobile application uses navigation.

---

# Android

Android provides multiple ways to navigate between screens.

Examples:

- Intent
- Navigation Component
- Activities
- Fragments

Modern Android mainly uses the Navigation Component.

---

# React Native

React Native uses **React Navigation**.

It is the most popular navigation library.

Official Package

```
@react-navigation/native
```

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Activity | Screen |
| Fragment | Screen |
| Intent | navigate() |
| Navigation Component | React Navigation |
| NavHost | NavigationContainer |
| NavController | Navigation Object |
| Back Press | goBack() |

---

# Navigation Types

React Native provides different navigation patterns.

- Stack Navigation
- Bottom Tab Navigation
- Drawer Navigation

---

# Stack Navigation

Used when navigating between screens.

Example

```
Login

↓

Home

↓

Profile

↓

Settings
```

Like opening new pages one after another.

Most applications use Stack Navigation.

---

# Bottom Tab Navigation

Shows tabs at the bottom of the screen.

Example

```
Home

Search

Cart

Profile
```

Very common in:

- Instagram
- WhatsApp
- Amazon
- Flipkart

---

# Drawer Navigation

Displays a side menu.

Example

```
☰ Menu

Home

Orders

Settings

Logout
```

Common in enterprise applications.

---

# Navigation Flow

Android

```
Intent

↓

Activity
```

React Native

```
navigate()

↓

Screen
```

---

# Navigate to Another Screen

Android

```kotlin
startActivity(
    Intent(this, HomeActivity::class.java)
)
```

---

React Native

```tsx
navigation.navigate("Home")
```

---

# Go Back

Android

```kotlin
finish()
```

---

React Native

```tsx
navigation.goBack()
```

---

# Passing Data

Android

```kotlin
intent.putExtra("id",100)
```

---

React Native

```tsx
navigation.navigate("Profile",{
    id:100
})
```

---

# Receiving Data

Android

```kotlin
intent.getIntExtra("id",0)
```

---

React Native

```tsx
route.params.id
```

---

# Navigation Container

Every React Native application starts with:

```tsx
<NavigationContainer>

</NavigationContainer>
```

This manages the navigation state.

Similar to:

```
NavHost
```

in Android.

---

# Stack Navigator

Example

```tsx
<Stack.Navigator>

    <Stack.Screen
        name="Home"
        component={HomeScreen}
    />

</Stack.Navigator>
```

Each screen is registered inside the navigator.

---

# Screen Lifecycle

Android

```
onCreate()

↓

onStart()

↓

onResume()
```

React Native

```
Component Mount

↓

Screen Focus

↓

Screen Blur

↓

Component Unmount
```

---

# Deep Linking

Deep Linking opens a specific screen directly.

Example

```
myapp://profile/101
```

Useful for:

- Notifications
- Email Links
- Payment Apps
- QR Codes

---

# Best Practices

✅ Use React Navigation.

✅ Separate navigation into its own folder.

✅ Keep navigation configuration simple.

✅ Pass only required data between screens.

✅ Avoid deeply nested navigators unless necessary.

---

# Interview Questions

### Which library is commonly used for navigation?

React Navigation.

---

### What is similar to Intent?

navigation.navigate()

---

### What is similar to Activity?

Screen.

---

### What is similar to Fragment?

Screen.

---

### How do you return to the previous screen?

```
navigation.goBack()
```

---

### Which navigation type is most commonly used?

Stack Navigation.

---

### How do you pass data to another screen?

```
navigation.navigate("Profile", {
    id: 100
})
```

---

### How do you receive data?

```
route.params
```

---

# Summary

Navigation in React Native is handled using **React Navigation**. It provides Stack, Bottom Tab, and Drawer navigation, making it easy to build multi-screen applications. Android developers can think of **Screen** as an equivalent to **Activity/Fragment**, and **navigate()** as an equivalent to **Intent**.
