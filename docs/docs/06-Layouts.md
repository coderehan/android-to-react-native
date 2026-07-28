# 6. Layouts

## What is a Layout?

A layout defines how UI components are arranged on the screen.

It controls:

- Position
- Size
- Alignment
- Spacing

---

# Android

Android provides multiple layout types.

- LinearLayout
- ConstraintLayout
- FrameLayout
- RelativeLayout
- CoordinatorLayout

Modern Android (Jetpack Compose):

- Column
- Row
- Box

---

# React Native

React Native mainly uses:

- View
- Flexbox

Everything is built using **View** and Flexbox properties.

Unlike Android, there are no separate Row or Column widgets.

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Column | View + flexDirection: "column" |
| Row | View + flexDirection: "row" |
| Box | View |
| LinearLayout | View |
| ConstraintLayout | Flexbox |
| FrameLayout | View |

---

# Column

## Android (Compose)

```kotlin
Column {
    Text("One")
    Text("Two")
}
```

---

## React Native

```tsx
<View
  style={{
    flexDirection: "column"
  }}>
  <Text>One</Text>
  <Text>Two</Text>
</View>
```

---

# Row

## Android

```kotlin
Row {
    Text("One")
    Text("Two")
}
```

---

## React Native

```tsx
<View
  style={{
    flexDirection: "row"
  }}>
  <Text>One</Text>
  <Text>Two</Text>
</View>
```

---

# Box

## Android

```kotlin
Box {

}
```

---

## React Native

```tsx
<View>

</View>
```

View acts like Box.

---

# Flex Direction

Defines how children are arranged.

Column

```tsx
flexDirection: "column"
```

Row

```tsx
flexDirection: "row"
```

---

# justifyContent

Controls alignment on the **Main Axis**.

Available values

```
flex-start
center
flex-end
space-between
space-around
space-evenly
```

Example

```tsx
<View
  style={{
    justifyContent: "center"
  }}>
</View>
```

---

# alignItems

Controls alignment on the **Cross Axis**.

Values

```
flex-start
center
flex-end
stretch
```

Example

```tsx
<View
  style={{
    alignItems: "center"
  }}>
</View>
```

---

# Weight vs Flex

Android

```kotlin
Modifier.weight(1f)
```

---

React Native

```tsx
flex: 1
```

Example

```tsx
<View style={{ flex: 1 }}>
```

---

# Padding

Android

```kotlin
Modifier.padding(16.dp)
```

---

React Native

```tsx
padding: 16
```

---

# Margin

Android

```kotlin
Modifier.padding()
```

or XML

```
layout_margin
```

---

React Native

```tsx
margin: 16
```

---

# Fill Max Size

Android

```kotlin
Modifier.fillMaxSize()
```

---

React Native

```tsx
flex: 1
```

---

# Width

Android

```kotlin
Modifier.fillMaxWidth()
```

---

React Native

```tsx
width: "100%"
```

---

# Height

Android

```kotlin
Modifier.fillMaxHeight()
```

---

React Native

```tsx
height: "100%"
```

---

# Centering

Android

```kotlin
contentAlignment = Alignment.Center
```

---

React Native

```tsx
justifyContent: "center",
alignItems: "center"
```

---

# Spacing

Android

```kotlin
Spacer()
```

---

React Native

```tsx
margin
padding
gap
```

---

# Complete Example

Android

```kotlin
Column(
    modifier = Modifier.fillMaxSize(),
    horizontalAlignment = Alignment.CenterHorizontally,
    verticalArrangement = Arrangement.Center
) {
    Text("Hello")
}
```

---

React Native

```tsx
<View
    style={{
        flex:1,
        justifyContent:"center",
        alignItems:"center"
    }}>
    <Text>Hello</Text>
</View>
```

---

# Best Practices

✅ Use Flexbox.

✅ Prefer reusable styles.

✅ Avoid deeply nested Views.

✅ Keep layouts simple.

✅ Use StyleSheet.create().

---

# Interview Questions

### Which layout system does React Native use?

Flexbox.

---

### Which component is used for layouts?

View.

---

### What is similar to Column?

View with

```
flexDirection: "column"
```

---

### What is similar to Row?

View with

```
flexDirection: "row"
```

---

### What is similar to Modifier.weight()?

```
flex:1
```

---

# Summary

Android uses multiple layout types like Column, Row, Box, and ConstraintLayout.

React Native mainly uses **View** with **Flexbox**, making one flexible layout system capable of handling almost every UI design.
