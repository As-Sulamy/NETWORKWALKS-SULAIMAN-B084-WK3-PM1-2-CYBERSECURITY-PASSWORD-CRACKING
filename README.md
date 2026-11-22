# NETWORKWALKS-SULAIMAN-B084-WK3-PM1-2-CYBERSECURITY-PASSWORD-CRACKING
WEEK 3 OF CYBERSECURITY INTERNSHIP
# 🔓 Password Cracking: John the Ripper & Dictionary Attacks (Week 3)

**Cracking password-protected PDF files using John the Ripper and Networkwalks' dictionary attack tool.**

![Skill](https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square)
![Phase](https://img.shields.io/badge/Phase-Password%20Cracking-C00000?style=flat-square)
![Kali](https://img.shields.io/badge/Kali%20Linux-2026.3-E87500?style=flat-square&logo=kalilinux&logoColor=white)
![JTR](https://img.shields.io/badge/John%20the%20Ripper-Used-238F89?style=flat-square)

---

## 📌 Project Overview

This repository documents my Week 3 work for the Cybersecurity Analyst internship at **[Program / Batch name]**. The task covered **password cracking**, using two different approaches on password-protected PDF challenge files provided by Networkwalks:

1. **John the Ripper (JTR)** — a classic offline password-cracking tool run from Kali Linux.
2. **Networkwalks' Dictionary Attack tool** — a browser-based cracker that matches a PDF's extracted hash against a wordlist.

Both challenges ended in a captured flag, confirming the password was recovered successfully.

---

## 🧰 Modules Completed

| Module | Description | Tool |
|---|---|---|
| W3-PM1 | Password cracking with John the Ripper | `john`, Kali Linux |
| W3-PM2 | Password cracking with Networkwalks' dictionary attack tool | Networkwalks Hash Calculator + Password Cracker (web tool) |

---

## 🔑 Methodology

### W3-PM1: John the Ripper
1. Extracted the password hash from the locked PDF using `pdf2john.pl`, which converts a PDF's encryption data into a crackable `$pdf$` hash format.
2. Saved the hash to a file.
3. Ran John the Ripper against the hash using its default wordlist (or a custom wordlist, if used).
4. Recovered the password with `john --show <hashfile>`.
5. Opened the PDF with the cracked password to reveal the flag.

**Flag captured:** `nw{networkwalks_persistence_jtr_270321}`

### W3-PM2: Networkwalks Dictionary Attack Tool
1. Extracted the `$pdf$` hash of the target PDF using Networkwalks' **Hash Calculator** tool.
2. Pasted the hash into the **Password Cracker through Dictionary Attacks** tool (networkwalks.com/password-cracker).
3. Ran the attack using the built-in 100-password list.
4. The tool matched the hash and returned the password.
5. Opened the PDF with the password to reveal the flag.

**Flag captured:** `nw{cybersecurity_flag_captured_2608}`

---

## 💡 Why This Matters

Both exercises demonstrate the same underlying idea: **a password hash can be cracked by hashing every word in a wordlist and comparing it to the target hash.** This is why:

- Weak or common passwords are recovered in seconds against a small wordlist.
- Longer, unique passphrases are dramatically harder to crack this way.
- PDF password protection (like many document-level encryption schemes) is only as strong as the password chosen, since the encryption algorithm itself isn't being broken, only the password is being guessed.

---

## 🐞 Challenges

- [Add anything you ran into, e.g. matching the exact hash format JTR expects, or wordlist not containing the password on the first try.]

---

## 💡 What I Learned

1. How to extract a crackable hash from a password-protected PDF.
2. How John the Ripper matches wordlist candidates against a target hash.
3. That the same dictionary-attack concept can be implemented as a simple web tool, not just a command-line one.
4. Why password strength and wordlist size directly determine how long a password survives.
5. That captured flags are a good way to confirm a recovered password is correct.

---

## 🔐 Ethical Use

These exercises were performed only on password-protected files provided for this internship exercise. Password cracking must only be performed on files, accounts or systems you own or have explicit written permission to test.

---

## 🔗 Tools & Resources

- **John the Ripper:** https://www.openwall.com/john/
- **Networkwalks Hash Calculator & Password Cracker:** https://networkwalks.com/password-cracker/

---

## 👤 Author

**Sulaiman Ismail Bello**
Cybersecurity Analyst Intern, [Program / Batch name]

LinkedIn: [your LinkedIn profile URL]

---

**Program:** [Program name] | **Week:** 03 | **Project:** Password Cracking | **Repository:** GitHub