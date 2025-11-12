# Network Security Threats — Report
**Author:** Surya  
**Date:** 2025-11-12  
**Internship:** Oasis Infobyte — Security Analyst

---

## 1. Introduction
Modern networks face numerous threats targeting confidentiality, integrity, and availability. Understanding how each threat works helps analysts detect and mitigate attacks before they cause harm.

---

## 2. Common Threats, Impact & Mitigation

### 2.1 Denial of Service (DoS) / Distributed DoS (DDoS)
- **How it works:** Floods the target with traffic to exhaust bandwidth or resources.  
- **Impact:** Service downtime, financial loss, damaged reputation.  
- **Mitigation:** Rate-limiting, CDNs or WAFs, redundant servers, filtering spoofed traffic.

### 2.2 Man-in-the-Middle (MITM)
- **How it works:** Intercepts communication between two parties to eavesdrop or alter data.  
- **Impact:** Credential theft, data manipulation.  
- **Mitigation:** Enforce HTTPS /TLS, use VPNs, certificate pinning, avoid open Wi-Fi.

### 2.3 ARP Poisoning / Spoofing
- **How it works:** Sends forged ARP packets to link attacker’s MAC address to a victim IP.  
- **Impact:** Traffic redirection and sniffing.  
- **Mitigation:** Dynamic ARP inspection, static ARP entries for critical systems, VLAN segmentation.

### 2.4 IP Spoofing
- **How it works:** Fakes the source IP address in packets to bypass trust relationships.  
- **Impact:** Helps DoS amplification or access control evasion.  
- **Mitigation:** Ingress/egress filtering (BCP 38), firewall validation of source IP.

### 2.5 Port Scanning / Reconnaissance
- **How it works:** Probes hosts for open ports and services to map vulnerabilities.  
- **Impact:** Reveals attack surface for exploitation.  
- **Mitigation:** Restrict unnecessary ports, IDS/IPS monitoring, honeypots, log analysis.

### 2.6 Session Hijacking
- **How it works:** Steals or predicts a session token to impersonate a legitimate user.  
- **Impact:** Unauthorized access, data breach.  
- **Mitigation:** Use secure cookies (HttpOnly, Secure), short token lifetime, MFA, token rotation.

---

## 3. Real-World Examples
- **GitHub DDoS 2018:** One of the largest attacks mitigated via Cloudflare scrubbing.  
- **Public Wi-Fi MITM:** Attackers steal credentials from unencrypted sessions.  

---

## 4. Best Practices Summary
1. Keep software and firmware patched.  
2. Limit exposed services and ports.  
3. Encrypt all network communications.  
4. Monitor traffic and logs continuously.  
5. Apply least privilege and strong authentication.  

---

## 5. Appendix — Scan Used in Internship
- Target: **127.0.0.1 (localhost)**  
- Command: `nmap -sV 127.0.0.1`  
- Output saved in `../Task1-Nmap/nmap_scan_results.txt`  
- Key findings: (check your file and add open ports here if any)

---

## 6. References
- OWASP Network Security Testing Guide  
- NIST SP 800-115 Technical Guide to Information Security Testing  
- Cloudflare DDoS Case Studies
