# -SCT__CS__1-
This Python program implements the Caesar Cipher, a classic substitution encryption technique where each letter in a message is shifted a fixed number of positions along the alphabet. The program allows users to both encrypt and decrypt text by specifying a custom shift value.
def caesar_cipher(text, shift, mode="encrypt"):
    """
    Encrypts or decrypts text using the Caesar Cipher algorithm.

    Args:
        text (str): The message to process.
        shift (int): The number of positions to shift each letter.
        mode (str): "encrypt" or "decrypt".

    Returns:
        str: The resulting encrypted or decrypted text.
    """
    if mode == "decrypt":
        shift = -shift

    result = []
    for char in text:
        if char.isupper():
            shifted = (ord(char) - ord('A') + shift) % 26
            result.append(chr(shifted + ord('A')))
        elif char.islower():
            shifted = (ord(char) - ord('a') + shift) % 26
            result.append(chr(shifted + ord('a')))
        else:
            # Non-alphabetic characters (spaces, numbers, punctuation) are unchanged
            result.append(char)

    return "".join(result)


def get_shift_value():
    while True:
        try:
            return int(input("Enter shift value (integer, e.g. 3): "))
        except ValueError:
            print("Please enter a valid integer.")


def main():
    print("=== Caesar Cipher ===")
    print("1. Encrypt")
    print("2. Decrypt")

    while True:
        choice = input("Choose an option (1 or 2): ").strip()
        if choice in ("1", "2"):
            break
        print("Invalid choice. Please enter 1 or 2.")

    message = input("Enter your message: ")
    shift = get_shift_value()

    if choice == "1":
        output = caesar_cipher(message, shift, mode="encrypt")
        print(f"\nEncrypted message: {output}")
    else:
        output = caesar_cipher(message, shift, mode="decrypt")
        print(f"\nDecrypted message: {output}")


if __name__ == "__main__":
    main()
    
