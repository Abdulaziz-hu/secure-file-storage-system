# Secure File Storage System

## Overview

This project is a secure file storage system built with Python. It keeps your files private and safe from unauthorized access using encryption and hashing.

## Features
* **File Encryption**: Uses AES (Fernet) to lock your files.
* **Secure Keys**: Uses PBKDF2 to turn your password into a strong security key.
* **Integrity Check**: Uses SHA-256 hashing to make sure your files have not been changed.
* **Tamper Detection**: Tells you if someone tried to mess with your data.
* **Wrong Password Protection**: Prevents access if the password is incorrect.

## Technologies Used
* Python
* Cryptography Library
* Hashlib (SHA-256)

## Setup and Installation

### 1. Create a Virtual Environment (.venv)
It is best to run this project in a virtual environment to keep your global Python setup clean.

**Windows (PowerShell or CMD):**
```powershell
python -m venv .venv
```

**Linux / macOS:**
```bash
python3 -m venv .venv
```

### 2. Activate the Environment
You must activate the environment every time you open a new terminal.

**Windows:**
```powershell
.venv\Scripts\activate
```

**Linux / macOS:**
```bash
source .venv/bin/activate
```

### 3. Install Dependencies
Once the environment is active, install the required library:
```bash
pip install cryptography
```
*(If you have a requirements.txt file, use: `pip install -r requirements.txt`)*

### 4. Deactivate
When you are finished working, you can turn off the environment by typing:
```bash
deactivate
```

## How to Run
1.  Make sure your virtual environment is active.
2.  Run the main program:
    ```bash
    python main.py
    ```

## How It Works
1.  You choose a file and a password.
2.  The system makes a secure key from your password.
3.  The file is encrypted and saved in the `storage/` folder.
4.  The system saves a "fingerprint" (hash) of the original file.
5.  To get your file back, the system checks your password and makes sure the file hasn't been tampered with.

## Project Structure
* `encrypt.py`: Handles locking the files.
* `decrypt.py`: Handles unlocking the files.
* `hash_utils.py`: Checks if files have been changed.
* `storage/`: A folder that holds your encrypted data.

## Author
* Asmatullah Baryali
* Abdulaziz Alhuzami
=======
This project is a secure file storage system developed using Python. It ensures confidentiality, integrity, and protection against unauthorized access using encryption and hashing techniques.

## Features
- File Encryption using AES (Fernet)
- Password-Based Key Derivation (PBKDF2)
- File Integrity Verification using SHA-256
- Tamper Detection
- Protection against wrong password access

## Technologies Used
- Python
- Cryptography Library
- Hashlib (SHA-256)

## How It Works
1. User provides a file and password
2. System generates a secure key using PBKDF2
3. File is encrypted and stored securely
4. Hash of the original file is stored
5. During decryption:
   - Password is verified
   - File integrity is checked

## How to Run
1. Install dependencies:
   pip install cryptography

2. Run the program:
   python main.py

## Project Structure
- encrypt.py → handles encryption
- decrypt.py → handles decryption
- hash_utils.py → hashing functions
- storage/ → stores encrypted files and hashes

## Security Concepts Implemented
- Symmetric Encryption (AES)
- Key Derivation (PBKDF2)
- Cryptographic Hashing (SHA-256)
- Integrity Verification

## Author
Asmatullah Baryali
