# 🔐 Simple Password Manager 
This is a **minimal password manager** built in Python as part of our secondary project for the **INSA Summer Camp**. It securely stores and retrieves passwords using encryption and a master password.

---

## ✨ Features
- 🔑 Master password authentication
- ➕ Add new credentials (service, username, password)
- 🔐 AES-based encryption with Fernet
- 📁 Encrypted local storage (`vault.txt`)
- 👁️ Decrypt and view saved passwords
- 🧠 Beginner-friendly CLI interface

---

## How It Works

1. On first run, it generates an encryption key (`key.key`).
2. You enter a **master password** to unlock your vault.
3. You can:
   - Add new login credentials
   - View existing ones
4. All data is stored **encrypted**, locally.

---

## Tech Stack
- Python 3.x
- [`cryptography`](https://pypi.org/project/cryptography/) library
- Plain text file storage (`vault.txt`)

---

## Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/crumpledflowers/cybertalent-group-44.git
cd password-manager
