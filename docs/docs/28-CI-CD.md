# 28. CI/CD

## What is CI/CD?

CI/CD stands for

- Continuous Integration (CI)
- Continuous Delivery / Continuous Deployment (CD)

It automates the process of:

- Building the application
- Running tests
- Generating APK/AAB/IPA
- Deploying to Play Store and App Store

Without CI/CD, developers perform these tasks manually.

---

# Android

Popular CI/CD tools

- GitHub Actions ⭐⭐⭐⭐⭐
- Jenkins ⭐⭐⭐⭐⭐
- Bitrise ⭐⭐⭐⭐☆
- GitLab CI ⭐⭐⭐⭐☆
- Fastlane ⭐⭐⭐⭐⭐

Most Android applications use

- GitHub Actions
- Fastlane

---

# React Native

Popular CI/CD tools

- GitHub Actions ⭐⭐⭐⭐⭐
- Fastlane ⭐⭐⭐⭐⭐
- Bitrise ⭐⭐⭐⭐⭐
- Codemagic ⭐⭐⭐⭐⭐
- Jenkins ⭐⭐⭐⭐☆

Most production applications use

- GitHub Actions
- Fastlane
- Codemagic

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Gradle Build | Gradle + Xcode Build |
| APK / AAB | APK / AAB / IPA |
| Fastlane | Fastlane |
| GitHub Actions | GitHub Actions |
| Play Store Upload | Play Store + App Store Upload |

---

# CI Pipeline

```
Developer Pushes Code

↓

GitHub

↓

Run Build

↓

Run Tests

↓

Generate APK / AAB

↓

Deploy
```

---

# Continuous Integration

Every code push automatically

- Builds the project
- Runs unit tests
- Checks code quality

If anything fails,

↓

Build Failed

---

# Continuous Delivery

After successful build

↓

Generate

- APK
- AAB
- IPA

Ready for release.

---

# Continuous Deployment

After successful testing

↓

Automatically publish

- Play Store
- App Store

---

# GitHub Actions

GitHub Actions is one of the most popular CI/CD platforms.

Typical Workflow

```
Push Code

↓

Checkout Repository

↓

Install Dependencies

↓

Run Tests

↓

Build App

↓

Upload Artifact
```

---

# Fastlane

Fastlane automates

- Build
- Signing
- Screenshots
- Play Store Upload
- App Store Upload

Most production teams use Fastlane.

---

# Codemagic

Codemagic is a CI/CD platform designed specifically for Flutter and React Native.

Supports

- Android
- iOS
- Automatic Signing
- Store Deployment

---

# Build Artifacts

Android

```
APK

AAB
```

iOS

```
IPA
```

Artifacts can be downloaded or uploaded automatically.

---

# Automated Testing

Before deployment

↓

Run

- Jest
- Detox

If tests fail,

↓

Stop Deployment

---

# Deployment Flow

```
Developer

↓

GitHub

↓

CI Pipeline

↓

Build

↓

Tests

↓

Generate APK

↓

Play Store
```

---

# Folder Structure

```
.github/

workflows/

    android.yml

    ios.yml

fastlane/

    Fastfile

    Appfile
```

---

# Best Practices

✅ Run tests automatically.

✅ Keep secrets outside the repository.

✅ Automate build signing.

✅ Fail the pipeline if tests fail.

✅ Generate release artifacts automatically.

✅ Use separate pipelines for Android and iOS.

---

# Interview Questions

### What is CI?

Continuous Integration automatically builds and tests code after every commit.

---

### What is CD?

Continuous Delivery/Deployment automates application release.

---

### Which CI/CD platform is commonly used?

GitHub Actions.

---

### Which tool automates Play Store uploads?

Fastlane.

---

### Which platform is popular for React Native?

Codemagic.

---

### Why use CI/CD?

- Faster Releases
- Fewer Manual Errors
- Better Code Quality
- Consistent Builds

---

# Real Project Example

Shopping App

```
Developer Pushes Code

↓

GitHub Actions

↓

Install Dependencies

↓

Run Jest Tests

↓

Build Android & iOS

↓

Fastlane

↓

Play Store

↓

App Store
```

---

# Summary

React Native applications commonly use **GitHub Actions**, **Fastlane**, and **Codemagic** to automate building, testing, signing, and deploying applications. Android developers will find the workflow very familiar, with the main addition being support for iOS builds and App Store deployment alongside Android releases.
