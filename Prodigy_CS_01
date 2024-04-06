
def caesar_encrypt(text, shift):
    encrypted_text = ""
    for char in text:
        if char.isalpha():
            shift_amount = (ord(char.lower()) - ord('a') + shift) % 26
            encrypted_char = chr(ord('a') + shift_amount) if char.islower() else chr(ord('A') + shift_amount)
            encrypted_text += encrypted_char
        else:
            encrypted_text += char
    return encrypted_text

def caesar_decrypt(text, shift):
    decrypted_text = ""
    for char in text:
        if char.isalpha():
            shift_amount = (ord(char.lower()) - ord('a') - shift) % 26
            decrypted_char = chr(ord('a') + shift_amount) if char.islower() else chr(ord('A') + shift_amount)
            decrypted_text += decrypted_char
        else:
            decrypted_text += char
    return decrypted_text

def main():
    while True:
        choice = input("Do you want to encrypt or decrypt? (encrypt/decrypt): ").lower()
        if choice not in ['encrypt', 'decrypt']:
            print("Invalid choice. Please enter 'encrypt' or 'decrypt'.")
            continue
        
        message = input("Enter the message: ")
        shift = int(input("Enter the shift value (a number between 0 and 25): "))

        if choice == 'encrypt':
            encrypted_message = caesar_encrypt(message, shift)
            print("Encrypted message:", encrypted_message)
        else:
            decrypted_message = caesar_decrypt(message, shift)
            print("Decrypted message:", decrypted_message)
        
        another = input("Do you want to perform another operation? (yes/no): ").lower()
        if another != 'yes':
            break

if __name__ == "__main__":
    main()
