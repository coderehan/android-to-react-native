# 37. Dependency Management

## What is Dependency Management?

Dependency Management is the process of adding, updating, and maintaining external libraries used by an application.

Examples

- Axios
- React Navigation
- Zustand
- Firebase
- Reanimated

Instead of writing everything from scratch, we use well-tested libraries.

---

# Android

Dependency Manager

- Gradle

Example

implementation("com.squareup.retrofit2:retrofit:2.11.0")

---

# React Native

Dependency Managers

- npm
- Yarn

Example

npm install axios

or

yarn add axios

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| Gradle | npm / Yarn |
| build.gradle | package.json |
| implementation() | npm install |
| Gradle Cache | node_modules |
| Gradle Sync | npm install |

---

# package.json

The most important file in every React Native project.

Contains

- Project Name
- Version
- Dependencies
- Scripts

Example

```json
{
  "dependencies": {
    "axios": "^1.12.0",
    "react-navigation": "^7.0.0"
  }
}
```

---

# package-lock.json

Generated automatically by npm.

Purpose

- Locks exact dependency versions.
- Ensures every developer installs the same versions.

Commit this file to Git.

---

# node_modules

Contains all installed packages.

Example

```
project/

node_modules/

package.json

package-lock.json
```

Do NOT edit files inside node_modules.

---

# Installing Packages

Install a package

```bash
npm install axios
```

or

```bash
yarn add axios
```

---

# Installing Development Packages

Development-only dependency

```bash
npm install --save-dev jest
```

Example

- Jest
- ESLint
- Prettier

---

# Removing Packages

```bash
npm uninstall axios
```

or

```bash
yarn remove axios
```

---

# Updating Packages

Update a package

```bash
npm update
```

or

```bash
npm install axios@latest
```

---

# Semantic Versioning (SemVer)

Format

```
MAJOR.MINOR.PATCH
```

Example

```
1.5.2
```

Meaning

- MAJOR → Breaking changes
- MINOR → New features
- PATCH → Bug fixes

---

# Version Symbols

```
^1.2.0
```

Allows compatible minor and patch updates.

```
~1.2.0
```

Allows only patch updates.

```
1.2.0
```

Uses exactly that version.

---

# Dependency Installation Flow

```
package.json

↓

npm install

↓

node_modules

↓

Application Ready
```

---

# Dependency Updates

Before updating

↓

Read Release Notes

↓

Check Breaking Changes

↓

Update

↓

Test Application

Never update packages blindly.

---

# Folder Structure

```
project/

package.json

package-lock.json

node_modules/
```

---

# Best Practices

✅ Keep dependencies updated.

✅ Remove unused libraries.

✅ Commit package-lock.json.

✅ Use stable versions.

✅ Read release notes before upgrading.

✅ Avoid adding unnecessary packages.

---

# Interview Questions

### Which file stores dependencies?

package.json.

---

### Which package managers are commonly used?

npm and Yarn.

---

### What is node_modules?

The folder containing all installed libraries.

---

### Why is package-lock.json important?

It locks exact dependency versions for consistent builds.

---

### What is SemVer?

Semantic Versioning using

MAJOR.MINOR.PATCH.

---

### Should node_modules be committed to Git?

No.

Only commit package.json and package-lock.json.

---

# Real Project Example

Shopping App

```
Developer

↓

npm install

↓

Download Packages

↓

node_modules

↓

Build Project

↓

Run Application
```

---

# Summary

React Native manages external libraries using **npm** or **Yarn**. Dependencies are listed in **package.json**, installed into the **node_modules** folder, and version-locked using **package-lock.json**. Android developers can think of this as the equivalent of **Gradle**, **build.gradle**, and the Gradle dependency cache.
