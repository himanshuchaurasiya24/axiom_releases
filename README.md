<div align="center">

<img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/logo.svg" width="120px" alt="Axiom Logo"/>

# Axiom

**End-to-End Encrypted Cloud Storage**

Your files. Your keys. Your privacy.

<br/>

[![Platform](https://img.shields.io/badge/platform-android%20%7C%20ios%20%7C%20windows%20%7C%20macos%20%7C%20linux-lightgrey)](#)
[![Flutter](https://img.shields.io/badge/flutter-3.0%2B-blue)](https://flutter.dev)
[![Encryption](https://img.shields.io/badge/encryption-AES--256--GCM-green)](#)

</div>

---

## Overview

Axiom is a secure cloud storage application that puts you in complete control of your data. Every file is encrypted on your device before upload using military-grade AES-256-GCM encryption. Your encryption keys never leave your device, ensuring true zero-knowledge privacy.

## Screenshots

<p align="center">
  <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/splash.png" width="24%" />
  <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/login.png" width="24%" />
  <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/dashboard.png" width="24%" />
  <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/files.png" width="24%" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/himanshuchaurasiya24/axiom_releases/main/assets/screenshots/decrypting.png" width="24%" />
</p>

## Features

### 🔒 Security First
- **Client-Side Encryption** - Files encrypted on your device before upload
- **AES-256-GCM** - Military-grade authenticated encryption
- **Zero-Knowledge** - Your keys never touch our servers
- **HKDF Key Derivation** - Secure cryptographic key generation
- **Screenshot Protection** - Prevents unauthorized screen captures

### 📁 Smart File Management
- **Category Organization** - Organize files into custom categories
- **Universal Viewer** - View images, videos, PDFs, and documents
- **Batch Operations** - Upload and download multiple files at once
- **Intelligent Processing** - Optimized handling for files of any size

### ⚡ Performance
- **Background Processing** - Operations continue when app is minimized
- **Real-Time Progress** - Live encryption/decryption progress tracking
- **Optimized Streaming** - Efficient handling of large files
- **Cross-Platform** - Native performance on all platforms

### 🛡️ Privacy
- **No Analytics** - Zero tracking or telemetry
- **App Lock** - Secure blur when backgrounded
- **Session Management** - Auto-logout on security events
- **Local Keys** - Encryption keys stored locally only

## How It Works

```
┌──────────────┐
│  Your File   │
└──────┬───────┘
       │
       ▼
┌──────────────────────┐
│  Encrypt (AES-256)   │  ← On your device
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│  Upload to Server    │  ← Encrypted only
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│  Secure Storage      │
└──────────────────────┘
```

**Download & Decrypt**
1. Download encrypted file from server
2. Decrypt on your device using your local key
3. View or save the decrypted file

## Technology

- **Framework**: Flutter 3.0+
- **Language**: Dart 3.0+
- **State Management**: Riverpod
- **Encryption**: PointyCastle (AES-256-GCM)
- **Key Derivation**: HKDF
- **Video Playback**: Media Kit
- **PDF Viewer**: Syncfusion

## Supported Platforms

- ✅ Android
- ✅ iOS
- ✅ Windows
- ✅ macOS
- ✅ Linux

## Security Architecture

### Encryption
- **Algorithm**: AES-256 in GCM mode (Galois/Counter Mode)
- **Key Size**: 256 bits
- **IV**: 16-byte random initialization vector (unique per file)
- **Authentication Tag**: 16 bytes for integrity verification

### Key Management
- **Master Key**: Stored in platform keychain (iOS Keychain / Android KeyStore)
- **Device Encryption Key (DEK)**: Derived from master key using HKDF
- **File Encryption**: Each file uses a unique random IV
- **Key Storage**: Keys never leave your device

### File Format
```
[IV (16 bytes)] + [Encrypted Data] + [Authentication Tag (16 bytes)]
```

## Privacy Policy

Axiom follows strict zero-knowledge principles:

- ✅ We **cannot** access your encrypted files
- ✅ We **do not** collect analytics or usage data
- ✅ We **do not** sell or share any user information
- ✅ Encryption keys are **stored locally only**
- ✅ No third-party tracking or advertising

## Support

For support or inquiries:
- **Email**: support@axiomvault.com
- **Developer**: [@himanshuchaurasiya24](https://github.com/himanshuchaurasiya24)

## Legal

**© 2026 Himanshu Chaurasiya. All rights reserved.**

This is proprietary software. Unauthorized copying, distribution, or modification is prohibited.

---

<div align="center">

**Axiom** - Your Secure Digital Vault

Built with Flutter • Encrypted with AES-256-GCM • Version 3.0.0

</div>
