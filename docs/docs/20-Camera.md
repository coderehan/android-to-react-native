# 20. Camera

## What is Camera?

The Camera allows an application to:

- Capture Photos
- Record Videos
- Scan QR Codes
- Scan Barcodes
- Scan Documents
- Verify Identity

Examples

- WhatsApp
- Google Pay
- Paytm
- Flipkart
- Instagram

---

# Android

Popular camera libraries

- CameraX ⭐⭐⭐⭐⭐
- Camera2 API ⭐⭐⭐⭐☆
- ML Kit ⭐⭐⭐⭐⭐

Most modern Android apps use:

- CameraX

---

# React Native

Popular camera libraries

- react-native-vision-camera ⭐⭐⭐⭐⭐
- react-native-image-picker ⭐⭐⭐⭐☆

Most production applications use:

- Vision Camera

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| CameraX | Vision Camera |
| Camera2 API | Vision Camera |
| ActivityResultContracts | launchCamera() |
| ML Kit | Vision Camera + Frame Processor |
| Image Picker | react-native-image-picker |

---

# Camera Flow

```
User Clicks Camera

↓

Check Camera Permission

↓

Open Camera

↓

Capture Photo

↓

Save Image

↓

Display Preview
```

---

# Camera Permission

Before opening the camera,

Request

```
CAMERA
```

permission.

Without permission, the camera cannot be opened.

---

# Android

Example

```kotlin
CameraX
```

is used to:

- Preview Camera
- Capture Images
- Record Videos

---

# React Native

Vision Camera provides

- Camera Preview
- Photo Capture
- Video Recording
- QR Scanner
- Barcode Scanner

---

# Taking Photo

Android

```kotlin
imageCapture.takePicture(...)
```

---

React Native

```typescript
const photo =
    await camera.takePhoto();
```

---

# Recording Video

Android

```kotlin
camera.startRecording()
```

---

React Native

```typescript
camera.startRecording()
```

---

# Stop Recording

Android

```kotlin
camera.stopRecording()
```

---

React Native

```typescript
camera.stopRecording()
```

---

# QR Code Scanner

Popular uses

- UPI Payment
- Login QR
- Event Tickets
- Restaurant Menu

Vision Camera supports QR scanning using Frame Processors.

---

# Barcode Scanner

Examples

- Shopping Apps
- Warehouse Apps
- Delivery Apps

Scan

↓

Barcode

↓

Fetch Product

↓

Display Details

---

# Image Picker

Sometimes users choose an existing image instead of taking a new one.

React Native

```
react-native-image-picker
```

Allows

- Camera
- Gallery

selection.

---

# Typical Camera Flow

```
Open Camera

↓

Capture Image

↓

Compress Image

↓

Upload API

↓

Backend

↓

Success
```

---

# Folder Structure

```
src/

camera/

    CameraScreen.tsx

hooks/

    useCamera.ts

services/

components/

    CameraPreview.tsx
```

---

# Best Practices

✅ Ask for permission only when needed.

✅ Compress large images before uploading.

✅ Handle camera errors gracefully.

✅ Release camera resources when leaving the screen.

✅ Test on real devices.

---

# Interview Questions

### Which camera library is commonly used?

react-native-vision-camera.

---

### Which library is similar to CameraX?

Vision Camera.

---

### Can Vision Camera record videos?

Yes.

---

### Can Vision Camera scan QR codes?

Yes.

Using Frame Processors.

---

### Which library allows selecting images from the gallery?

react-native-image-picker.

---

# Real Project Example

UPI Payment App

```
Tap Scan QR

↓

Check Camera Permission

↓

Open Camera

↓

Scan QR

↓

Extract Payment Details

↓

Confirm Payment
```

---

# Summary

React Native applications commonly use **react-native-vision-camera** for camera functionality. It supports photo capture, video recording, QR code scanning, and barcode scanning, making it comparable to CameraX in Android. For selecting existing photos from the device gallery, **react-native-image-picker** is commonly used.
