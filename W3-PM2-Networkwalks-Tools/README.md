# W3-PM2 — Password Cracking with Networkwalks Tools

## Project Information

- **Internship:** Networkwalks Cybersecurity Internship
- **Batch:** B084
- **Week:** 3
- **Module:** W3-PM2
- **Project:** Password Cracking with Networkwalks Tools
- **Date:** November 21, 2026
- **Operating System:** Windows 11

## 1. Objective

The objective of this project was to demonstrate dictionary-based password recovery using the Networkwalks Hash Calculator and Password Cracker.

The task involved extracting a password hash from an encrypted training PDF, testing password candidates, and verifying the recovered password.

## 2. Tools Used

- Networkwalks Hash Calculator
- Networkwalks Password Cracker
- Google Chrome
- Windows 11
- Notepad (for creating a custom wordlist)

## 3. Project Implementation

### Task 1 — PDF Hash Extraction

Opened the Networkwalks Hash Calculator and selected the PDF section.

Imported the password-protected training file, `My Locked PDF1.pdf`.

**Observed results:**

| Parameter | Result |
|---|---|
| PDF file size | 266.9 KB |
| Encryption revision | R4 |
| PDF version | V4 |
| Key length | 128 bits |
| Extracted hash format | $pdf$ |
| Hash extraction | Successful |

The extracted hash was used for the password recovery exercise.

The complete hash value is excluded from public documentation.

### Task 2 — Built-in Dictionary Attack

Opened the Networkwalks Password Cracker and entered the extracted PDF hash.

Selected the default built-in dictionary containing 100 password candidates.

**Results:**

- Passwords attempted: 100/100
- Dictionary: Built-in List
- Result: Access Denied
- Message: Exhausted wordlist. No match.

The initial attack failed because the correct password was not included in the built-in dictionary.

### Task 3 — Custom Wordlist Creation

After the unsuccessful built-in dictionary attempt, a custom wordlist was created using Windows Notepad.

The wordlist contained seven password candidates, including the password previously recovered during W3-PM1.

**File:** `W3-PM2-Custom-Wordlist.txt`

**Number of candidates:** 7

This second test was performed to demonstrate and verify the use of a custom dictionary.

### Task 4 — Custom Dictionary Attack

Uploaded the custom wordlist to the Networkwalks Password Cracker.

The tool successfully recognized the seven password candidates.

**Results:**

| Parameter | Result |
|---|---|
| Attack type | Dictionary Attack |
| Dictionary | Custom Wordlist |
| Total candidates | 7 |
| Candidates attempted | 5 |
| Successful match | Yes |
| Password recovery | Successful |

The correct password was matched on the fifth attempt.

Since the recovered password was already known from W3-PM1 and included in the custom dictionary, this result demonstrates successful dictionary-based verification rather than an independent discovery of an unknown password.

### Task 5 — PDF Verification

The matching password was used to open the encrypted training PDF.

The document opened successfully and displayed the Networkwalks congratulations and flag-capture message.

**Verification status: Successful.**

## 4. Troubleshooting

### Issue — Built-in Wordlist Failed

The Password Cracker initially returned:

`ACCESS DENIED — Exhausted wordlist. No match.`

**Cause:**

The correct password was not present among the 100 built-in password candidates.

**Solution:**

Created and uploaded a custom seven-word dictionary containing the previously recovered training password.

The subsequent dictionary test successfully matched the password.

**Lesson learned:**

Dictionary attacks depend on the candidate passwords included in the selected wordlist. A failed dictionary attack does not prove that a password cannot be recovered through other methods.

## 5. Security Observations

This exercise demonstrated several important password-security concepts:

1. Dictionary attacks test password candidates against protected data.
2. A wordlist's contents directly affect the chances of a successful match.
3. Predictable or previously known passwords can be vulnerable to dictionary-based recovery.
4. Password recovery results should be interpreted according to the methodology used.
5. Strong, unique passwords and appropriate encryption help protect sensitive documents.

## 6. Evidence

The following evidence was collected during the exercise:

- PDF hash extraction using Networkwalks Hash Calculator
- Unsuccessful built-in dictionary attack
- Custom wordlist creation and selection
- Successful password matching
- PDF verification and flag capture

Publicly shared screenshots will conceal extracted hash values, recovered passwords, and flag codes.

## 7. Conclusion

W3-PM2 was successfully completed using the Networkwalks Hash Calculator and Password Cracker.

The experiment demonstrated the differences between a failed built-in dictionary attempt and a successful custom dictionary verification.

The project strengthened practical skills in password security, hash extraction, dictionary attacks, troubleshooting, and technical documentation.

**Disclaimer:** All activities were performed on a training PDF provided for an educational cybersecurity exercise. No unauthorized systems, accounts, or documents were targeted.
