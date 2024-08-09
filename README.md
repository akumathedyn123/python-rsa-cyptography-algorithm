# RSA-Cyptography-Algorithm
## Author: Md. N e H Jack

RSA (Rivest–Shamir–Adleman) is a public-key cryptosystem, one of the oldest widely used for secure data transmission. The initialism "RSA" comes from the surnames of Ron Rivest, Adi Shamir and Leonard Adleman, who publicly described the algorithm in 1977. An equivalent system was developed secretly in 1973 at Government Communications Headquarters (GCHQ), the British signals intelligence agency, by the English mathematician Clifford Cocks. That system was declassified in 1997. (Ref: Wikipedia)


# Let's see how it works

## Here's how RSA works with small prime numbers: 

### Let's say p = 11 and q = 13

### Key Generation

#### Modulus (n): 
We calculate n by multiplying the primes together (n = p * q = 11 * 13 = 143).

#### Euler's Totient Function (phi(n)): 
This function tells us how many positive integers less than n are coprime (share no common factors) with n. In this case, phi(n) = (p - 1) * (q - 1) = (11 - 1) * (13 - 1) = 10 * 12 = 120.

#### Public Exponent (e): 
This is a small number chosen to be coprime with phi(n). A common choice is e = 7.

#### Private Exponent (d): 
This is the trickier part. It's the modular multiplicative inverse of e modulo phi(n), meaning (e * d) mod phi(n) = 1. In this example, d = 103 (calculated through algorithms).


### Encryption:

#### Suppose you want to encrypt the message "5" (converted to a numerical representation for encryption).
#### You raise the message "5" to the power of the public exponent (e) and take the modulo by the modulus (n): Ciphertext = 5^7 mod 143 = 78.


### Decryption:

The receiver with the private key can decrypt the message by raising the ciphertext (78) to the power of the private exponent (d) and taking the modulo by the modulus (n): Decrypted message = 78^103 mod 143 = 5.

Real-world RSA uses much larger prime numbers (thousands of digits), making it incredibly difficult to crack the code by factoring the public key (n) back into its prime components. This is why RSA is a secure cryptosystem for real-world applications.


# Setting Up the Program

1. **Clone the Repository:**

   (Follow your preferred method for cloning the repository)

2. **Python Version:**

   - Ensure you have Python 3.x installed. You can check by running `python3 --version` in your terminal.

3. **Install Libraries:**

   ```bash
   pip install pycryptodome matplotlib
   ``` 

4. Running the Chatting Program

   1. Open two separate terminal windows:

   2. In the first terminal, run:

    ```bash
    python chat.py
    ```

   3. In the second terminal, run:

    ```bash
    python chat.py
    ```

    **The program will automatically generate and share port numbers and keys, allowing you to start chatting immediately.**

5. To run the attack program and the analysis of encryption/decryption times, run the following command in the terminal:

```bash
python analysis.py
```

# What the program does

The program offers two functionalities: secure chatting and analysis. The chatting feature allows you to send and receive encrypted messages, ensuring confidentiality. The analysis feature explores how the number of bits (key size) impacts the difficulty of cracking the code. It examines two methods for breaking encryption: **Prime Factorization** and **Brute Force**. Additionally, the analysis tool measures encryption and decryption times.

# License

**This project is licensed under the MIT License (see LICENSE file for details).**

# Warning

## This script is intended for educational purposes only. It is designed to help you learn about scripting concepts and explore programming possibilities. It is not intended for production use or any situation where unintended consequences could have a negative impact or any legal issues.  The author is not responsible for any damages or hazards caused by its use. And, know about local laws.
