# -SCT__CS__1-
This Python program implements the Caesar Cipher, a classic substitution encryption technique where each letter in a message is shifted a fixed number of positions along the alphabet. The program allows users to both encrypt and decrypt text by specifying a custom shift value.
Caesar Cipher Program

A simple Python program that encrypts and decrypts text using the Caesar Cipher algorithm — a classic substitution cipher where each letter is shifted a fixed number of positions along the alphabet.

Features
Encrypt or decrypt any message
Supports positive and negative shift values
Preserves letter case (uppercase/lowercase)
Leaves spaces, numbers, and punctuation unchanged
Simple command-line menu interface
Input validation for the shift value
How It Works

The Caesar Cipher shifts each letter in the alphabet by a fixed number of positions.
For example, with a shift of 3:

A → D
B → E
Z → C (wraps around)

Decryption simply reverses the shift.

Requirements
Python 3.x
How to Run
Clone or download this repository.
Open a terminal in the project folder.
Run the script:
   python3 caesar_cipher.py
Follow the prompts:
Choose 1 to encrypt or 2 to decrypt
Enter your message
Enter a shift value (e.g. 3)
Example
=== Caesar Cipher ===
1. Encrypt
2. Decrypt
Choose an option (1 or 2): 1
Enter your message: Hello, World!
Enter shift value (integer, e.g. 3): 3

Encrypted message: Khoor, Zruog!

Decrypting Khoor, Zruog! with a shift of 3 returns Hello, World!.

License

Free to use and modify for learning purposes.
  
   
