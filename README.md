
# Substitution and Transposition Ciphers Using Python

## Project Overview

This lab explores the implementation and analysis of substitution and transposition ciphers using Python in a Kali Linux environment.

The objective was to understand how substitution ciphers transform individual characters and how transposition ciphers rearrange the positions of characters within a message.

The exercises included implementing a Shift 6 substitution cipher, modifying the program to use ROT13, and creating a basic transposition cipher that reverses a string.

## Lab Objectives & Tools

**Objectives:**
- Understand the differences between substitution and transposition ciphers.
- Implement a substitution cipher using Python.
- Perform encryption and decryption using a Shift 6 cipher.
- Modify the program to implement ROT13.
- Implement a basic transposition cipher.
- Test encryption and decryption functionality.
- Understand the limitations of classical cryptographic techniques.

**Tools Used:**

| Tool | Purpose |
|---|---|
| Kali Linux | Programming environment |
| Python 3 | Implement and execute cipher programs |
| Nano | Create and edit Python scripts |
| Terminal | Execute and test the program |

## Lab Procedure

### Step 1 — Navigate to Desktop

The terminal was opened and the working directory was changed to the Desktop.

**Command Used:**

```bash
cd ~/Desktop
```

<img width="468" height="69" alt="image" src="https://github.com/user-attachments/assets/ea2ec65c-041d-4353-8239-75b455fd6efc" />


### Step 2 — Create Python File

A new Python file was created using Nano.

**Command Used:**

```bash
nano crypto.py
```
<img width="468" height="37" alt="image" src="https://github.com/user-attachments/assets/dac48b2e-a4f1-4493-9069-073d61a4d673" />

### Step 3 — Add Substitution Cipher Code (Shift 6)

The provided substitution cipher code was copied and pasted into the Nano editor.

<img width="468" height="371" alt="image" src="https://github.com/user-attachments/assets/aa9bd0be-1680-4264-b412-db5a5a79576c" />

### Step 4 — Save the File

The file was saved using the following keyboard sequence:

`Ctrl + X` → `Y` → `Enter`

### Step 5 — Run the Program

The Python program was executed from the terminal.

**Command Used:**

```bash
python3 crypto.py
```

### Step 6 — Test Encryption

The encrypt option was selected and a sentence was entered.

**Example:**

- **Input:** `hello world`
- **Output:** Encrypted text

<img width="468" height="84" alt="image" src="https://github.com/user-attachments/assets/3d6808e1-6049-4e73-a4c9-3f925639e7fe" />


### Step 7 — Test Decryption

The program was executed again and the decrypt option was selected.

**Example:**

- **Input:** Encrypted text
- **Output:** `hello world`

<img width="468" height="83" alt="image" src="https://github.com/user-attachments/assets/6826e6a7-5554-475f-8d8c-b27cefbe44fe" />


### Step 8 — Modify Program to ROT13

The program was reopened in Nano and modified to shift characters by 13 positions.

**Command Used:**

```bash
nano crypto.py
```


### Step 9 — Save ROT13 Changes

The updated file was saved using the following keyboard sequence:

`Ctrl + X` → `Y` → `Enter`

<img width="468" height="415" alt="image" src="https://github.com/user-attachments/assets/7fd53808-80da-42ae-8965-f5005e7fd478" />


### Step 10 — Run ROT13 Program

The updated program was executed again.

**Command Used:**

```bash
python3 crypto.py
```

### Step 11 — Test ROT13 Encryption

The encrypt option was selected.

**Example:**

- **Input:** `hello world`
- **Output:** `uryyb jbeyq`

<img width="468" height="89" alt="image" src="https://github.com/user-attachments/assets/08253f8c-6e4b-476c-8764-456a378f3377" />

### Step 12 — Test ROT13 Decryption

The decrypt option was selected.

**Example:**

- **Input:** `uryyb jbeyq`
- **Output:** `hello world`

<img width="468" height="81" alt="image" src="https://github.com/user-attachments/assets/a59d6af9-c5f6-47da-93fa-fcc2b14b4f70" />


### Step 13 — Modify Program for Transposition Cipher

The program was modified to implement a transposition cipher by reversing the string.

**Command Used:**

```bash
nano crypto.py
```

<img width="468" height="320" alt="image" src="https://github.com/user-attachments/assets/a7c40f16-1514-43a2-a27b-518f5f7ce9ab" />


### Step 14 — Save Transposition Code

The updated file was saved using the following keyboard sequence:

`Ctrl + X` → `Y` → `Enter`

### Step 15 — Run Transposition Program

The program was executed again.

**Command Used:**

```bash
python3 crypto.py
```

### Step 16 — Test Transposition Encryption

The encrypt option was selected.

**Example:**

- **Input:** `hello`
- **Output:** `olleh`

<img width="468" height="83" alt="image" src="https://github.com/user-attachments/assets/f3c6242e-5e7b-4318-89d1-c38c7d251a4a" />

### Step 17 — Test Transposition Decryption

The decrypt option was selected.

**Example:**

- **Input:** `olleh`
- **Output:** `hello`

<img width="468" height="82" alt="image" src="https://github.com/user-attachments/assets/60927b13-5bec-4b1b-b634-33d7d11bdbb7" />

## Results & Analysis

The lab successfully demonstrated the implementation of substitution and transposition ciphers using Python.

The following results were observed:

- **Shift 6 Cipher:** Characters were shifted six positions to produce encrypted text. The original message was recovered through decryption.
- **ROT13 Cipher:** Characters were shifted thirteen positions. The example `hello world` was encrypted into `uryyb jbeyq` and successfully decrypted.
- **Transposition Cipher:** The characters in a string were reversed. The example `hello` became `olleh` and was restored through the reverse operation.

The exercises demonstrated that substitution and transposition ciphers use different approaches to transform plaintext.

## Technical Analysis

### Substitution Cipher

A substitution cipher replaces individual characters with other characters according to a defined transformation.

In this lab, the Shift 6 and ROT13 implementations demonstrated how character positions in the alphabet can be shifted to produce ciphertext.

### ROT13

ROT13 is a substitution cipher that shifts each alphabetical character thirteen positions.

Because the English alphabet contains 26 letters, applying ROT13 twice restores the original message.

### Transposition Cipher

A transposition cipher rearranges the positions of characters without changing the characters themselves.

In this lab, the string was reversed during encryption and reversed again during decryption.

### Security Limitations

These classical cipher techniques are useful for understanding basic cryptographic concepts, but they are not suitable for protecting sensitive information.

Their transformations are simple and can be reversed or analyzed without modern cryptographic security mechanisms.

## Security Recommendations

- **Use Modern Encryption:** Use established encryption standards such as AES instead of classical substitution or transposition ciphers.
- **Protect Encryption Keys:** Keep cryptographic keys secure and restrict unauthorized access.
- **Use Established Cryptographic Libraries:** Avoid developing custom encryption algorithms for real-world security applications.
- **Use Secure Protocols:** Implement modern encrypted protocols such as TLS when transmitting sensitive information.
- **Understand Cryptographic Limitations:** Recognize that simple character transformations do not provide meaningful protection against modern attacks.

## Results & Conclusion

This lab provided practical experience implementing basic cryptographic techniques using Python in Kali Linux.

The exercises demonstrated how substitution ciphers modify individual characters while transposition ciphers rearrange character positions. The Shift 6 and ROT13 implementations showed how substitution-based encryption and decryption work, while the reverse-string implementation demonstrated a basic transposition technique.

Overall, this project reinforced foundational cryptographic concepts, Python programming skills, and the importance of understanding the limitations of classical encryption methods.
