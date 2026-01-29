<div align="center">
  
# 🔐 Axiom

### Your Files. Your Keys. Your Privacy.

**End-to-End Encrypted Cloud Storage Built with Flutter**

[![Flutter](https://img.shields.io/badge/Flutter-3.0+-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-3.0+-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
[![Platform](https://img.shields.io/badge/Platform-Android%20|%20iOS%20|%20Windows%20|%20macOS%20|%20Linux-lightgrey?style=for-the-badge)](https://github.com/himanshuchaurasiya24/axiom)
[![Version](https://img.shields.io/badge/Version-3.0.0-blue?style=for-the-badge)]()

*A proprietary encrypted storage solution for modern privacy-conscious users*

</div>

---

## 🎯 Overview

**Axiom** is a next-generation encrypted cloud storage application that puts *you* in complete control of your data. Unlike traditional cloud providers, Axiom implements **true client-side encryption** - meaning your files are encrypted on your device before they ever leave, and only you hold the keys.

### Why Axiom?

In an era of constant data breaches and privacy violations, Axiom offers peace of mind:

- 🔑 **You Hold the Keys** - Not the server, not the cloud provider. Just you.
- 🔐 **Encrypted Before Upload** - AES-256-GCM encryption happens on your device
- 🚫 **Zero Server Access** - Even if servers are compromised, your data remains encrypted
- 🎯 **Cross-Platform** - Native performance on Android, iOS, Windows, macOS, and Linux
- 🚀 **Optimized Performance** - Smart encryption strategies for files of all sizes

---

## 📸 Application Screenshots

<div align="center">

### Splash Screen & Authentication

<img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/splash.png" alt="Splash Screen" width="45%"/> <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/login.png" alt="Login Screen" width="45%"/>

### Dashboard & File Management

<img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/dashboard.png" alt="Dashboard" width="45%"/> <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/files.png" alt="File List" width="45%"/>

### Real-Time Decryption

<img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/decrypting.png" alt="Decryption Progress" width="45%"/>

*Modern, intuitive interface with real-time encryption/decryption progress*

</div>

---

## ✨ Core Features

### 🔒 **Military-Grade Security**

- **AES-256-GCM Encryption**: Industry-standard authenticated encryption for all files
- **Client-Side Only**: Files are encrypted on your device before upload
- **Zero-Knowledge Architecture**: Your encryption keys never touch our servers
- **HKDF Key Derivation**: Secure derivation of Device Encryption Keys (DEK)
- **Secure Memory Management**: Multi-pass overwrite for temporary files
- **Screenshot Protection**: Prevents screenshots on Windows, macOS, and iOS

### 📁 **Smart File Management**

- **Intelligent Processing**:
  - Small files (<50MB): RAM-only encryption for speed
  - Large files (>50MB): Optimized disk streaming to handle any size
- **Category Organization**: Organize files into custom categories
- **Universal File Viewer**: 
  - Images (JPG, PNG, WebP, etc.)
  - Videos (MP4, MKV, AVI, etc.)
  - Documents (PDF, TXT, etc.)
  - Audio files
- **Batch Operations**: Upload and download multiple files simultaneously
- **Duplicate Detection**: Automatic file renaming to prevent overwrites

### 🚀 **Performance & UX**

- **Background Processing**: Operations continue even when app is minimized
- **Real-Time Progress Indicators**:
  - Dual-phase tracking (Download + Decrypt / Encrypt + Upload)
  - Live speed monitoring
  - Accurate completion estimates
- **Responsive Interface**: 
  - Smooth 60 FPS animations
  - Instant feedback on all interactions
  - Adaptive layouts for all screen sizes
- **Robust Cancellation**: Clean cancellation support with proper cleanup

### 🛡️ **Privacy & Safety**

- **App Lock**: Automatic blur screen when backgrounded
- **Secure Session Management**: Auto-logout on security events
- **No Analytics**: Zero tracking, telemetry, or data collection
- **Platform Security**: Integration with system keychains and secure storage
- **Account Protection**: Built-in account lock and subscription management

---

## 🔐 Security Architecture

### Encryption Workflow

```
┌─────────────────┐
│   User File     │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Generate Random │  16-byte Initialization Vector (IV)
│       IV        │  Unique per file
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  AES-256-GCM    │  Algorithm: AES-256 in GCM mode
│  Encryption     │  Key: Device Encryption Key (DEK)
│                 │  Tag: 16-byte authentication tag
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Encrypted File  │  Format: [IV(16) + Ciphertext + Tag(16)]
│ Upload to Server│  Server stores encrypted blob only
└─────────────────┘
```

### Key Management

- **Master Key**: Stored in platform-specific secure storage (Keychain/KeyStore)
- **Device Encryption Key (DEK)**: Derived from master key using HKDF with salt
- **File-Level IVs**: Unique random IV generated for each file upload
- **No Key Transmission**: Keys never leave your device or touch the network

### Data Flow

1. **Upload**: File → Encrypt (Client) → Upload (Encrypted) → Server Storage
2. **Download**: Server → Download (Encrypted) → Decrypt (Client) → File
3. **Viewing**: Download → Decrypt → Secure Temp Storage → View → Secure Wipe

---

## 🛠️ Technical Stack

<div align="center">

| Category | Technology |
|----------|------------|
| **Framework** | Flutter 3.0+ |
| **Language** | Dart 3.0+ |
| **State Management** | Riverpod |
| **Encryption** | PointyCastle (AES-256-GCM) |
| **Key Derivation** | HKDF (HMAC-based KDF) |
| **Video Playback** | Media Kit |
| **PDF Rendering** | syncfusion_flutter_pdfviewer |
| **HTTP Client** | Dio with interceptors |
| **Secure Storage** | flutter_secure_storage |
| **Platform Channels** | Native integration (Android/iOS/Desktop) |

</div>

---

## 🎨 Design Philosophy

Axiom combines **security** with **usability**:

- **Modern UI**: Sleek dark theme with cyan/purple accents
- **Intuitive Navigation**: Clear visual hierarchy and consistent patterns
- **Responsive Feedback**: Real-time progress and status updates
- **Cross-Platform Consistency**: Native feel on every platform
- **Accessibility**: Semantic labels and keyboard navigation support

---

## 🚀 Performance Optimizations

### Encryption Strategy

- **Small Files (<50MB)**: Complete RAM-based encryption/decryption for instant processing
- **Large Files (>50MB)**: Chunked streaming (5MB chunks) to handle files of any size without memory overflow

### Background Processing

- Uses Dart **Isolates** for true parallel processing
- Operations continue during:
  - App minimization
  - Screen lock
  - Task switching
- **AxiomBackgroundService** maintains foreground notification to prevent OS termination

### UI Responsiveness

- Progress updates throttled to 50ms for smooth animations
- Smart dummy progress (0-60%) for instant feedback
- Explicit event loop yielding to prevent UI freezing
- Cancellation checks at every critical point

---

## 🔄 Roadmap

### Upcoming Features

- 📱 **Mobile-First Updates**: Enhanced touch gestures and mobile UX
- 🔗 **File Sharing**: Secure encrypted sharing with time-limited access
- 📊 **Usage Analytics Dashboard**: Storage trends and file insights (client-side only)
- 🌐 **Web Interface**: Responsive web client for browser access
- 🔍 **Full-Text Search**: Encrypted search across file contents
- 🎨 **Themes**: Light mode and custom theme support
- 🗂️ **Advanced Filters**: Smart filters and saved searches

---

## 📞 Support & Contact

For support, feature requests, or inquiries:

- **Email**: support@axiomvault.com
- **Developer**: [Himanshu Chaurasiya](https://github.com/himanshuchaurasiya24)

---

## 📄 Legal

### Copyright

© 2026 Himanshu Chaurasiya. All rights reserved.

This is proprietary software. Unauthorized copying, distribution, or modification is strictly prohibited.

### Privacy Policy

Axiom follows a strict **zero-knowledge** policy:
- We cannot access your encrypted files
- We do not collect analytics or telemetry
- We do not sell or share user data
- Encryption keys are stored locally only

---

<div align="center">

### 🔐 Built with Privacy in Mind

**Axiom** - *Your Secure Digital Vault*

**Version 3.0.0** | **Powered by Flutter** | **Encrypted with AES-256-GCM**

---

Made with 🔒 by [Himanshu Chaurasiya](https://github.com/himanshuchaurasiya24)

</div>

