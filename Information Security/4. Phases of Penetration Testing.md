# Phases of Penetration Testing & Hacking Lifecycle

Penetration testing is a structured process used to identify, exploit, and document security vulnerabilities. It is often used to simulate real-world attacks in a legal and ethical manner.

---

## 1. Planning and Scoping (Pre-engagement)

**Objective:** Define the goals, scope, and rules of engagement.

### Key Activities:

- Understand client objectives, security policies, and compliance requirements.
- Define the scope: systems, applications, networks, APIs, physical assets.
- Identify testing boundaries (IP ranges, domains, accounts).
- Establish rules of engagement: timeframe, tools, escalation protocols.
- Obtain written authorization to ensure legality and avoid legal issues.

---

## 2. Reconnaissance (Information Gathering)

**Objective:** Collect intelligence about the target to identify potential attack vectors.

### Passive Reconnaissance (No direct interaction):

- WHOIS lookups, DNS enumeration, social media analysis.
- Scrape metadata from documents/websites (e.g., using FOCA).

### Active Reconnaissance (Direct interaction):

- Port scanning (e.g., Nmap), service enumeration, banner grabbing.
- Network mapping, OS fingerprinting, interrogation tools (Netcat, Shodan).

---

## 3. Vulnerability Analysis

**Objective:** Identify and assess weaknesses that could be exploited.

### Key Activities:

- Perform vulnerability scans (Nessus, OpenVAS, Qualys).
- Identify:
    - Misconfigurations
    - Outdated software
    - Weak credentials
    - Exposed services or APIs
- Prioritize using CVE IDs and CVSS scores.

---

## 4. Exploitation

**Objective:** Exploit identified vulnerabilities to gain unauthorized access or demonstrate impact.

### Key Activities:

- Execute known/custom exploits (SQLi, XSS, buffer overflows).
- Use tools like Metasploit, Burp Suite, SQLMap.
- Attempt privilege escalation (gain root/admin).
- Bypass firewalls or authentication mechanisms.

---

## 5. Post-Exploitation

**Objective:** Evaluate the extent of compromise and business impact.

### Key Activities:

- Establish persistence (backdoors, cron jobs, startup scripts).
- Move laterally within the network (pivoting).
- Extract sensitive data (credentials, tokens, intellectual property).
- Assess impact on data confidentiality, integrity, and availability.

---

## 6. Reporting

**Objective:** Document findings, exploitation steps, and remediation advice.

### Key Activities:

- Create a technical report:
    - Vulnerabilities discovered
    - Exploitation methods used
    - Systems or data accessed
- Include screenshots, logs, payloads, evidence.
- Provide remediation suggestions: patches, config fixes, best practices.
- Share technical + executive summaries.

---

## 7. Remediation Verification (Retesting)

**Objective:** Confirm that vulnerabilities have been fixed properly.

### Key Activities:

- Retest to ensure patches/configs are applied correctly.
- Validate fixes and check no new vulnerabilities were introduced.

---

### Summary Flow:

```bash
Planning → Reconnaissance → Vulnerability Analysis → Exploitation → Post-Exploitation → Reporting → (Optional) Retesting

```

---

## Hacking vs Penetration Testing

| Phase | Malicious Hacking | Ethical Penetration Testing |
| --- | --- | --- |
| Reconnaissance | Info gathering (passive/active) | Reconnaissance |
| Scanning | Identify open ports/services | Vulnerability Analysis |
| Gaining Access | Exploit vulnerabilities | Exploitation |
| Maintaining Access | Install backdoors, pivot | Post-Exploitation |
| Covering Tracks | Delete logs, hide traces | Not performed ethically |

---

## Common Tools by Phase

| Phase | Tools Used |
| --- | --- |
| Reconnaissance | theHarvester, Maltego, Shodan, FOCA |
| Scanning & Analysis | Nmap, Nessus, OpenVAS, Nikto |
| Exploitation | Metasploit, SQLMap, Burp Suite, Custom Scripts |
| Post-Exploitation | Mimikatz, BloodHound, PowerView |
| Reporting | Dradis, Serpico, Markdown, Screenshot tools |

---

## Notable Figures & References

- **Kevin Mitnick** – *Ghost in the Wires* (pioneer of social engineering).
- **Edward Snowden** – NSA whistleblower (security and surveillance ethics).
- **Mr. Robot** – TV series showing realistic hacking and social engineering.
