# 36. File Handling

## What is File Handling?

File Handling is the process of

- Reading Files
- Writing Files
- Downloading Files
- Uploading Files
- Sharing Files
- Deleting Files

Examples

- Upload Profile Picture
- Download PDF Invoice
- Share Image
- Select Resume
- Upload Aadhaar/PAN

---

# Android

Popular APIs

- Storage Access Framework
- File API
- DownloadManager
- ContentResolver

---

# React Native

Popular libraries

- react-native-fs
- react-native-document-picker
- react-native-image-picker
- react-native-share

---

# Android vs React Native

| Android | React Native |
|----------|--------------|
| File API | react-native-fs |
| DownloadManager | react-native-fs |
| ContentResolver | Document Picker |
| Image Picker | react-native-image-picker |
| Share Intent | react-native-share |

---

# Common Operations

- Read File
- Write File
- Delete File
- Copy File
- Move File
- Rename File

---

# Reading Files

Read

- PDF
- TXT
- JSON
- Images

React Native

```
react-native-fs
```

---

# Writing Files

Examples

- Save Invoice
- Save Report
- Export Data

---

# Download Files

Common downloads

- PDF
- Images
- Videos
- Documents

Flow

```
API

↓

Download

↓

Local Storage

↓

Open File
```

---

# Upload Files

Examples

- Resume
- Passport
- Aadhaar
- PAN
- Product Images

Flow

```
Select File

↓

Upload API

↓

Backend

↓

Success
```

---

# Image Picker

Popular library

```
react-native-image-picker
```

Supports

- Camera
- Gallery

---

# Document Picker

Popular library

```
react-native-document-picker
```

Supports

- PDF
- DOC
- DOCX
- XLS
- PPT
- ZIP

---

# File Sharing

Popular library

```
react-native-share
```

Examples

- Share PDF
- Share Image
- Share Invoice

Flow

```
Select File

↓

Share Sheet

↓

WhatsApp

↓

Email

↓

Drive
```

---

# File System

React Native uses

```
react-native-fs
```

Supports

- Read
- Write
- Copy
- Delete
- Move
- Create Folder

---

# Folder Structure

```
src/

services/

FileService.ts

screens/

utils/
```

---

# Architecture

```
UI

↓

File Service

↓

File System

↓

Storage
```

---

# Best Practices

✅ Request storage permission only when needed.

✅ Validate file type.

✅ Validate file size.

✅ Show upload/download progress.

✅ Delete temporary files.

✅ Handle failures gracefully.

---

# Interview Questions

### Which library is used for file operations?

react-native-fs.

---

### Which library is used to select documents?

react-native-document-picker.

---

### Which library is used to select images?

react-native-image-picker.

---

### Which library is used for file sharing?

react-native-share.

---

### Can React Native upload files?

Yes.

Using multipart/form-data with Axios or Fetch API.

---

### Why validate file size?

To improve performance and avoid uploading unsupported files.

---

# Real Project Example

Document Upload App

```
User Selects PDF

↓

Document Picker

↓

Validate File

↓

Upload API

↓

Backend

↓

Success
```

---

# Another Example

Invoice Download

```
User Clicks Download

↓

API

↓

react-native-fs

↓

Store PDF

↓

Open PDF

↓

Share
```

---

# Summary

React Native provides libraries such as **react-native-fs**, **react-native-document-picker**, **react-native-image-picker**, and **react-native-share** to manage files. Android developers can think of these as equivalents to the **File API**, **Storage Access Framework**, **DownloadManager**, and **Share Intents**, making it straightforward to implement file upload, download, and sharing features.
