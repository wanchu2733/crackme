# Writeup: really easy
**Challenge by:** ezloom  
**Date:** March 2026  
**Platform:** Linux (x86_64)

---

## 1. Challenge Overview
"really easy" is a beginner-level binary exploitation/reverse engineering challenge. The goal is to identify the correct password required to trigger the "Correct!" message.

## 2. Initial Reconnaissance
### File Information
First, I checked the file type to confirm the architecture:
- **Command:** `file crackme.out`
- **Result:** `ELF 64-bit LSB executable, x86-64...`

### Static Analysis (Strings)
Running `strings` revealed several interesting plain-text hints:

---
