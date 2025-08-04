

---

# 🔐 VaultGuard – Simple Password Manager

*A minimal, secure password manager built in Python for the INSA Summer Camp.*

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-orange)

Securely store and manage passwords with **AES encryption** and a master password. All data is encrypted **locally**—no cloud dependency.

---

## ✨ Features

* 🔐 **Master Password Protection** – A single password unlocks the vault
* 🛡️ **AES-256 Encryption** – Secure with Fernet (from `cryptography`)
* 📝 **Credential Management** – Add, view, and manage service credentials
* 📁 **Local Storage** – Encrypted data saved in `vault.txt`, created on first run
* 🚫 **Fully Offline** – No internet access required, ensuring maximum privacy

---

## ⚙️ How It Works

1. **First Run**

   * Prompts user to set a master password
   * Generates a secure encryption key (`key.key`)

2. **Vault Access**

   * Enter your master password to unlock encrypted credentials

3. **Credential Management**

   * Add service credentials (e.g., site, username, password)
   * View decrypted credentials temporarily during runtime

4. **Secure Storage**

   * Passwords are encrypted and saved locally in `vault.txt`

---

## 🛠️ Tech Stack

* **Language**: Python 3.8+
* **Libraries**:

  * [`cryptography`](https://pypi.org/project/cryptography/) – AES/Fernet encryption
  * `hashlib` – Password hashing and key derivation
* **Storage**:

  * `vault.txt` – Encrypted vault file
  * `key.key` – Stored encryption key (must be kept safe)

---

## 🚀 Getting Started

### Prerequisites

* Python 3.8 or later
* `pip` for installing dependencies

### Installation & Running

```bash
git clone https://github.com/crumpledflowers/vault-guard-cli.git
cd vault-guard-cli
pip install -r requirements.txt
python main.py
```

If `requirements.txt` is not present, install manually:

```bash
pip install cryptography
```

---

## 🔒 Security Notes

> ⚠️ **Important:**

* Your **master password is unrecoverable** if forgotten — store it safely
* For production or long-term use, consider adding:

  * ✅ Two-Factor Authentication (2FA)
  * 🔁 Brute-force attempt limits or lockout timer
  * 🔍 Audit logging or intrusion alerts

---

## 📁 Project Structure

```
vault-guard-cli/
├── main.py          # Application entry point
├── vault.txt        # Encrypted credentials (auto-generated)
├── key.key          # Encryption key (auto-generated)
└── README.md        # Project documentation
```

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---


