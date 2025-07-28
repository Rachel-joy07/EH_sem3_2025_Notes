

## 📡 Network Basics

### What is a Network?
- Communication between devices (computers, servers, routers, etc.).
- Allows sharing of resources and data.

### What is a Subnet?
- A **subnetwork** or **subnet** is a logically visible subdivision of an IP network.
- Think of it as a "network within a network".
- Structure: `Network → Router → Hosts`

---

## 🔄 IP Addressing

### What is an IP Address?
- Unique identifier assigned to each device on a network.
- Format: IPv4 (`192.168.0.1`) or IPv6 (`2001:0db8:85a3::8a2e:0370:7334`)

### Static vs Dynamic IP Address

| Static IP              | Dynamic IP             |
|------------------------|------------------------|
| Manually assigned      | Automatically assigned (DHCP) |
| Does not change        | May change periodically |
| Used for servers       | Used for client devices |

### IPv4 vs IPv6

| IPv4                | IPv6                                 |
|---------------------|---------------------------------------|
| 32-bit address      | 128-bit address                       |
| Example: `192.168.0.1` | Example: `2001:0db8::1`             |
| ~4.3 billion addresses | Virtually unlimited addresses     |
| Widely used         | Designed to replace IPv4             |

---

## 📦 Protocols

### TCP vs UDP

| Feature                 | TCP                               | UDP                            |
|-------------------------|------------------------------------|--------------------------------|
| Type                    | Connection-oriented                | Connectionless                 |
| Reliability             | High (guarantees delivery)         | Low (no delivery guarantee)    |
| Speed                   | Slower                            | Faster                         |
| Use Cases               | HTTP, FTP, SSH                    | DNS, VoIP, Streaming           |

---

## 🌐 Virtual Networking in VMs

### NAT Adapter
- Shares host’s IP address to access external networks.
- Suitable for internet access but limits inbound connections.

### Host-Only Network
- Only allows communication between host and VM.
- No internet access.

### Bridged Network
- VM acts like a separate device on the network.
- Gets IP from the same network as the host.

---

## 🛠️ Tools & Concepts

### MAC Address
- A unique hardware ID assigned to a network interface.

### Broadcasting
- Sending data to all devices in a subnet (e.g., ARP requests).

---

## 🔍 Nmap – Network Scanning

### Common Use Cases
- Network scanning
- Troubleshooting
- Vulnerability assessment
- Red Team vs Blue Team exercises

### Sample Nmap Command
```bash
nmap -Bn -A -sV -O -oN output.txt --script -vv -p- -sT <target>
```
### 🔍 Flags Explained

| Flag       | Description                      |
|------------|----------------------------------|
| `-A`       | Aggressive scan (OS + version)   |
| `-sV`      | Detect service versions          |
| `-O`       | OS detection                     |
| `-oN`      | Output to normal file            |
| `--script` | Run NSE scripts                  |
| `-vv`      | Increase verbosity               |
| `-p-`      | Scan all ports (1–65535)         |
| `-sT`      | TCP connect scan                 |

---

## 🔐 Penetration Testing Concepts

### Port Forwarding
- Redirects traffic from one IP/port to another.
- Useful in internal exploitation and pivoting.

### Payload
- Carrier for malicious code (e.g., reverse shell).
- Injected with attacker’s IP for reverse communication.

### Reverse Shell Concept
- Target connects back to attacker.
- Enables remote control over compromised system.

```text
Adversary → Email Client → Victim → Payload triggers → Reverse shell to Attacker
```
### 🔐 UAC (User Access Control)
- Windows feature for privilege escalation control.

---

## 🕵️ Reconnaissance & Info Gathering

### Reconnaissance
- Military concept adapted to cybersecurity.
- First stage of an attack: information gathering.

#### Types:
- **Passive Recon**: No interaction (e.g., social media, WHOIS)
- **Active Recon**: Direct interaction (e.g., pings, scans)

### Tools & Resources
- **Wayback Machine**: View historical versions of websites.
- **.env Files**: May contain sensitive data (e.g., API keys).
- **Cursor**: Platform to build SaaS tools and scanning apps quickly.

---

## 📅 Attack Timeline
- Step-by-step view of how attackers compromise systems.
- Useful for Red/Blue Team exercises and threat modeling.

---

## 🧠 Extra Concepts
- **Data Mining**: Extracting patterns from large data.
- **Red Team**: Offensive security testing.
- **Blue Team**: Defensive strategy and monitoring.
- **Scenario-Based Security**: Real-world simulation of attacks.

---

## 🔗 Internal IP Ranges

| Range                      | Description              |
|----------------------------|--------------------------|
| `192.168.x.x`              | Private (home/office)    |
| `10.x.x.x`                 | Private (large networks) |
| `172.16.x.x – 172.31.x.x`  | Private (medium networks) |

