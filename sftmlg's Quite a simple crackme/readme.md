# Writeup: Quite a simple crackme
**Challenge by:** sftmlg  
**Date:** March 2026  
**Platform:** Linux (x86_64)

---

## 1. Challenge Overview
"Quite a simple crackme" is a beginner-level binary exploitation/reverse engineering challenge. The goal is to identify the correct password required to trigger the "Correct!" message.

## 2. Initial Reconnaissance
### File Information
First, I checked the file type to confirm the architecture:
- **Command:** `file crackme.out`
- **Result:** `ELF 64-bit LSB executable, x86-64...`

### Static Analysis (Strings)
Running `strings` revealed several interesting plain-text hints:
* `Usage: %s password` (Indicates a command-line argument is needed)
* `Access denied!`
* `Correct!`
* `[POTENTIAL_PASSWORD_HERE]` <-- *Check your output for this!*



---

## 3. Technical Analysis
### Control Flow
Using **Ghidra**, I decompiled the `main` function. The program logic follows these steps:

1. **Argument Check:** Verifies if `argc` is equal to 2.
2. **Length Check:** Uses `strlen` to check if the input is exactly **10** characters.
3. **Logic Check:** - Compares index `[4]` to the `@` character.
   - Performs a string comparison (`strcmp`) against a hardcoded value.

### Disassembly Snippet
```assembly
0x004011ab <+43>:  call   0x401030 <strlen@plt>
0x004011b0 <+48>:  cmp    rax, 0xa
0x004011b4 <+52>:  jne    0x4011cf <main+79>