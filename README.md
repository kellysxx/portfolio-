# portfolio-
my first rest
# 👩‍💻 Kelechi Happiness Uzoma — Aspiring SOC Analyst

Driven to protect people’s digital security and financial wellbeing through technology, analysis, and continuous learning.

-----

## 👋 About Me

- 🎓 Google Cybersecurity Certificate ✅
- 🌱 Currently Learning: Splunk | ELK Stack | TryHackMe | HackTheBox
- 🎯 Goal: Entry-Level SOC Analyst Role
- 💡 Strengths: Log Analysis · Network Traffic Analysis · Incident Response · Problem Solving
- 📍 Open to Remote / Hybrid Opportunities

-----

## 🛡️ Security Skills

|Skill                       |Details                                              |
|----------------------------|-----------------------------------------------------|
|Log Analysis & Correlation  |Reviewing and correlating logs to identify threats   |
|Network Traffic Analysis    |Using tcpdump and Wireshark to investigate packets   |
|Threat Detection            |Identifying attack patterns using MITRE ATT&CK       |
|Incident Response           |Following structured SOC playbooks to contain threats|
|DNS & ICMP Protocol Analysis|Diagnosing DNS failures and ICMP error messages      |
|DoS / SYN Flood Recognition |Identifying denial-of-service attack patterns        |
|Security Risk Assessment    |Evaluating organizational risks and control gaps     |
|Compliance Auditing         |PCI DSS · GDPR · SOC 2                               |

-----

## 🧰 Tools & Frameworks

