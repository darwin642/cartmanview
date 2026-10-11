# CartmanView

**A standalone Windows application for encrypted file handling.**

CartmanView is a desktop application designed to encrypt files into a custom `.cartman` format and restore them through a dedicated graphical interface. The application organizes the process into clear stages, from file selection and encryption to container inspection and decryption.

## 📦 1. Standalone Executable

CartmanView is packaged as a standalone Windows executable, allowing the application to be distributed as a single `.exe` file.

![CartmanView Standalone Executable](images/screenshot-00-standalone.png)

## 🔐 2. Encryption Overview

The Encryption screen is the application's default view. It provides the starting point for selecting a file and initiating the encryption workflow.

![CartmanView Encryption Overview](images/screenshot-01-encryption.png)

### ⚠️ 2.1 File Selection & Warning

After a file is selected, CartmanView displays a warning before proceeding with the operation. This step gives the user an opportunity to review the action before continuing.

![CartmanView File Selection Warning](images/screenshot-02-warning.png)

## 📂 3. File View

The File View section presents the application's file-processing workflow. It is divided into three key stages: the processing pipeline, AES-GCM, and CartmanCodec.

### 3.1 Processing Pipeline

The pipeline illustrates how file data moves through the application's encryption and encoding stages.

```text
Original File
     │
     ▼
AES-GCM Encryption
     │
     ▼
CartmanCodec Encoding
     │
     ▼
.cartman Container
```

![CartmanView Processing Pipeline](images/screenshot-03-pipeline.png)

### 3.2 AES-GCM

AES-GCM provides authenticated encryption. It protects the confidentiality of the file contents and allows the application to verify the integrity of the encrypted data during decryption.

![CartmanView AES-GCM Details](images/screenshot-04-aes-gcm.png)

### 3.3 CartmanCodec

CartmanCodec handles the application's custom data-encoding layer. It converts the encrypted payload into the representation used by the `.cartman` container and decodes it during restoration.

Encoding is separate from encryption: the security of the file depends on the encryption process, not on the custom encoding format.

![CartmanView CartmanCodec Details](images/screenshot-05-cartmancodec.png)

## 🔓 4. Decryption

The Decryption screen provides the interface for selecting a `.cartman` file and restoring its contents. During the process, the encoded payload is decoded and the encrypted data is authenticated and decrypted.

Successful restoration requires the correct password and valid encrypted data.

![CartmanView Decryption](images/screenshot-06-decryption.png)

## ℹ️ 5. About

The About section presents the application's identity and information through its dedicated interface.

![CartmanView About](images/screenshot-07-about.png)

## 📥 6. Distribution

The standalone Windows executable can be published through the repository's [Releases](../../releases) section.

This repository serves as a project showcase. The application source code is not publicly included.

## ⚠️ Disclaimer

CartmanView is an independent personal project and has not been presented as independently audited security software. Keep backups of important files and protect your passwords. Do not rely on the application as the sole copy of important data.

---

**CartmanView — Encrypted files. A dedicated viewer.**
