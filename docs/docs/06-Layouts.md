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
