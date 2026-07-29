# 13. Image Loading

## What is Image Loading?

Image Loading is the process of downloading, displaying, and caching images efficiently inside an application.

Examples:

- User Profile Picture
- Product Images
- News Thumbnails
- Movie Posters
- Banner Images

Efficient image loading improves performance and user experience.

---

# Android

Popular image loading libraries:

- Coil ⭐⭐⭐⭐⭐
- Glide ⭐⭐⭐⭐⭐
- Picasso ⭐⭐⭐☆☆

Modern Android applications mostly use:

- Coil

---

# React Native

Popular image loading libraries:

- Image (Built-in)
- react-native-fast-image ⭐⭐⭐⭐⭐

Most production applications use:

- FastImage

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Coil | FastImage |
| Glide | FastImage |
| Picasso | Image |
| AsyncImage | FastImage |
| painterResource() | require() |
| rememberAsyncImagePainter() | FastImage |

---

# Built-in Image Component

React Native provides an Image component.

Example

```tsx
<Image
    source={{
        uri: "https://example.com/profile.png"
    }}
/>
```

It is suitable for small applications.

---

# FastImage

FastImage is the most popular image loading library.

Features

- Memory Cache
- Disk Cache
- Faster Loading
- Better Performance
- Priority Loading
- Preloading

Example

```tsx
<FastImage
    source={{
        uri: imageUrl
    }}
/>
```

---

# Image Loading Flow

Android

```
UI

↓

Coil

↓

Memory Cache

↓

Disk Cache

↓

Network
```

---

React Native

```
Image

↓

FastImage

↓

Memory Cache

↓

Disk Cache

↓

Network
```

The flow is almost identical.

---

# Memory Cache

Memory Cache stores recently loaded images in RAM.

Advantages

- Very Fast
- No Internet Required
- Smooth Scrolling

---

# Disk Cache

Disk Cache stores images inside device storage.

Advantages

- Images remain available after the app restarts.
- Reduces network requests.
- Improves loading speed.

---

# Cache Flow

```
Request Image

↓

Memory Cache

↓

Disk Cache

↓

Download from Server

↓

Store in Memory

↓

Store on Disk
```

This is the same concept used by Coil.

---

# Local Images

Android

```kotlin
painterResource(
    R.drawable.logo
)
```

---

React Native

```tsx
<Image
    source={require("./assets/logo.png")}
/>
```

---

# Remote Images

Android

```kotlin
AsyncImage(
    model = imageUrl
)
```

---

React Native

```tsx
<Image
    source={{
        uri: imageUrl
    }}
/>
```

---

# Placeholder Image

Shown while the image is loading.

Android

```kotlin
placeholder(...)
```

---

React Native

```tsx
<FastImage
    defaultSource={require("./placeholder.png")}
/>
```

---

# Error Image

Shown if image loading fails.

Android

```kotlin
error(...)
```

---

React Native

```tsx
onError={() => {

}}
```

You can display a fallback image when loading fails.

---

# Image Resize Modes

React Native provides:

```
cover
contain
stretch
center
repeat
```

Example

```tsx
<Image

resizeMode="cover"

 />
```

---

# Image Prefetching

Download images before they are displayed.

React Native

```tsx
FastImage.preload([
    {
        uri: imageUrl
    }
])
```

Useful for:

- Product Lists
- News Apps
- Gallery Apps

---

# Lazy Loading

Images are loaded only when they become visible.

Android

```
LazyColumn
```

---

React Native

```
FlatList
```

FlatList automatically loads visible items efficiently.

---

# Folder Structure

```
src/

assets/

    images/

    icons/

components/

    UserImage.tsx

    ProductImage.tsx
```

Store reusable image components inside the `components` folder.

---

# Best Practices

✅ Use FastImage for production apps.

✅ Cache remote images.

✅ Use placeholders while loading.

✅ Show fallback images on errors.

✅ Compress large images before uploading.

✅ Use FlatList for large image lists.

---

# Interview Questions

### Which library is commonly used for image loading?

FastImage.

---

### What is similar to Coil?

FastImage.

---

### What is similar to Glide?

FastImage.

---

### What is similar to AsyncImage?

FastImage.

---

### Why is caching important?

It improves performance, reduces network usage, and provides a smoother user experience.

---

### What are the two main types of image cache?

- Memory Cache
- Disk Cache

---

# Summary

React Native provides a built-in Image component for basic image loading. For production applications, **react-native-fast-image** is preferred because it offers efficient memory caching, disk caching, placeholder support, and better performance—similar to Coil or Glide in Android.
