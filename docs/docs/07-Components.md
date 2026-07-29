# 7. Components

## What are Components?

Components are reusable building blocks used to create the User Interface (UI).

Everything you see on the screen is made up of components.

Examples:

- Text
- Images
- Buttons
- Lists
- Text Fields
- Cards

---

# Android Components

Android provides many UI components.

Some common ones are:

- TextView
- ImageView
- Button
- EditText
- RecyclerView
- ScrollView
- CardView
- CheckBox
- RadioButton
- Switch
- ProgressBar

Jetpack Compose provides modern equivalents.

---

# React Native Components

React Native also provides built-in components.

Some common ones are:

- Text
- Image
- Button
- Pressable
- TextInput
- FlatList
- ScrollView
- View
- Switch
- ActivityIndicator

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| TextView | Text |
| ImageView | Image |
| Button | Button |
| MaterialButton | Pressable |
| EditText | TextInput |
| RecyclerView | FlatList |
| LazyColumn | FlatList |
| LazyRow | FlatList (horizontal) |
| ScrollView | ScrollView |
| CardView | View |
| CheckBox | CheckBox (Community Library) |
| RadioButton | Community Library |
| Switch | Switch |
| ProgressBar | ActivityIndicator |
| FloatingActionButton | Pressable |
| Toolbar | Custom Header |

---

# Text

## Android

```kotlin
Text(
    text = "Hello Android"
)
```

---

## React Native

```tsx
<Text>
    Hello React Native
</Text>
```

---

# Image

## Android

```kotlin
Image(
    painter = painterResource(...)
)
```

---

## React Native

```tsx
<Image
    source={require("./logo.png")}
/>
```

---

# Button

## Android

```kotlin
Button(
    onClick = {}
)
```

---

## React Native

```tsx
<Button
    title="Login"
    onPress={() => {}}
/>
```

---

# Pressable

Used for creating fully customizable buttons.

```tsx
<Pressable onPress={() => {}}>
    <Text>Login</Text>
</Pressable>
```

Most production applications use **Pressable** instead of Button.

---

# TextInput

Android

```kotlin
TextField(
    value = name
)
```

---

React Native

```tsx
<TextInput
    placeholder="Enter Name"
/>
```

---

# FlatList

FlatList is used for displaying lists efficiently.

Android

```kotlin
LazyColumn {

}
```

---

React Native

```tsx
<FlatList
    data={users}
    renderItem={({ item }) => (
        <Text>{item.name}</Text>
    )}
/>
```

---

# ScrollView

Used when the content needs to scroll.

Android

```kotlin
Column(
    modifier = Modifier.verticalScroll()
)
```

---

React Native

```tsx
<ScrollView>

</ScrollView>
```

---

# View

View is the most important component.

It acts like:

- Box
- LinearLayout
- FrameLayout

Everything is usually placed inside a View.

Example

```tsx
<View>

</View>
```

---

# Switch

Android

```kotlin
Switch(
    checked = true
)
```

---

React Native

```tsx
<Switch
    value={true}
/>
```

---

# ActivityIndicator

Android

```kotlin
CircularProgressIndicator()
```

---

React Native

```tsx
<ActivityIndicator
    size="large"
/>
```

---

# Card

Android

```kotlin
Card {

}
```

---

React Native

Cards are usually created using:

```tsx
<View style={styles.card}>

</View>
```

Example Style

```tsx
const styles = StyleSheet.create({
    card:{
        backgroundColor:"#fff",
        borderRadius:10,
        padding:16,
        elevation:5
    }
})
```

---

# Touchable Components

React Native provides multiple touchable components.

- Button
- Pressable ⭐⭐⭐⭐⭐
- TouchableOpacity
- TouchableHighlight

Most modern applications prefer **Pressable**.

---

# Component Hierarchy

Android

```
Activity

↓

Composable

↓

Button
```

React Native

```
Screen

↓

View

↓

Button
```

---

# Best Practices

✅ Create reusable components.

✅ Keep components small.

✅ Avoid duplicate UI.

✅ Separate UI from business logic.

✅ Prefer Pressable over Button for custom designs.

---

# Interview Questions

### What is similar to TextView?

Text.

---

### What is similar to RecyclerView?

FlatList.

---

### What is similar to EditText?

TextInput.

---

### Which component is used to display images?

Image.

---

### Which component is used for custom clickable views?

Pressable.

---

### Which component is used for loading indicators?

ActivityIndicator.

---

# Summary

React Native provides a rich set of built-in components that closely match Android UI components. While the names differ, the purpose remains almost the same. Android developers can quickly become productive by understanding these one-to-one mappings.
