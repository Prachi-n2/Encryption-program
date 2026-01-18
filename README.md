# Simple Substitution Encryption

Small Python script that performs a randomized substitution cipher for learning purposes.

## File
- Main script: `encryption%20program.py`  
  Recommended: rename to `encryption_program.py` (no spaces/percent-encoding).

## Requirements
- Python 3.8+ (standard library only)

## Install (Windows / PowerShell)
```powershell
python -m venv .venv
.\.venv\Scripts\Activate
pip install --upgrade pip
Run
From the project folder (PowerShell):
.\.venv\Scripts\Activate
python `encryption%20program.py`
Or, after renaming:
python `encryption_program.py`
Usage
Enter a plaintext message when prompted to encrypt.
The script prints the encrypted message, then prompts for a ciphertext to decrypt (in the same run).
The script uses an in-memory randomized key, so encryption and decryption must occur within the same execution unless the key is saved.
Known issues & quick fixes
Filename: rename encryption%20program.py to encryption_program.py to avoid issues with shells and tools.
Characters outside the allowed set will raise an error. Fix: validate input or catch ValueError and inform the user.
Typo: change any UI text from "Dencrypt" to "Decrypt".
Key persistence: the script currently generates a new random key each run. To decrypt later, save the key mapping (for example, as JSON) and load it for decryption instead of generating a new key.
Unicode: non-ASCII characters (e.g., emojis) are not in the charset and will fail. Extend the charset or normalize inputs if required.
Not cryptographically secure: this is a learning demo. Do not use for real secret data. For secure encryption use a vetted library such as cryptography.
Troubleshooting
ValueError / crashes: check for unsupported characters in input.
Wrong decryption: ensure the same key is used for both encrypt/decrypt (same program run or saved key).
No output: ensure Python 3.8+ is used and the script is executed with the expected interpreter.
Contributing
Small, focused changes are preferred. Test on Windows (PowerShell) and keep filenames safe (no spaces).
