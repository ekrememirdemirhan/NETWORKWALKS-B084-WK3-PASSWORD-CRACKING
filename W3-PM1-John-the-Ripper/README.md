# W3-PM1 — Password Cracking with John the Ripper

## Project Information

- **Internship:** Networkwalks Cybersecurity Internship
- **Batch:** B084
- **Week:** 3
- **Module:** W3-PM1
- **Project:** Password Cracking with John the Ripper
- **Date:** November 21, 2026
- **Operating Systems:** Windows 11 and Kali Linux

## 1. Objective

The objective of this project was to recover the password of a training PDF file using John the Ripper and its graphical interface, Johnny.

The exercise demonstrated how password recovery tools work and why strong passwords are important for protecting sensitive files.

## 2. Tools Used

- John the Ripper 1.9.0-jumbo-1
- Johnny GUI 2.2
- Kali Linux
- Windows 11
- VirtualBox
- pdf2john

## 3. Project Implementation

### Task 1 — John the Ripper Installation

Downloaded and extracted John the Ripper on Windows.

Located `john.exe` inside the extracted `run` directory.

### Task 2 — Johnny GUI Configuration

Installed Johnny and configured it to use the John the Ripper executable.

Johnny successfully detected John the Ripper 1.9.0-jumbo-1.

### Task 3 — PDF Hash Extraction

The password-protected training file, `My Locked PDF1.pdf`, was accessed through a VirtualBox shared folder.

The PDF hash was extracted locally using Kali Linux.

**Command:**

```bash
pdf2john "/media/sf_downloads/My Locked PDF1.pdf" > "/media/sf_downloads/hash1.txt"
```

**Result:**
- PDF file size: approximately 267 KB
- Extracted hash file: `hash1.txt`
- Hash file size: 232 bytes
- Hash format: PDF

### Task 4 — Password Recovery

The extracted hash was imported into Johnny.

A password recovery attack was performed using John the Ripper.

**Result:**
- Hashes loaded: 1
- Passwords recovered: 1
- Recovery status: 100% successful

The recovered password is intentionally excluded from the public documentation.

### Task 5 — PDF Verification

The recovered password was used to unlock the training PDF.

The document opened successfully and displayed the Networkwalks congratulations and flag-capture message.

**Status: Successfully completed.**

## 4. Troubleshooting

### Issue 1 — Incorrect pdf2john Path

Initially, the following command failed:

```bash
python3 /usr/share/john/pdf2john.py
```

The specified Python script was not present in the installed Kali Linux environment.

**Solution:**

Located the available utility using:

```bash
find /usr -iname '*pdf2john*' 2>/dev/null
```

The tool was available as `/usr/bin/pdf2john`.

Using the correct executable resolved the problem.

### Issue 2 — Johnny File Selection

The extracted hash file was initially difficult to locate because of the file dialog and format filters.

**Solution:**

Used Johnny's password-file import option and selected `hash1.txt`.

Johnny successfully recognized the PDF hash.

## 5. Security Considerations

Password recovery tools can demonstrate weaknesses in password protection when passwords are predictable or vulnerable to guessing.

This exercise highlights the importance of:

- Strong and unique passwords
- Appropriate encryption settings
- Secure storage of sensitive documents
- Authorized security testing
- Protecting password hashes and recovered credentials

## 6. Evidence

Screenshots collected during the project include:

1. Johnny installation and configuration
2. PDF hash extraction and troubleshooting
3. Successful hash import
4. Successful password recovery
5. PDF verification and flag capture

Public evidence will exclude password hashes, recovered passwords, and lab flag values.

## 7. Conclusion

W3-PM1 was successfully completed.

This project provided hands-on experience with John the Ripper, Johnny GUI, PDF hash extraction, password recovery, troubleshooting, and verification.

The practical exercise strengthened my understanding of password security and ethical cybersecurity testing.

**Disclaimer:** This project was performed exclusively on a training PDF provided for an authorized educational laboratory. No unauthorized access or exploitation was conducted.
