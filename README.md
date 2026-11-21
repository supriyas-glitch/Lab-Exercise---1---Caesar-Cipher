# Lab-Exercise---1---Caesar-Cipher
## AIM :
To encrypt and decrypt the given message using the Caesar Cipher encryption algorithm.

## PROCEDURE :
1.Start the program.
2.Define a function to implement the Caesar Cipher algorithm.
3.Get the choice from the user (encryption or decryption).
4.Read the message and shift value from the user.
5.For encryption, shift each letter forward by the given number of positions.
6.For decryption, shift each letter backward by the given number of positions.
7.Use modulo 26 to keep the letters within the alphabet.
8.Display the encrypted or decrypted message.
9.Stop the program.

## PROGRAM :
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
## OUTPUT :
<img width="952" height="1016" alt="Screenshot 2026-10-17 140947" src="https://github.com/user-attachments/assets/94043b1f-8eec-4e22-ac87-8a454cb59e1d" />

## RESULT :
The Caesar Cipher encryption and decryption program was executed successfully, and the given message was encrypted and decrypted using the specified shift value.
