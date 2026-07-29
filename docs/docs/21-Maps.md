# 21. Maps

## What are Maps?

Maps allow applications to display geographical locations and help users navigate.

Common use cases:

- Current Location
- Delivery Tracking
- Nearby Restaurants
- Ride Booking
- Route Navigation
- Store Locator

Examples

- Google Maps
- Uber
- Ola
- Swiggy
- Zomato

---

# Android

Popular map libraries

- Google Maps SDK ⭐⭐⭐⭐⭐
- Google Maps Compose ⭐⭐⭐⭐⭐

Most modern Android apps use:

- Google Maps SDK
- Google Maps Compose

---

# React Native

Popular map libraries

- react-native-maps ⭐⭐⭐⭐⭐
- react-native-geolocation-service ⭐⭐⭐⭐☆

Most production applications use:

- react-native-maps

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Google Maps SDK | react-native-maps |
| GoogleMap | MapView |
| Marker | Marker |
| CameraPosition | Region |
| Polyline | Polyline |
| Fused Location Provider | react-native-geolocation-service |

---

# Maps Flow

```
Open Map

↓

Request Location Permission

↓

Get Current Location

↓

Move Camera

↓

Show Marker

↓

User Interaction
```

---

# MapView

Android

```kotlin
GoogleMap
```

---

React Native

```tsx
<MapView

/>

```

MapView displays the map on the screen.

---

# Marker

Markers indicate locations.

Examples

- User Location
- Restaurant
- Delivery Partner
- Hotel

Android

```kotlin
MarkerOptions()
```

---

React Native

```tsx
<Marker

coordinate={location}

/>
```

---

# Current Location

Flow

```
Request Permission

↓

Get GPS Location

↓

Move Camera

↓

Show Marker
```

---

# Region

Region defines the visible area of the map.

Example

```tsx
<MapView

initialRegion={...}

/>
```

---

# Camera Movement

Android

```kotlin
moveCamera(...)
```

---

React Native

```tsx
mapRef.current.animateToRegion(...)
```

Moves the camera smoothly.

---

# Polyline

A Polyline draws a route between locations.

Examples

- Uber Route
- Delivery Route
- Navigation

React Native

```tsx
<Polyline

coordinates={route}

/>
```

---

# Directions

Typical Flow

```
Pickup

↓

Google Directions API

↓

Route Points

↓

Polyline

↓

Display Route
```

---

# Current User Location

React Native

```tsx
showsUserLocation={true}
```

Displays the user's current location on the map.

---

# Live Location Tracking

Flow

```
GPS

↓

Location Updates

↓

Backend

↓

Map Updates

↓

Move Marker
```

Useful for:

- Delivery Apps
- Ride Booking
- Fleet Tracking

---

# Reverse Geocoding

Convert

```
Latitude + Longitude

↓

Address
```

Example

```
12.9716

77.5946

↓

Bengaluru
```

---

# Geocoding

Convert

```
Address

↓

Latitude + Longitude
```

Example

```
Mumbai Airport

↓

19.xxxx

72.xxxx
```

---

# Folder Structure

```
src/

maps/

    MapScreen.tsx

components/

    MapMarker.tsx

hooks/

    useLocation.ts

services/

    LocationService.ts
```

---

# Best Practices

✅ Request location permission only when needed.

✅ Use high accuracy only when required.

✅ Stop location updates when leaving the screen.

✅ Cache frequently used locations.

✅ Optimize marker rendering.

---

# Interview Questions

### Which library is commonly used?

react-native-maps.

---

### What is similar to Google Maps SDK?

react-native-maps.

---

### What is similar to GoogleMap?

MapView.

---

### What is used to display a location?

Marker.

---

### How do you draw a route?

Polyline.

---

### How do you show the user's current location?

```
showsUserLocation={true}
```

---

# Real Project Example

Food Delivery App

```
Restaurant

↓

Delivery Partner

↓

Customer

↓

Google Directions API

↓

Polyline

↓

Live Delivery Tracking
```

---

# Summary

React Native applications commonly use **react-native-maps** for displaying maps. It supports MapView, Markers, Polylines, camera movement, and current location. Android developers can think of it as the equivalent of the Google Maps SDK, making it straightforward to build delivery tracking, ride booking, and navigation features.
