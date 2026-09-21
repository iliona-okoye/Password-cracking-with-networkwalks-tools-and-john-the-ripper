# PDF Password Cracking Lab — Cybersecurity Capstone

## Overview
This project documents a hands-on exercise in cracking password-protected PDF files, completed as part of a cybersecurity internship/capstone in a **controlled, authorized lab environment**. The goal was to understand the end-to-end workflow of password recovery: extracting a crackable hash from a locked file, running dictionary/brute-force attacks against it, and verifying the recovered password.

> ⚠️ **Disclaimer**: All activity in this repository was performed on test files provided within an authorized training/lab environment. No real-world systems, third-party data, or unauthorized files were accessed. This repository is for educational and portfolio purposes only.

## Objective
- Extract a hash from a password-protected PDF
- Attempt to recover the original password using dictionary and brute-force methods
- Verify successful recovery by unlocking the file

## Tools Used

| Tool | Purpose |
|---|---|
| John the Ripper | CLI password-cracking tool used to run dictionary/brute-force attacks against extracted hashes |
| Johnny | GUI front-end for John the Ripper, used to manage attacks and view cracked results |
| Online HashCrack — PDF Hash Extractor | Web tool used to extract a pdf2john/hashcat-compatible hash from a locked PDF |
| Networkwalks Hash Calculator | Browser-based tool to generate/extract hashes (MD5, SHA family, and PDF hashes) locally |
| Networkwalks Password Cracker | Web-based cracking tool used to test candidate passwords against the extracted hash |

## Methodology

1. **Hash Extraction** — Uploaded the locked PDF to a hash extraction tool to generate a `$pdf$...` formatted hash (pdf2john/hashcat-compatible format).
2. **Attack Setup** — Loaded the extracted hash into John the Ripper via the Johnny GUI, selecting the PDF format for the attack.
3. **Cracking** — Ran a dictionary-based attack against the hash. The Networkwalks Password Cracker tool was also used to test candidate passwords against the same hash for comparison.
4. **Verification** — Successfully cracked passwords were used to unlock the original PDF files, confirming correct recovery.

## Results
Both target PDFs were successfully unlocked, confirming the extracted hashes and cracking methodology were correct. Screenshots of each step (hash extraction, attack progress, and successful crack) are included in `/screenshots`.

## Repository Structure

├── README.md
├── screenshots/  
|.  ├── hash-extraction.png
│   ├── johnny-gui-cracked.png
│   └── password-cracker-result.png
└── notes/
└── methodology-notes.md

## Key Takeaways
- Understanding of how PDF password protection is stored and how it can be converted into a crackable hash format
- Practical experience with John the Ripper and its GUI counterpart, Johnny
- Comparison between offline (John the Ripper) and online cracking tool workflows
- Reinforced the importance of strong, non-dictionary passwords for sensitive docum

## Author
**Okoye Amara Iliona**
[LinkedIn](https://www.linkedin.com/in/okoye-amara-bb38033a5)

---
*This project was completed as part of a cybersecurity training program (Networkwalks) in a sandboxed environment designed for learning password security concepts.*

