# 26. Testing

## What is Testing?

Testing ensures that an application works correctly before it reaches users.

Benefits

- Finds bugs early
- Prevents regressions
- Improves code quality
- Makes refactoring safer
- Increases confidence during releases

Popular Apps

- WhatsApp
- Amazon
- Flipkart
- Netflix
- Google Pay

All production applications have automated tests.

---

# Android

Popular testing libraries

- JUnit ⭐⭐⭐⭐⭐
- Mockito ⭐⭐⭐⭐⭐
- Espresso ⭐⭐⭐⭐⭐
- JaCoCo ⭐⭐⭐⭐☆

Most Android applications use

- JUnit
- Mockito
- Espresso

---

# React Native

Popular testing libraries

- Jest ⭐⭐⭐⭐⭐
- React Native Testing Library ⭐⭐⭐⭐⭐
- Detox ⭐⭐⭐⭐⭐

Most production applications use

- Jest
- React Native Testing Library
- Detox

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| JUnit | Jest |
| Mockito | Jest Mock |
| Espresso | React Native Testing Library |
| UI Test | Component Test |
| JaCoCo | Jest Coverage |
| Instrumentation Test | Detox |

---

# Types of Testing

### Unit Testing

Tests individual functions.

Example

```
calculateTotalPrice()
```

---

### Component Testing

Tests a UI component.

Example

```
Login Button

↓

Click

↓

Navigate
```

---

### Integration Testing

Tests multiple components working together.

Example

```
Login Screen

↓

API

↓

Navigate Home
```

---

### End-to-End Testing

Tests the complete application.

Example

```
Launch App

↓

Login

↓

Open Product

↓

Add To Cart

↓

Checkout
```

---

# Jest

Jest is the most popular testing framework.

Used for

- Unit Tests
- Component Tests
- Mock Functions
- Coverage Reports

Example

```typescript
test("Addition", () => {

});
```

---

# Mocking

Sometimes we don't want to call the real API.

Instead

```
API

↓

Mock Response

↓

Test
```

Jest provides built-in mocking support.

---

# Component Testing

React Native Testing Library

Tests

- Buttons
- Text
- User Input
- Navigation
- Screen Rendering

Very similar to Espresso UI testing.

---

# Snapshot Testing

Snapshot Testing captures the UI structure.

Future test runs compare the current UI against the saved snapshot.

Useful for detecting unexpected UI changes.

---

# End-to-End Testing

Detox is commonly used.

Flow

```
Launch App

↓

Tap Button

↓

Enter Text

↓

Verify Screen

↓

Success
```

---

# Coverage

Coverage measures how much code is tested.

Typical metrics

- Statements
- Functions
- Branches
- Lines

Higher coverage generally provides better confidence, but quality of tests is more important than percentage alone.

---

# Testing Flow

```
Write Code

↓

Write Test

↓

Run Tests

↓

Fix Bugs

↓

Deploy
```

---

# Folder Structure

```
src/

components/

hooks/

services/

__tests__/

    Login.test.tsx

    Home.test.tsx

    Product.test.tsx
```

---

# Best Practices

✅ Write unit tests for business logic.

✅ Test user interactions.

✅ Mock network requests.

✅ Keep tests independent.

✅ Run tests in CI/CD.

✅ Maintain meaningful test coverage.

---

# Interview Questions

### Which testing framework is commonly used?

Jest.

---

### Which library is similar to Espresso?

React Native Testing Library.

---

### Which library is used for End-to-End testing?

Detox.

---

### Why use mocks?

To avoid calling real APIs during tests.

---

### What is Snapshot Testing?

It compares the current UI against a previously saved snapshot to detect unexpected changes.

---

### Why is testing important?

To improve application quality and reduce bugs.

---

# Real Project Example

Shopping App

```
Login Screen

↓

Enter Email

↓

Enter Password

↓

Click Login

↓

Mock API

↓

Navigate Home

↓

Test Passed
```

---

# Summary

React Native applications commonly use **Jest** for unit testing, **React Native Testing Library** for component testing, and **Detox** for end-to-end testing. Android developers can think of these as the equivalents of **JUnit**, **Espresso**, and instrumentation tests, making testing concepts highly transferable.