![tcpdump](https://img.shields.io/badge/tcpdump-informational?style=flat&color=0D1B2A)
![Wireshark](https://img.shields.io/badge/Wireshark-informational?style=flat&color=1E3A5F)
![Splunk](https://img.shields.io/badge/Splunk-informational?style=flat&color=00C2CB)
![Wazuh](https://img.shields.io/badge/Wazuh-informational?style=flat&color=1B6CA8)
![TryHackMe](https://img.shields.io/badge/TryHackMe-informational?style=flat&color=C45C00)
![Linux](https://img.shields.io/badge/Linux_CLI-informational?style=flat&color=1A7A4A)
![NIST CSF](https://img.shields.io/badge/NIST_CSF-informational?style=flat&color=4A4A6A)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE_ATT%26CK-informational?style=flat&color=8B1A1A)

-----

## 📂 Portfolio Projects

-----

### 🔍 Project 1 — DNS & ICMP Network Traffic Analysis

**Tools:** tcpdump · DNS · ICMP · UDP

**Summary:**
Analyzed tcpdump packet logs to investigate a reported website outage. Identified a breakdown in DNS communication caused by an unreachable service on UDP port 53.

**Key Findings:**

- Client system repeatedly sent DNS queries over UDP port 53 — all failed
- ICMP error responses confirmed `UDP port 53 unreachable`
- The `+` flag on query ID `35084` and `A?` symbol confirmed failed DNS query operations
- Root cause: DNS service down (possible DoS attack) or firewall blocking port 53
- Recommended: verify DNS server status and audit firewall rules for port 53

> 📄 [View Full Report](./reports/Cybersecurity_incident_report_network_traffic_analysis.pdf)

-----

### 🔐 Project 2 — Security Incident Report: Brute Force & Website Compromise

**Tools:** HTTP · tcpdump · Protocol Analysis

**Summary:**
Investigated a full website compromise of `yummyrecipesforme.com`. Traced the complete attack chain from initial brute force access to malware delivery and browser redirection.

**Key Findings:**

- Attacker guessed the default admin password using brute force
- Malicious JavaScript embedded into the site prompted visitors to download fake “browser updates”
- Victims were silently redirected to `greatrecipesforme.com` (malware site)
- tcpdump confirmed traffic: first to `203.0.113.22`, then redirected to `192.0.2.17` — both over port 80
- Remediation: enforce Two-Factor Authentication (2FA) on all admin accounts

> 📄 [View Full Report](./reports/Security_incident_report.pdf)

-----

### 💥 Project 3 — DoS / SYN Flood Attack Analysis

**Tools:** TCP Protocol Analysis · Packet Inspection

**Summary:**
Identified and documented a Denial of Service attack targeting a web server. Analyzed how the SYN flood exploits the TCP three-way handshake to exhaust server resources.

**Key Findings:**

- Web server became unresponsive after being flooded with SYN packets
- Attack type: SYN Flood — exhausted server connection slots
- Legitimate users received `connection timeout` errors
- Recommended controls: SYN cookies, rate limiting, firewall rules, load balancing

> 📄 [View Full Report](./reports/Cybersecurity_incidents_report.pdf)

-----

### 📋 Project 4 — Controls & Compliance Audit (Botium Toys)

**Frameworks:** PCI DSS · GDPR · SOC 2

**Summary:**
Performed a full security controls assessment and compliance checklist review for a fictional retail company, evaluating gaps across administrative, technical, and physical controls.

**Key Findings:**

- Missing controls: Least Privilege, Separation of Duties, IDS, Encryption, Password Management
- PCI DSS gaps: no card data encryption; unauthorized access possible
- GDPR gaps: no 72-hour breach notification plan; data not classified or inventoried
- SOC 2 gaps: user access policies absent; PII/SPII confidentiality not ensured
- Priority recommendations: implement MFA, strong password policies, configure firewall filtering

> 📄 [View Checklist](./reports/Controls_and_compliance_checklist.pdf)

-----

### 🔧 Project 5 — Security Risk Assessment & Hardening Recommendations

**Focus:** MFA · Password Policy · Firewall Hardening

**Summary:**
Produced a security risk assessment report recommending three hardening tools to address identified vulnerabilities in an organization’s network and access controls.

**Recommendations:**

- **MFA** — Prevents unauthorized access even when passwords are compromised
- **Password Policies** — Enforce hashing, salting, and eliminate default/shared credentials
- **Firewall Port Filtering** — Block unauthorized traffic with rule-based filtering

> 📄 [View Report](./reports/Security_risk_assessment_report.pdf)

-----

## 🧠 Threat Detection Methodology

```
1. Log Collection      →  Gather logs from endpoints, servers, and network devices
2. Normalization       →  Ingest and organize logs using SIEM (Splunk / Wazuh)
3. Detection           →  Identify anomalies using MITRE ATT&CK patterns
4. Analysis            →  Investigate via IP reputation checks, packet analysis, log correlation
5. Containment         →  Block malicious IP, isolate affected host
6. Documentation       →  Record findings, timeline, and lessons learned
```

-----

## 🚨 Incident Response Playbook

|Step|Phase            |Action                                                          |
|----|-----------------|----------------------------------------------------------------|
|1   |🔔 Detection      |Alert triggered from SIEM — review severity and affected systems|
|2   |🔎 Triage         |Validate true positive — identify severity level and scope      |
|3   |🕵️ Investigation  |Examine logs, IPs, user behavior — map to MITRE ATT&CK          |
|4   |🛑 Containment    |Block malicious IPs — isolate affected systems                  |
|5   |🧹 Eradication    |Remove malware or threat source — patch vulnerabilities         |
|6   |✅ Recovery       |Restore clean systems — monitor for re-infection                |
|7   |📝 Lessons Learned|Document incident — improve detection rules                     |

-----

## 🏛️ NIST Cybersecurity Framework

|Function      |Description                                                                 |
|--------------|----------------------------------------------------------------------------|
|🔵 **Identify**|Audit networks, systems, devices and access privileges to find security gaps|
|🟣 **Protect** |Implement policies, procedures, training and tools to mitigate threats      |
|🔴 **Detect**  |Scan for incidents and improve monitoring via SIEM and IDS tools            |
|🟡 **Respond** |Contain, neutralize and analyze incidents; implement improvements           |
|🟢 **Recover** |Restore affected systems to normal operation and communicate recovery steps |

-----

## 📜 Certifications

|Status       |Certification                          |
|-------------|---------------------------------------|
|✅ Completed  |Google Cybersecurity Certificate       |
|🔄 In Progress|CompTIA Security+                      |
|🎯 Planned    |ISC2 Certified in Cybersecurity (CC)   |
|📚 Practicing |TryHackMe · HackTheBox · Blue Team Labs|

-----

## 🚀 Career Objective

Aspiring SOC Analyst seeking an entry-level position that leverages hands-on skills in **threat detection**, **log analysis**, **network traffic investigation**, and **structured incident response** — to help organizations build stronger defenses against evolving cyber threats.

-----

## 📫 Contact Me

- 💼 LinkedIn: [linkedin.com/in/Uzomahappiness](https://linkedin.com/in/Uzomahappiness)
- 📧 Email: [kellysxx111@gmail.com](kellysxx111@gmail.com)
- 🐙 GitHub: [github.com/kellysxx](https://github.com/kellysxx)

-----

*📄 Download my full portfolio PDF → [Kelechi_Uzoma_Cybersecurity_Portfolio.pdf](./Kelechi_Uzoma_Cybersecurity_Portfolio.pdf)*
