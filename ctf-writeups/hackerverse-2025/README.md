# 🏴 HackerVerse CTF — Writeup

**Category:** Cryptography / Warm Up  
**Solved Challenges:** 2  
**Platform:** HackerVerse CTF  

---

## 🌐 Warm Up — Challenge 1

### Description
The challenge requires us to decrypt the provided message.

### Approach
The provided message appears to be encoded text. Upon closer inspection, it uses the Caesar Cipher — one of the most classic ciphers that shifts each letter by a certain fixed position.

### Tools
* Caesar Cipher decoder (manual / online)

### Walkthrough
1. Receive the encrypted message.
2. Attempt to decrypt it using the Caesar Cipher.
3. Shift all letters until the plaintext makes sense.

### Flag / Output
`seven three four zero five eight two one six four`



