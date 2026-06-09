# 🔐 OWASP Top 10 - Web Application Security Risks

The OWASP Top 10 is a standard awareness document for developers and web application security. It represents a broad consensus about the most critical security risks.

---

## 🧨 A01:2021 – Broken Access Control
- Violations of least privilege
- Bypassing authorization checks
- Forced browsing to admin pages

## 🔍 A02:2021 – Cryptographic Failures
- Insecure storage or transmission of data
- Weak or no encryption
- Using outdated or misconfigured cryptographic algorithms

## 🐞 A03:2021 – Injection
- SQL, NoSQL, OS, and LDAP injection
- Occurs when untrusted data is sent to an interpreter
- Can lead to data theft or full system compromise

## 🚪 A04:2021 – Insecure Design
- Lack of secure design patterns
- Insecure default behavior
- Missing threat modeling

## 🏷️ A05:2021 – Security Misconfiguration
- Default credentials, open S3 buckets, verbose error messages
- Unnecessary services or ports exposed

## 🔑 A06:2021 – Vulnerable and Outdated Components
- Using old libraries or software
- No version control or patching strategy

## 👤 A07:2021 – Identification and Authentication Failures
- Broken authentication or session management
- Credential stuffing, brute-force attacks

## 🎯 A08:2021 – Software and Data Integrity Failures
- Insecure deserialization
- Dependency confusion
- CI/CD pipeline attacks

## 📦 A09:2021 – Security Logging and Monitoring Failures
- No or poor logging
- Inability to detect/respond to attacks
- Missing audit trails

## 🔗 A10:2021 – Server-Side Request Forgery (SSRF)
- Allows attacker to make requests from vulnerable server
- Can reach internal systems or cloud metadata endpoints

---

## ✅ Mitigation Tips

- Implement least privilege and strong access controls
- Sanitize all user inputs
- Keep all components up to date
- Use secure defaults
- Encrypt sensitive data at rest and in transit
- Enable logging and alerting

---

📁 [Back to Portfolio Home](../README.md) | 🔗 [OWASP Official Site](https://owasp.org)
