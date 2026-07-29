# 24. Animations

## What are Animations?

Animations improve the user experience by making UI interactions smoother and more engaging.

Common examples:

- Button Click
- Screen Transition
- Loading Animation
- Expand / Collapse
- Fade In
- Slide Animation

Popular Apps

- Instagram
- WhatsApp
- Flipkart
- Amazon
- Google Pay

---

# Android

Popular animation APIs

- View Animation ⭐⭐⭐⭐☆
- Property Animation ⭐⭐⭐⭐⭐
- MotionLayout ⭐⭐⭐⭐⭐
- Lottie ⭐⭐⭐⭐⭐

Most modern Android apps use:

- Property Animation
- MotionLayout
- Lottie

---

# React Native

Popular animation libraries

- Animated API ⭐⭐⭐⭐⭐
- React Native Reanimated ⭐⭐⭐⭐⭐
- Lottie React Native ⭐⭐⭐⭐⭐
- React Native Gesture Handler ⭐⭐⭐⭐⭐

Most production applications use:

- Reanimated
- Lottie
- Gesture Handler

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Property Animation | Animated API |
| MotionLayout | Reanimated |
| AnimatorSet | Animation Sequence |
| GestureDetector | Gesture Handler |
| Lottie Android | Lottie React Native |

---

# Animation Flow

```
User Interaction

↓

Animation Trigger

↓

Animation Starts

↓

UI Updates

↓

Animation Ends
```

---

# Animated API

The built-in animation library in React Native.

Supports

- Fade
- Scale
- Rotation
- Translation

Example

```tsx
Animated.timing(...)
```

---

# Reanimated

The most popular animation library for production apps.

Supports

- Smooth Animations
- Shared Values
- Gesture Animations
- Native Performance

Example

```tsx
useSharedValue()
```

---

# Fade Animation

Flow

```
Opacity

0

↓

1

↓

Visible
```

---

# Scale Animation

Flow

```
1.0

↓

1.2

↓

1.0
```

Commonly used for

- Buttons
- Cards
- Icons

---

# Slide Animation

Examples

- Bottom Sheet
- Navigation Drawer
- Side Menu

Flow

```
Off Screen

↓

Translate

↓

Visible
```

---

# Rotation Animation

Examples

- Loading Spinner
- Refresh Icon

Flow

```
0°

↓

360°
```

---

# Gesture Animation

Examples

- Swipe Card
- Drag & Drop
- Pull To Refresh
- Bottom Sheet

React Native

```
react-native-gesture-handler
```

works closely with Reanimated.

---

# Lottie Animation

Lottie allows developers to use animations created in Adobe After Effects.

Common uses

- Success Animation
- Error Animation
- Loading Animation
- Empty State

Library

```
lottie-react-native
```

---

# Shared Element Transition

Examples

- Product Image
- Profile Picture
- Gallery Preview

Flow

```
Small Image

↓

Smooth Transition

↓

Full Screen Image
```

---

# Animation Architecture

```
User Action

↓

Animation

↓

State Update

↓

UI Re-render
```

---

# Folder Structure

```
src/

animations/

    FadeAnimation.tsx

    ScaleAnimation.tsx

components/

hooks/

screens/
```

---

# Best Practices

✅ Keep animations smooth.

✅ Avoid unnecessary animations.

✅ Use Reanimated for complex animations.

✅ Use Lottie for loading and success screens.

✅ Optimize animations for low-end devices.

---

# Interview Questions

### Which animation library is commonly used?

React Native Reanimated.

---

### Which library is used for Lottie animations?

lottie-react-native.

---

### What is similar to MotionLayout?

React Native Reanimated.

---

### Which library handles gestures?

react-native-gesture-handler.

---

### Why use animations?

To improve user experience and make interactions feel smooth and natural.

---

# Real Project Example

E-Commerce App

```
User Taps Product

↓

Scale Animation

↓

Navigate

↓

Shared Element Animation

↓

Product Details
```

---

# Summary

React Native provides multiple animation solutions. The built-in Animated API is suitable for simple animations, while React Native Reanimated delivers high-performance, native-like animations for production applications. Lottie is commonly used for rich animated illustrations, and Gesture Handler enables smooth touch interactions.
