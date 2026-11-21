# Lab-Exercise---1---Caesar-Cipher
## AIM

To write a Python program to implement the Caesar Cipher technique for encryption and decryption of messages using a given shift value.

## PROCEDURE

1. Import the necessary modules and define a function named `caesar_cipher()`.
2. Initialize an empty string to store the encrypted or decrypted result.
3. Get the user's choice to encrypt or decrypt the message.
4. Read the message and the shift value from the user.
5. If the choice is decryption, convert the shift value into a negative value.
6. Traverse each character in the given message.
7. Use the ASCII values to shift uppercase and lowercase letters by the specified number of positions.
8. Keep spaces, numbers, and special characters unchanged.
9. Return the resulting encrypted or decrypted message.
10. Display the final result.

## PROGRAM
```
def caesar_cipher(text, shift):
    result = ""

    for char in text:
        if char.isupper():
            result += chr((ord(char) - ord('A') + shift) % 26 + ord('A'))
        elif char.islower():
            result += chr((ord(char) - ord('a') + shift) % 26 + ord('a'))
        else:
            result += char  # Keep spaces, numbers, and punctuation unchanged

    return result


choice = input("Encrypt or decrypt? (e/d): ").lower()
message = input("Enter your message: ")
shift = int(input("Enter shift value: ")) % 26

if choice == "d":
    shift = -shift
elif choice != "e":
    print("Invalid choice.")
    raise SystemExit

print("Result:", caesar_cipher(message, shift))
```
## OUTPUT
<img width="1917" height="1016" alt="Screenshot 2026-10-17 143920" src="https://github.com/user-attachments/assets/e4840657-e6e3-4961-a2a9-3155599fdd7f" />

## RESULT
Thus, the Python program for implementing the Caesar Cipher technique was successfully executed, and the given message was encrypted and decrypted based on the specified shift value.
