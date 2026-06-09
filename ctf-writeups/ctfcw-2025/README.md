# 🏴 CTFCW — Writeup

**Category:** Web Exploitation, Cryptography  
**Solved Challenges:** 6  
**Platform:** CTFCW  

### Challenge List

| # | Category | Challenge Name | Status |
| :-: | :--- | :--- | :-: |
| 1 | Web Exploitation | Comment Alert | ✅ Solved |
| 2 | Cryptography | Coffee Time with Me | ✅ Solved |
| 3 | Cryptography | Grandfather's Memory | ✅ Solved |
| 4 | Cryptography | Cipher No Hint | ✅ Solved |
| 5 | Cryptography | Morse Code | ✅ Solved |
| 6 | Cryptography | More, More and More Morse Code and Caesar Cipher | ✅ Solved |

---

## 🌐 Web Exploitation — Comment Alert

### Description
The challenge requires us to trigger a popup/alert on the website.

### Approach
This is a basic Cross-Site Scripting (XSS) challenge. The website does not sanitize user input, allowing us to inject JavaScript code directly into the page.

### Tools
* Browser
* Basic JavaScript

### Walkthrough
1. Identify the input field on the website.
2. Insert the following XSS script: `<script>alert(1)</script>`
3. Submit the input — the popup alert appears, and the flag is displayed.

### Flag
`ctfcw{popup_triger}`

### Takeaways
* Unsanitized input leads to XSS attacks.
* In real-world scenarios, XSS can be exploited to steal cookies, session tokens, and other sensitive data.

---

## 🔐 Cryptography — Coffee Time with Me

### Description
The challenge provides a hint: "BRAZIL" and the standard Vigenere cipher.

### Approach
The Vigenere Cipher uses a keyword (key) to encrypt messages. The hint "BRAZIL" is the key.

### Tools
* Cryptii — Vigenere cipher decoder

### Walkthrough
1. Navigate to cryptii.com.
2. Select Vigenere Cipher → Decode mode.
3. Input the encrypted message.
4. Set the key to `BRAZIL`.
5. Decode — the flag is successfully retrieved.

### Flag
`ctfcw{Arabica_Coffee_bean}`

### Takeaways
* The Vigenere Cipher is a polyalphabetic substitution cipher.
* Decryption is straightforward once the keyword is known.
* Hints in CTF challenges always serve a purpose — never ignore them!

---

## 🔐 Cryptography — Grandfather's Memory

### Description
A `.txt` file containing an encrypted message is provided. No direct hints are given.

### Approach
The first step is to identify the type of cipher using a cipher identifier tool. The top two candidates are the ROT Cipher and the Caesar Cipher.

### Tools
* dCode.fr — Cipher Identifier
* dCode — ROT Cipher Decoder

### Walkthrough
1. Download the `.txt` file and open it to view the content.
2. Copy and paste the message into the dCode Cipher Identifier.
3. The analysis suggests both ROT Cipher and Caesar Cipher as potential matches.
4. Testing the ROT Cipher yields a more complete and coherent decoded output compared to the Caesar Cipher.
5. Input the message into the ROT Cipher decoder.
6. Read through the entire output — the flag is hidden near the bottom of the text.

### Flag
`ctfcw{hidden_CaesarCipher}`

### Takeaways
* Always use a cipher identifier first if the encryption type is unknown.
* Flags can be hidden inside long blocks of text — read the entire output carefully.
* ROT13 is a specific subset of the Caesar Cipher (where the shift = 13).

---

## 🔐 Cryptography — Cipher No Hint

### Description
No hints are provided. Only an encoded message is given.

### Approach
Conducted a trial-and-error process using various ciphers on Cryptii. The encryption was eventually identified as the Affine Cipher — a cipher that utilizes a mathematical formula involving slope and intercept.

### Tools
* Cryptii — Multi-cipher platform
* Affine Cipher Decoder

### Walkthrough
1. Go to Cryptii and test different ciphers.
2. The ROT cipher does not produce meaningful output.
3. Try the Affine Cipher — adjust the slope and intercept values one by one.
4. Continue the trial-and-error process until the output begins with the known flag format `ctfcw{`.
5. The flag is successfully uncovered.

### Flag
`ctfcw{basic_knowledge_crypto}`

### Takeaways
* Affine Cipher formula: E(x) = (ax + b) mod 26 — where a is the slope and b is the intercept.
* When no hints are given, combining a cipher identifier with trial and error is the best approach.
* Always look for the expected flag format as a validation point.

---

## 🔐 Cryptography — Morse Code

### Description
An audio file is provided. The challenge hint states: "Analyze morse code audio file and submit the flag in this format: ctfcw{answer}"

### Approach
The audio file contains Morse Code signals. We need to use a tool that can automatically decode Morse Code audio.

### Tools
* morsefm — Morse code audio decoder

### Walkthrough
1. Download the provided audio file.
2. Navigate to morsefm.com.
3. Upload the audio file to the designated area.
4. The tool decodes the audio and displays the text along with the Morse code translation.
5. Extract the resulting text and wrap it in the required format: `ctfcw{<text>}`.

### Flag
`ctfcw{TEMPERTEMPERTEMPER}`

### Takeaways
* Morse Code can be transmitted via audio, light, or text.
* Tools like morsefm simplify the process of automatically decoding audio-based Morse code.
* Pay close attention to the requested flag format — sometimes the answer must be in uppercase.

---

## 🔐 Cryptography — More, More and More Morse Code and Caesar Cipher

### Description
A two-step combination challenge: Morse Code decoding followed by Caesar Cipher decryption.

### Approach
The process starts similarly to the previous Morse Code challenge, but the Morse output remains encrypted using a Caesar Cipher. It requires a two-layer decoding process.

### Tools
* morsefm — Morse Code audio decoder
* Cryptii — Caesar Cipher decoder

### Walkthrough
1. Decode the audio file using morsefm to get the initial text output.
2. The output text still appears to be ciphertext.
3. Input this text into Cryptii, select Caesar Cipher, and set it to Decode.
4. Cycle through different shift values until meaningful plaintext is revealed.
5. Place the plaintext into the `ctfcw{}` format.

### Flag
`ctfcw{PMJCYBERWARRIORARETHEBEST}`

### Takeaways
* CTF challenges often chain multiple layers of encryption together (chained ciphers).
* Decode one layer at a time, then re-analyze the resulting output.
* Stay patient and systematic — do not skip any steps.

