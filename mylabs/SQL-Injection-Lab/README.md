# SQL Injection Testing Lab

## Overview

This lab demonstrates the identification, exploitation, and mitigation of SQL Injection vulnerabilities within a controlled lab environment using DVWA (Damn Vulnerable Web Application) hosted on Metasploitable2.

The exercise covered manual SQL injection techniques, automated testing using SQLMap, and an evaluation of common mitigation strategies.

---

## Lab Environment

### Attacker

- Kali Linux

### Target

- Metasploitable2
- DVWA (Damn Vulnerable Web Application)

---

## Tools Used

- DVWA
- Kali Linux
- SQLMap
- Firefox Browser

---

## Objectives

- Identify SQL Injection vulnerabilities
- Perform manual SQL Injection testing
- Automate SQL Injection testing using SQLMap
- Understand the impact of SQL Injection
- Evaluate mitigation techniques

---

## Methodology

### Phase 1: Vulnerability Identification

The DVWA application was accessed through a browser and configured with the security level set to Low.

The SQL Injection module was selected and tested using crafted input values to determine whether unauthorized database information could be retrieved.

Skills Demonstrated:

- Web Application Testing
- Vulnerability Identification
- Input Validation Testing

---

### Phase 2: Manual SQL Injection Testing

Manual payloads were used to manipulate backend SQL queries and observe application behavior.

Activities Performed:

- Authentication bypass testing
- SQL query manipulation
- Database information disclosure testing

Skills Demonstrated:

- SQL Injection Fundamentals
- Payload Testing
- Vulnerability Verification

---

### Phase 3: Automated SQL Injection Testing

SQLMap was used to automate the enumeration of databases, tables, and sensitive information exposed through the SQL Injection vulnerability.

Activities Performed:

- Database enumeration
- Table discovery
- Credential extraction

Skills Demonstrated:

- SQLMap Usage
- Database Enumeration
- Automated Security Testing

---

### Phase 4: Security Validation

The DVWA security level was increased and the SQL Injection tests were repeated to evaluate whether the vulnerability remained exploitable.

The higher security configuration successfully prevented the previously successful attacks.

Skills Demonstrated:

- Security Control Validation
- Mitigation Verification
- Defensive Testing

---

## Security Impact

SQL Injection vulnerabilities may allow attackers to:

- Access unauthorized information
- Retrieve sensitive database records
- Bypass authentication controls
- Compromise application integrity

---

## Mitigation Strategies

The following controls help reduce SQL Injection risks:

- Prepared Statements (Parameterized Queries)
- Input Validation and Sanitization
- Principle of Least Privilege
- Web Application Firewall (WAF)
- Secure Coding Practices

---

## Key Learning Outcomes

- SQL Injection Identification
- Manual Exploitation Techniques
- SQLMap Usage
- Web Application Security Testing
- Security Control Validation
- Secure Coding Awareness

---

## Supporting Documentation

Detailed walkthrough and screenshots are available in:

`SQL-Injection.pdf`
