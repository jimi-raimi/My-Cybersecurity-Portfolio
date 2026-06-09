# 🏴 SiberSiaga CTF — Writeup

**Category:** Web Exploitation  
**Solved Challenges:** 1  
**Platform:** SiberSiaga CTF  

---

## 🌐 Entry to Meta City

### Description
A website URL is provided. The objective is to gain access and locate the flag.

### Approach
The website features an input page. Upon closer inspection of the challenge description, the word "admin" is given as a hint. This suggests that we need to provide this specific value as input to grant ourselves access.

This technique is related to Authentication Bypass — where the system fails to properly validate user input before granting administrative or authorized access.

### Tools
* Browser (manual testing)
* Burp Suite (optional for request interception)

### Walkthrough
1. Navigate to the provided website URL.
2. Review the challenge details closely — notice the explicit hint involving the word "admin".
3. Enter `admin` into the input/reason field on the form.
4. Click submit → the access is granted and the flag is revealed.

### Flag
SIBER25{w31c0m3_70_7h3_c001357_c17y}
