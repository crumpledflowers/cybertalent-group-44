---

# 🔐 VaultGuard – Simple Password Manager  

*A minimal, secure password manager built in Python for the INSA Summer Camp.*  

![Demo](https://img.shields.io/badge/status-active-brightgreen) 
![Python](https://img.shields.io/badge/python-3.8%2B-blue) 
![License](https://img.shields.io/badge/license-MIT-orange)  

Securely store and manage passwords with **AES encryption** and a master password. All data is encrypted locally—no cloud dependency.  

---

## ✨ Features  
- **🔐 Master Password Protection** – Single password to unlock your vault.  
- **🛡️ AES-256 Encryption** – Uses Fernet (symmetric encryption via `cryptography`).  
- **📝 Credential Management** – Add, view, and manage service credentials.  
- **📁 Local Storage** – Encrypted data stored in `vault.txt` (auto-created on first run).  
- **🚫 No Internet Needed** – Fully offline for maximum privacy.  

---

## ⚙️ How It Works  
1. **First Run**: Generates an encryption key (`key.key`) and prompts for a master password.  
2. **Unlock Vault**: Enter the master password to decrypt and access stored credentials.  
3. **Manage Passwords**:  
   - Add new `(service, username, password)` entries.  
   - View all saved credentials (decrypted temporarily).  
4. **Secure Storage**: All data is encrypted before saving to `vault.txt`.  

---

## 🛠️ Tech Stack  
- **Python 3.8+**  
- **Dependencies**:  
  - [`cryptography`](https://pypi.org/project/cryptography/) (for Fernet encryption).  
  - `hashlib` (for key derivation).  
- **Storage**: Plaintext → Encrypted (`vault.txt` + `key.key`).  

---

## 🚀 Getting Started  

### Prerequisites  
- Python 3.8+  
- `pip` (Python package manager).  

### Installation  
1. **Clone the repository**:  
   ```bash
   git clone https://github.com/crumpledflowers/cybertalent-group-44.git
   cd cybertalent-group-44/password-manager
   ```

2. **Install dependencies**:  
   ```bash
   pip install cryptography
   ```

3. **Run the password manager**:  
   ```bash
   python main.py
   ```

---

## 🔒 Security Notes  
⚠️ **Important**:  
- The master password **cannot be recovered**. If lost, encrypted data is permanently inaccessible.  
- For real-world use, consider:  
  - Adding **2FA** (e.g., TOTP).  
  - Using a **keyring** instead of `key.key` for key storage.  
  - Implementing **brute-force protection** (e.g., delay after failed attempts).  

---

## 📜 License  
MIT License. See [LICENSE](LICENSE) for details.  

---

## 🙋 FAQ  
**Q: Can I use this for production?**  
A: This is a **proof-of-concept**. For critical use, consider audited tools like Bitwarden or KeePass.  

**Q: How do I reset the vault?**  
A: Delete `vault.txt` and `key.key`, then restart the app.  

---
