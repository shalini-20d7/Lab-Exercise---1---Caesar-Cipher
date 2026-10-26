# Lab-Exercise---1---Caesar-Cipher
## Aim

To encrypt and decrypt the given message by using Ceaser Cipher encryption algorithm. 

## Procedure 
Step 1: 
Design of Caeser Cipher algorithnm 
Step 2: 
Implementation using C or pyhton code 
Step 3: 
1.  In Ceaser Cipher each letter in the plaintext is replaced by a letter some fixed number 
of positions down the alphabet.
2. For example, with a left shift of 3, D would be replaced by A, E would become B, and so on.
3. The encryption can also be represented using modular arithmetic by first transforming the letters into numbers, according to the scheme, A = 0, B = 1, Z = 25.
4. Encryption of a letter x by a shift n can be described mathematically as,  En(x) = (x + n)mod26
5. 1 Decryption is performed similarly, Dn (x)=(x - n) mod26
## Program
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
else:
    print("Result:", caesar_cipher(message, shift))
    raise SystemExit

print("Result:", caesar_cipher(message, shift))
```
## output
<img width="1917" height="935" alt="image" src="https://github.com/user-attachments/assets/a16f5663-b550-4122-a658-7bc06c06fda6" />


## Result
The program is executed successfully.
