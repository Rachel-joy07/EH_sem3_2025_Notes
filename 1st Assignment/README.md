# Assignment 20: Check Internet Exposure via Shodan

**Name:** Kuragayala Rachel  
**Register Number:** 2462106  

---

## 🎯 Objective

To assess what information about my internet connection is publicly visible by attackers using Shodan, simulating a real-world personal security audit. This activity helps identify potential vulnerabilities from an external perspective.

---

## 🧪 Methodology

### 1. Finding My Public IP Address
- Visited [https://whatismyipaddress.com](https://whatismyipaddress.com)
- My public IPv4 address was recorded but is masked in this report for privacy.

### 2. Searching My IP on Shodan
- Navigated to [https://www.shodan.io](https://www.shodan.io)
- Entered my public IP address in the search bar  
**Result:** `"No results found"`

---

## 🖼️ Screenshot of Shodan Result  
*(IP address masked for privacy)*  
![Shodan Result](Screenshot.png)

---

## 📊 Findings and Analysis

- **No exposed services** were found by Shodan on my public IP.
- This is a **positive security indicator**, suggesting:
  - My firewall/router is not exposing ports or services to the public.
  - There are no obvious vulnerabilities externally visible to attackers.
- **Possible reasons:**
  - My ISP uses dynamic IPs that change frequently.
  - No active internet-facing services (e.g., HTTP, FTP, SSH) are running.
  - My router or ISP blocks unsolicited incoming traffic by default.

---

## 🔐 Recommendations to Harden System

Although no exposure was detected, the following best practices should be followed:

1. Ensure the **firewall is active** on router and devices.  
2. **Disable UPnP (Universal Plug and Play)** on the router.  
3. **Avoid port forwarding** unless absolutely necessary.  
4. **Keep all firmware/software updated** (router, IoT, computers).  
5. **Use strong passwords** and disable default logins on devices.  
6. Run periodic internal scans (e.g., `nmap 192.168.1.0/24`) to detect local exposure.

---

## ✅ Conclusion

This audit confirms that my home network currently has **no visible attack surface** on the public internet, according to Shodan. While this is reassuring, consistent monitoring, patching, and proper configurations are essential to maintain a secure environment.

---

## 💻 Code/Configuration Submitted

No custom code or scripts were required, as this task was executed using public tools and browsers.  
**Screenshot of results is attached as supporting evidence.**
