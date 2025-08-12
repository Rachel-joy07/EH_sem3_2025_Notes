# Cybersecurity Notes
Date: 1-08-2025
---

## 1. Basic Networking Concepts

### What is a Protocol?  
A **protocol** is a set of rules that computers use to communicate with each other. Just like humans need a language to talk, computers use protocols to understand and send data correctly.

---

### TCP vs UDP  
These are two important protocols used for sending data over the internet.

- **TCP (Transmission Control Protocol):**  
  - Ensures data is sent accurately and in order.  
  - Checks if data arrives and asks to resend if anything is lost.  
  - Used for websites, emails, and file downloads.

- **UDP (User Datagram Protocol):**  
  - Sends data quickly but does not check if it arrives or is in order.  
  - Used for live video, voice calls, or online games where speed is more important than accuracy.

---

### What is a Port?  
- A **port** is like a door on a computer where data comes in or goes out.  
- Each service (like a web server or email) uses a specific port number to listen for data.  
- Example ports:  
  - Port 22 for SSH (secure remote login)  
  - Port 80 for HTTP (websites)  
  - Port 443 for HTTPS (secure websites)

---

### DNS and IP Addresses  
- Computers use **IP addresses** (numbers) to find each other on the internet.  
- Humans use names like `google.com`.  
- **DNS (Domain Name System)** translates these names into IP addresses so computers know where to send data.

---

## 2. Security Basics

### What is SSH?  
- SSH (Secure Shell) is a way to securely connect to another computer over the internet.  
- It encrypts data so no one else can read what you send or receive.

---

### User Privileges  
- Computers have different user levels:  
  - **Root/Admin:** Full access to everything.  
  - **Low Privilege User:** Limited access for safety.  
- Always run services with low privilege users to minimize risks.  
- **Privilege escalation** is when attackers try to get higher access than they should.

---

### Why Use Low Privilege Users?  
- Limits damage if an account is hacked.  
- Prevents attackers from controlling the entire system easily.

---

### User Account Control (UAC)  
- A security feature in Windows that asks for permission before allowing important changes.  
- Hackers try to bypass UAC to gain admin access.

---

## 3. Hosting and File Permissions

### File Permissions and `chmod`  
- Controls what users or programs can do with files (read, write, execute).  
- Important to restrict permissions on servers to prevent malicious actions.

---

### File Monitoring  
- Tools check if files change unexpectedly by comparing their hashes (unique fingerprints).  
- If changes are suspicious, the system can restore the safe version.

---

## 4. Useful Tools and Services

### Shodan  
- Search engine for devices connected to the internet.  
- Used by hackers to find vulnerable machines.

### VirusTotal API  
- Online service to scan files for malware using multiple antivirus engines.  
- Can be integrated into servers to check uploaded files automatically.

### Ncat  
- Tool to send and receive data over networks for testing and communication.

### Bash Scripts  
- Small programs to automate tasks on Linux or Unix systems.

---

## 5. Security Operations

### Security Operations Center (SOC)  
- Team or system that monitors networks for attacks or suspicious activity.

### Data Exfiltration  
- Unauthorized stealing or transfer of data from a system.

---

## 6. Setting up Python Development Environment

 Create isolated Python environments to manage packages and dependencies using:  
  ```bash
  python3 -m venv env_name
```
Activate the environment:
 Linux/macOS:
```bash
source env_name/bin/activate
```
 Windows:
```bash
.\env_name\Scripts\activate
```
 Install packages with:
```bash
pip3 install package_name
```
#Run Python scripts:
```bash
python3 script.py
```
## 7. Villain Framework Overview
A tool to generate payloads for penetration testing.
 Key terms:
rhost: IP address of target (victim).
lhost: IP address of attacker’s machine.
 Process:
Find attacker IP with ifconfig (Linux/macOS) or ipconfig (Windows).
Set lhost to this IP.
Generate payload and send to victim.
Once payload runs, attacker can open shells and control victim remotely.
Persistent remote connections require static IP or dynamic DNS.

## 8. Project Ideas and Concepts
Build AI chat helpers on Linux using Groq API.
Learn about authentication and authorization.
Use API keys to secure services.
Create Python servers for file sharing.
Automate malware scanning with VirusTotal API.
Explore freelance cybersecurity projects.
