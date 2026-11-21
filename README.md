# Networkwalks Cybersecurity Internship — Week 3

**Batch:** B084  
**Date:** November 21, 2026  
**Focus:** Password Security, Hash Extraction & Dictionary Attacks

## Project Overview

During Week 3 of my Networkwalks Cybersecurity Internship, I completed two hands-on password security modules using John the Ripper and Networkwalks online tools.

Both exercises were conducted on an authorized training PDF.

## Completed Modules

### W3-PM1 — Password Cracking with John the Ripper

- Installed John the Ripper and configured Johnny GUI.
- Extracted an encrypted PDF hash using `pdf2john`.
- Troubleshot an incorrect utility path.
- Successfully recovered the training PDF password.
- Verified access to the PDF and captured the lab flag.

[View W3-PM1 Project & Evidence](W3-PM1-John-the-Ripper/)

### W3-PM2 — Password Cracking with Networkwalks Tools

- Extracted the PDF hash using Networkwalks Hash Calculator.
- Tested a built-in dictionary containing 100 passwords.
- Documented the unsuccessful first attempt.
- Created a custom seven-word dictionary containing the password recovered in PM1.
- Successfully verified the password on the fifth attempt.
- Opened the protected PDF and verified the flag.

[View W3-PM2 Project & Evidence](W3-PM2-Networkwalks-Tools/)

## Skills Practiced

- Password security fundamentals
- John the Ripper and Johnny GUI
- PDF hash extraction
- Dictionary-based password recovery
- Custom wordlist creation
- Linux troubleshooting
- Technical documentation
- Security-conscious evidence handling

## Key Learning

The exercises demonstrated that dictionary-based password recovery depends heavily on the candidate passwords included in the wordlist.

The successful custom dictionary test in PM2 was a verification using a previously known training password, not an independent password discovery.

## Security & Ethics

All exercises were conducted using a training PDF provided for educational purposes.

Public evidence excludes extracted password hashes, recovered passwords, and lab flag values.

No unauthorized systems, accounts, or documents were targeted.
