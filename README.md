
# Password Cracking with Networkwalks Tools and John the Ripper

## Overview
This project documents a hands-on exercise in cracking password-protected PDF files, completed as part of my cybersecurity internship training with **Networkwalks**, in a **controlled, authorized lab environment**. The goal was to understand the end-to-end workflow of password recovery: extracting a crackable hash from a locked file, running dictionary/brute-force attacks against it, and verifying the recovered password — using two different toolsets across multiple target files.

> ⚠️ **Disclaimer**: All activity in this repository was performed on test files provided within an authorized training/lab environment. No real-world systems, third-party data, or unauthorized files were accessed. This repository is for educational and portfolio purposes only.

## Objective
- Extract a hash from a password-protected PDF
- Attempt to recover the original password using dictionary and brute-force methods
- Verify successful recovery by unlocking the file

## Tools Used

| Tool | Purpose |
|---|---|
| Online HashCrack — PDF Hash Extractor | Web tool used to extract a pdf2john/hashcat-compatible hash from a locked PDF |
| John the Ripper | CLI password-cracking tool used to run dictionary/brute-force attacks against extracted hashes |
| Johnny | GUI front-end for John the Ripper, used to manage attacks and view cracked results |
| Networkwalks Hash Calculator | Browser-based tool to extract a crackable hash from a locked PDF |
| Networkwalks Password Cracker | Web-based cracking tool used to test candidate passwords against the extracted hash |

## Methodology

### PDF1 — Online HashCrack + John the Ripper / Johnny
1. Extracted the hash from the locked PDF using the Online HashCrack PDF Hash Extractor.
2. Saved the extracted hash into a `.txt` file.
3. Loaded the hash file into John the Ripper via the Johnny GUI and ran an attack.
4. John the Ripper successfully cracked the password.
5. Used the recovered password to unlock PDF1 — verified successfully.

### PDF2 — Networkwalks Hash Calculator + Networkwalks Password Cracker
1. Extracted the hash from the locked PDF using the Networkwalks Hash Calculator.
2. Ran the extracted hash through the Networkwalks Password Cracker.
3. The tool returned a match, cracking the password successfully.
4. Used the recovered password to unlock PDF2 — verified successfully.

## Results
Both toolsets (John the Ripper/Johnny and the Networkwalks hash tools) reliably recovered weak/dictionary-based PDF passwords across the target files. Screenshots of each step are included in `/screenshots`.

## Repository Structure
.
├── README.md

└── screenshots/

├── 01-pdf1-hash-extraction-onlinehashcrack.png

├── 02-pdf1-johnny-cracked-result.png

├── 03-pdf1-unlocked-verification.png

├── 04-pdf2-hash-extraction-networkwalks-calculator.png

├── 05-pdf2-networkwalks-password-cracker-result.png

└── 06-pdf2-unlocked-verification.png

## Key Takeaways
- Understanding of how PDF password protection is stored and how it can be converted into a crackable hash format
- Practical experience with John the Ripper and its GUI counterpart, Johnny
- Comparison between a CLI-based cracking workflow and web-based Networkwalks tools
- Reinforced the importance of strong, non-dictionary passwords for sensitive documents

## Author
**Okoye Amara Iliona**
[LinkedIn](https://www.linkedin.com/in/okoye-amara-bb38033a5)

---
*This project was completed as part of a cybersecurity internship training program with Networkwalks, in a sandboxed environment designed for learning password security concepts.*
