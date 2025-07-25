# 🔐 Cybersecurity Notes - Christ University (SEM 3)

This repository contains structured notes based on the Cybersecurity lectures from Semester 3 at Christ University. Topics include basic malware analysis, setting up a pentesting environment, using hacking frameworks like Villain, Linux basics, and more.

---

## 🛠️ Mini Project Ideas

- **Firewall Development**  
  Implement a basic rules-based or packet-filtering firewall using Python or iptables.

- **Scanning Tool**  
  Create a tool similar to `nmap` that scans open ports or services on a target system.

---

## 💻 Setting Up Kali Linux

### 1. Install VS Code
```bash
sudo apt update
sudo apt install code
```

## 2. Clone a GitHub Repository (Example: Villain Framework)
```bash
git clone https://github.com/t3l3machus/Villain.git
cd Villain
ls
pip3 install -r requirements.txt --break-system-packages
python3 Villain.py
```
If you get an error related to the Crypto library:
```bash
pip3 install pycryptodome --break-system-packages
```
## 🔍 Malware Analysis
## 🧪 Types of Malware Analysis
Type	Description
Static	Analyzing malware without executing it (strings, signatures, reverse engineering).
Dynamic	Executing malware in a safe environment (sandbox) to observe its behavior.

## 📦 Common Malware File Types
.exe – Windows executable (usually zipped)

.apk – Android package (also a zip)

.pdf – Structured as a zip file with .pdf extension

## 🧱 Sandbox Environment
A sandbox is an isolated, controlled environment to safely run and analyze potentially malicious files without affecting the host system.

## 🖼️ Hacking with GIFs
Attackers may hide malicious payloads in image files such as GIFs, or rename executables with misleading extensions (e.g., image.gif.exe).

## 🐧 Linux Terminal Basics
Important Directories and Symbols
/ – Root directory

. – Current directory

.. – Parent directory

## Common Commands
Command	Description
pwd	Print working directory
ls	List files
cd	Change directory
touch	Create empty file
chmod	Change file permissions
man	View manual for commands
pip3 install	Install Python 3 packages

## File Permission Example
rw-rw-r--
user-group-others

## ⚙️ Bash and Scripting Concepts
Bash terminal is built into Kali Linux.

Scripts can interact with the kernel through the terminal.

Obfuscation is used to hide or disguise code to evade detection or reverse engineering.

## 🚀 CI/CD Concepts
CI (Continuous Integration) – Merging developer changes frequently.

CD (Continuous Deployment) – Automatically testing and deploying code.

## 👿 Villain Framework Overview
A post-exploitation C2 (Command & Control) tool for hacking Windows and Linux systems.

Exploits the fact that most antivirus tools only monitor OS-level activities, not RAM.

Used to create reverse shells and persistent access in compromised systems.

Setup Summary:
```bash
git clone https://github.com/t3l3machus/Villain.git
cd Villain
pip3 install -r requirements.txt --break-system-packages
python3 Villain.py
pip3 install pycryptodome --break-system-packages  # if Crypto error occurs
```
## 🔄 Keeping Kali Linux Updated
Always update and upgrade your Kali Linux system before starting any project:
```bash
sudo apt update
sudo apt upgrade
```
## 📌 Notes Summary
Use man <command> for help with Linux tools.

Malware often hides in .exe, .apk, .pdf, or even .gif files.

Linux permissions are crucial when dealing with scripts and malware.

Tools like Villain exploit memory-level execution where antivirus tools don’t operate.

