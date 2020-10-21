# Text encryption and decryption
To encrypt texts and also decrypt them using a generated/user supplied key.

# Detailed functions and implementation
## Encryptor:
The encryptor is very simple to implement. All the characters "abcdef...z" are imported and shuffled to form a random string (say "jgfbh...") or a user specified string (which must contain all the letters used in the supplied text to encrypt). Then each of the characters of the supplied to text to encrypt are encrypted using the key. (The code maybe modified to accept capital letters as well, currently it only encrypts small letters and leaves other symbols or characters as it is).
## Decryptor:
Requires the encryption key. Proceeds with the exact inverse of the method applied to encrypt the text.
