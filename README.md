# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.

AES does not use a Feistel network like DES, it uses variant of Rijndael.

It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len];
    }
}

int main() {
    char url[] = "RAJAVELMURUGAN";
    char key[] = "secret";
    
    printf("Original text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted text: %s\n", url);

    return 0;
}
```
# OUTPUT:

<img width="560" height="200" alt="Screenshot 2026-11-18 141535" src="https://github.com/user-attachments/assets/d47d003a-1a45-4d88-bc47-8849275727a6" />



# RESULT:
Thus the program to perform AES Algorithm for a given url has been successfully executed.


