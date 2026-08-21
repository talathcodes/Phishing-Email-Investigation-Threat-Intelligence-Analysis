# Phishing Email Investigation & Threat Intelligence Analysis

## Overview

This project demonstrates a Security Operations Center (SOC) Level 1
investigation of a suspected phishing/brand-impersonation email.

The investigation involved analyzing raw email headers, authentication
results, sender infrastructure, domains, IP addresses, URLs, and threat
intelligence data.

The objective was to determine whether the email represented a legitimate
business communication or a potential phishing/impersonation attempt.

---

## Objectives

- Analyze raw email headers
- Investigate email authentication mechanisms
- Extract Indicators of Compromise (IOCs)
- Investigate IP addresses and domains using VirusTotal
- Perform WHOIS/RDAP analysis
- Analyze URLs without directly visiting suspicious links
- Correlate infrastructure and identity indicators
- Determine the final risk classification
- Document findings from an L1 SOC analyst perspective

---

## Tools Used

- VS Code
- VirusTotal
- WHOIS / RDAP
- DNS analysis
- MITRE ATT&CK
- Web-based threat intelligence

---

## Investigation Workflow

Email
  ↓
Header Analysis
  ↓
Authentication Analysis
  ↓
IOC Extraction
  ↓
Threat Intelligence
  ↓
Infrastructure Correlation
  ↓
URL Analysis
  ↓
Identity Verification
  ↓
Risk Assessment
  ↓
Final Verdict

---

## Key Findings

The investigation identified several suspicious indicators:

1. DMARC authentication failure for the claimed sender domain.
2. Email infrastructure associated with `wintermute.business`.
3. A PHP mailer script hosted under the `wintermute.business` domain.
4. The domain had been registered shortly before the analyzed email.
5. VirusTotal showed a malicious classification from Bfore.Ai for
   `wintermute.business`.
6. The email contained a Telegram invitation link.
7. The claimed sender identity could not be independently verified.
8. Multiple infrastructure indicators were identified and investigated.

---

## IOC Summary

| Type | Indicator | Result |
|---|---|---|
| IP | 77.37.35.56 | 0/91 VT detections |
| Domain | srv1862.main-hosting.eu | 0/91 VT detections |
| IP | 146.70.104.28 | 0/91 VT detections |
| Domain | wintermute.business | 1/91; Bfore.Ai malicious |
| URL | Telegram invitation | 0/92 VT detections |

---

## Final Assessment

The email was assessed as a likely phishing/brand-impersonation attempt
with high confidence.

The conclusion was based on correlation of multiple indicators rather
than relying on a single threat-intelligence detection.

Key evidence included authentication failure, suspicious infrastructure,
domain registration timing, malicious domain classification, and an
unverified sender identity.

---

## Skills Demonstrated

- Email Header Analysis
- Phishing Investigation
- IOC Extraction
- Threat Intelligence
- VirusTotal Analysis
- WHOIS/RDAP Analysis
- DNS Analysis
- Email Authentication Analysis
- Security Investigation
- Evidence Correlation
- SOC L1 Alert Triage
- Incident Documentation
