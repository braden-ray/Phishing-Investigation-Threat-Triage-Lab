# Phishing Investigation & Threat Triage Lab

## Overview
This project simulates a real-world SOC phishing investigation involving a suspicious Microsoft 365 credential harvesting email. The investigation focuses on email header analysis, URL and domain reputation analysis, IOC extraction, threat triage, and remediation recommendations.

The objective of this lab was to simulate the workflow of a SOC analyst handling a phishing-related security incident from initial alert through final investigation and documentation.

---

## Objectives

- Analyze a suspicious phishing email
- Investigate email headers and sender information
- Examine malicious URLs and domain reputation
- Extract and document indicators of compromise (IOCs)
- Perform threat triage and classification
- Map observed behavior to MITRE ATT&CK techniques
- Provide remediation recommendations
- Document findings in a professional SOC investigation format

---

## Tools Used

- VirusTotal
- Any.Run
- Cisco Talos Intelligence
- MxToolbox
- AbuseIPDB
- WHOIS Lookup
- Windows Event Viewer
- PowerShell
- Browser Developer Tools

---

## Lab Environment

| Component | Details |
|---|---|
| Operating System | Windows 11 Virtual Machine |
| Investigation Type | Phishing Investigation & Threat Triage |
| Environment | Isolated Home Lab |
| Focus Areas | Email Security, IOC Analysis, Threat Investigation |

---

## Incident Scenario

A user reported receiving a suspicious Microsoft 365 password reset email requesting immediate account verification. The email contained a hyperlink directing the user to a spoofed Microsoft login page designed to harvest user credentials.

The SOC investigation focused on validating the legitimacy of the sender, analyzing email headers, reviewing embedded URLs, identifying indicators of compromise (IOCs), and determining the overall threat severity of the phishing attempt.

The investigation concluded that the email was a credential harvesting phishing attack leveraging spoofed branding and deceptive social engineering techniques.

---

## Initial Alert

| Field | Value |
|---|---|
| Alert Type | Suspicious Phishing Email |
| Reported By | End User |
| Targeted Platform | Microsoft 365 |
| Investigation Priority | Medium |
| Initial Severity | Suspicious |
| Investigation Status | Confirmed Phishing |

---

## Investigation Process

### 1. Initial Email Review

The suspicious email was reviewed to identify indicators commonly associated with phishing attempts, including spoofed branding, urgent language, suspicious sender information, and embedded hyperlinks.

### 2. Email Header Analysis

Email headers were analyzed to validate sender legitimacy and identify potential spoofing attempts. SPF, DKIM, and DMARC validation checks were reviewed along with originating IP information and relay path analysis.

### 3. URL & Domain Investigation

Embedded URLs were extracted and analyzed using multiple threat intelligence platforms to determine domain reputation, registration history, and potential malicious classification.

### 4. Threat Intelligence Correlation

Threat intelligence platforms including VirusTotal, Cisco Talos Intelligence, AbuseIPDB, and WHOIS lookup services were used to investigate domains, IP addresses, and associated indicators.

### 5. IOC Extraction

Indicators of compromise including malicious domains, suspicious IP addresses, URLs, and file hashes were documented and categorized for future detection and response activities.

### 6. Threat Classification

Based on investigation findings, the activity was classified as a credential harvesting phishing attack targeting Microsoft 365 users through social engineering techniques.

---

## Indicators of Compromise (IOCs)

| IOC Type | Indicator | Description |
|---|---|---|
| Domain | login-microsoftverify[.]com | Credential harvesting domain |
| URL | hxxps://login-microsoftverify[.]com/auth | Fake Microsoft 365 login portal |
| IP Address | 185.XXX.XXX.XXX | Suspicious hosting infrastructure |
| Email Subject | Microsoft 365 Password Reset Required | Social engineering lure |
| Sender Address | security-alert@micr0soft-support[.]com | Spoofed sender address |

---

## MITRE ATT&CK Mapping

| Technique ID | Technique | Description |
|---|---|---|
| T1566.002 | Phishing: Link | Malicious phishing link delivery |
| T1204 | User Execution | User interaction required |
| T1071 | Application Layer Protocol | Web protocol communication |
| T1583.001 | Acquire Infrastructure: Domains | Malicious domain registration |

---

## Remediation Recommendations

- Block identified malicious domains and IP addresses
- Reset potentially compromised user credentials
- Enable Multi-Factor Authentication (MFA)
- Conduct phishing awareness training for users
- Monitor for additional phishing activity targeting Microsoft 365 accounts
- Add identified IOCs to SIEM and email filtering solutions
- Review email gateway filtering policies and detection rules

---

## Skills Demonstrated

- Phishing Email Analysis
- Email Header Investigation
- IOC Extraction & Documentation
- Threat Intelligence Correlation
- URL & Domain Reputation Analysis
- MITRE ATT&CK Mapping
- Threat Triage Methodology
- SOC Investigation Documentation
- Security Incident Analysis
- Cyber Threat Investigation

---

## Conclusion

This project simulated a realistic SOC phishing investigation workflow involving threat triage, email analysis, IOC extraction, and remediation planning. The investigation demonstrated the importance of identifying phishing indicators, validating sender legitimacy, and leveraging threat intelligence resources to classify and contain phishing-related threats.

The lab provided practical experience with SOC investigation methodologies, phishing detection techniques, and incident documentation processes commonly used in security operations environments.
