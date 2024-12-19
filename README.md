# Password Security Checker

This Python script checks whether a password has been exposed in a data breach using the [Have I Been Pwned API](https://haveibeenpwned.com/Passwords).

## Features
- Uses the SHA-1 hash of the password to query the API securely.
- Protects password privacy by only sending the first 5 characters of the hash.
- Returns the number of times the password has been found in breaches.

## How It Works
1. The script hashes the password using SHA-1.
2. It sends the first 5 characters of the hash to the API.
3. The API returns a list of hash suffixes and their breach counts.
4. The script checks if the full hash exists in the returned data and reports the count.

## Requirements
- Python 3.x
- `requests` library (for API usage)
- `hashlib` library (to turn your password into a secure hash algorithm)
- `sys` library (to input your password using your terminal)
  
To install the required library, use:
```bash
pip install requests

