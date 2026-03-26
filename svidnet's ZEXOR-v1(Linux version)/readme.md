# Writeup: ZEXOR-v1 (Linux)
**Challenge by:** svidnet  
**Date:** March 2026  
**Platform:** Linux (x86_64)

---

## 1. Challenge Overview
ZEXOR-v1 is an entry-level Linux crackme. The goal is to identify the correct authentication key. Based on the name "ZEXOR," the challenge likely involves a simple **XOR-based** obfuscation or comparison.

## 2. Initial Reconnaissance
### File Information
First, I checked the file type to confirm the architecture:
- **Command:** `file crackme.out`
- **Result:** `ELF 64-bit LSB executable, x86-64...`

### Static Analysis (Strings)
Running `strings` revealed several interesting plain-text hints:

---