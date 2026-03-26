# 🛡️ Reverse Engineering Lab: Crackmes.one Solutions
A collection of technical writeups, binary analysis, and exploit reports for challenges hosted on [Crackmes.one](https://crackmes.one).

---

## 🔍 What is Crackmes.one?
**Crackmes.one** is the largest community-driven platform for reverse engineering challenges. It serves as a legal "playground" for security researchers to practice:

* **Binary Analysis:** Understanding how compiled code works without the source.
* **Assembly Debugging:** Navigating x86, x64, and ARM instructions.
* **Security Bypassing:** Defeating anti-debugging, anti-VM, and obfuscation techniques.
* **Keygenning:** Reversing mathematical algorithms to generate valid registration keys.



---

## 🛠️ My Analysis Environment
To ensure a safe and efficient workflow, all challenges are analyzed within an isolated sandbox:
* **Key Tools:**
    * **Ghidra:** For static analysis and decompilation.
    * **GDB / x64dbg:** For dynamic analysis and runtime debugging.
    * **Radare2:** For command-line binary forensics.
    * **Python 3:** For writing automated keygens and exploit scripts.

---

## 📂 Repository Structure
Each directory is named after the challenge author and the specific binary name.

| Challenge Name | Author | Difficulty | Writeup Link |
| :--- | :--- | :--- | :--- |
| **Quite a simple crackme** | sftmlg | 1.0 (Beginner) | [Read Writeup](./sftmlg/quite-simple/README.md) |
| **BFCrackMe401** | Boba_Fett | 2.5 (Intermediate) | [Read Writeup](./boba_fett/bf401/README.md) |

---

## ⚠️ Safety Warning
**Please Note:** All files in this repository are for educational purposes only. Many binaries from Crackmes.one use "malware-like" techniques to hinder analysis. **Never run these binaries on your physical host machine.** Always use a Virtual Machine (VM).

---

## 📬 Contact
If you have questions about a specific solution or want to collaborate on a challenge, feel free to open an Issue or reach out!
