# Defensive Security Fundamentals – SOC Case Study

## Overview
This repository documents hands-on defensive security analysis performed across multiple SOC-related scenarios on TryHackMe. The focus of this work was to understand how a SOC analyst investigates alerts, analyzes logs, validates incidents, and recommends response actions.

The analysis covers:
- Log analysis
- Phishing incident investigation
- Digital forensics basics
- SOC alert triage using structured methodologies

---

## 1. Log Analysis

### Windows Event Logs
- Analyzed Windows Security Event Logs to identify account-related activity.
- Observed "user account creation" followed by a "password reset event".
- Such activity can be legitimate but may also indicate unauthorized access if it occurs unexpectedly.

SOC Consideration:
This activity would require validation against change records and user context to rule out account compromise.

---

### Web Access Logs
- Analyzed web server access logs to review GET and POST requests.
- Identified source IP addresses and destination URLs accessed.
- Observed request patterns that could indicate normal browsing or automated activity.

SOC Consideration:
Unusual request frequency or suspicious endpoints would require correlation with threat intelligence and endpoint logs.

---

## 2. Phishing Incident Analysis

### Scenario
- Investigated an incident involving a malicious file attachment delivered via a phishing email.
- Focused on identifying indicators of compromise related to email-based attacks.

### Analysis
- Reviewed attachment behavior and delivery method.
- Determined the activity to be a **true positive phishing incident**.

### SOC Response Actions
- Isolate the affected endpoint.
- Reset credentials of the impacted user.
- Block sender address and malicious attachment hash.
- Review mail logs for similar messages sent to other users.

MITRE ATT&CK Mapping:
- T1566 – Phishing

---

## 3. Digital Forensics Fundamentals

### File Metadata Analysis
- Used `pdfinfo` to extract metadata from PDF files.
- Identified attributes such as creation date, modification date, and document properties.

### Image Metadata Analysis
- Used `exiftool` to extract EXIF data from image files.
- Metadata assisted in understanding file origin and timeline.

SOC Value:
Metadata analysis supports deeper investigations when malware or suspicious documents are involved.

---

## 4. SOC Alert Triage – Port Scanning Activity

### Scenario
- Analyzed logs indicating **port scanning activity originating from a host within the network.

### Investigation Methodology (5W Analysis)
- What: Port scanning behavior detected
- When: Timestamp identified from logs
- Where: Affected host and network segment
- Who: Source IP / system initiating the scan
- Why: Potential reconnaissance activity

### Verdict
- Activity classified as suspicious.
- Requires validation to determine whether the scan was authorized or malicious.

### SOC Response Actions
- Verify host ownership and purpose.
- Check for indicators of compromise on the scanning host.
- Monitor for lateral movement or follow-up attacks.
- Escalate to Tier 2 SOC if malicious intent is confirmed.

---

## Conclusion
This case study demonstrates practical exposure to SOC workflows, including log analysis, phishing investigation, digital forensics, and alert triage. Effective defensive security relies on structured analysis, log correlation, and accurate decision-making to reduce false positives and identify real threats.

---

## Skills Demonstrated
- SOC alert triage
- Log analysis (Windows and web logs)
- Phishing investigation
- Digital forensics fundamentals
- Incident response concepts
- MITRE ATT&CK mapping
