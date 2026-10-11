# CartmanView

**A Windows desktop application for encrypted file storage and restoration.**

CartmanView is a desktop application designed to encrypt files into a custom `.cartman` format and restore them when the correct password is provided. It combines authenticated encryption with a custom encoding layer and a graphical interface for managing file operations.

---

## 📌 Project Overview

CartmanView provides a graphical interface for encrypting files, reviewing recorded operations, and restoring encrypted files.

The application is designed around a simple workflow that keeps encryption, file viewing, and decryption operations organized in one place.

### Key Features

- 🔐 **File Encryption** — Encrypts file contents before storing them in a custom container.
- 📦 **Custom File Format** — Uses the `.cartman` format for encoded encrypted data.
- 🔓 **File Decryption** — Restores encrypted files when the correct password is provided.
- 📂 **File Viewer** — Provides an interface for reviewing recorded operations and their details.
- 🖥️ **Desktop Interface** — Offers dedicated sections for encryption, file viewing, decryption, and application information.
- 📦 **Standalone Application** — Designed to run as a Windows desktop executable.

## 🏗️ Architecture

CartmanView follows a structured workflow that separates encrypted data processing from its presentation in the graphical interface.

### Encryption Workflow

```text
Original File
     │
     ▼
Encryption
     │
     ▼
Encrypted Data
     │
     ▼
Custom Encoding
     │
     ▼
.cartman Container
```

### Decryption Workflow

```text
.cartman Container
     │
     ▼
Data Decoding
     │
     ▼
Encrypted Data
     │
     ▼
Authentication & Decryption
     │
     ▼
Restored File
```

The application reverses the encryption workflow during restoration. Successful decryption requires the correct password and valid authenticated data.

## 1. 🔐 Encryption

The Encryption section provides the interface for selecting a file and initiating the encryption process.

The resulting encrypted data is stored in the custom `.cartman` format.

### 📸 Screenshot 01 — Encryption Interface

![CartmanView Encryption Interface](images/screenshot-01-encryption.png)

## 2. 📂 File View

The File View section provides access to recorded operations and their details.

Users can review the available history and refresh the displayed information through the application interface.

### 📸 Screenshot 02 — File View

![CartmanView File View](images/screenshot-02-file-view.png)

## 3. 🔓 Decryption

The Decryption section provides the interface for selecting a `.cartman` file and restoring its contents.

The application verifies the encrypted data during the decryption process before restoring the original file.

### 📸 Screenshot 03 — Decryption Interface

![CartmanView Decryption Interface](images/screenshot-03-decryption.png)

## 4. 🖥️ Application Interface

CartmanView brings its primary operations together in a single desktop interface, with dedicated sections for encryption, file viewing, and decryption.

The About section provides additional information about the application.

### 📸 Screenshot 04 — About Section

![CartmanView About Section](images/screenshot-04-about.png)

## 5. 📦 Download

The Windows executable can be made available through the repository's [Releases](../../releases) section.

The public repository showcases the application and its interface. **The application source code is not included in this repository.**

## 6. 🚧 Project Status

CartmanView is an independent personal project focused on encrypted file handling and a dedicated desktop viewing experience.

The application may continue to evolve as new features and improvements are introduced.

## ⚠️ Disclaimer

CartmanView is a personal project and should not be considered independently audited security software. Keep separate backups of important files and protect your passwords. Do not rely on the application as the sole copy of important data.

---

**CartmanView — Encrypted files. A dedicated viewer.**
