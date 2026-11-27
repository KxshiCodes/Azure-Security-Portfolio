
# Phishing Incident Investigation

A simulated SOC incident investigation focused on identifying a phishing attempt, analysing indicators of compromise (IOCs), and assessing potential identity compromise within a Microsoft Azure security environment.

## Overview

Investigated a phishing email impersonating a legitimate payment service provider. The investigation aimed to determine whether the email was malicious, whether credentials were potentially exposed, and whether any subsequent suspicious identity activity occurred.

**Incident classification:** Phishing  
**Severity:** Medium  
**Status:** Resolved  
**Outcome:** No confirmed account compromise

## Tools & Technologies

- Microsoft Sentinel
- Microsoft Defender for Office 365
- Microsoft Entra ID
- Azure Monitor

## Investigation

The investigation followed a structured incident response workflow:

- **Email Analysis:** Reviewed sender details, email headers, SPF/DKIM/DMARC results, suspicious domains, and embedded URLs.
- **IOC Investigation:** Identified and assessed indicators associated with the suspected phishing infrastructure.
- **Identity Investigation:** Reviewed Entra ID sign-in activity for suspicious authentication attempts and potential credential misuse.
- **Impact Assessment:** Correlated available security evidence to determine whether the phishing attempt resulted in further malicious activity.

## Key Findings

- Identified a lookalike domain impersonating a legitimate service.
- Identified suspicious email authentication results and a link directing users to a fake login page.
- Reviewed available identity telemetry for signs of credential compromise.
- Found no evidence of successful authentication or subsequent suspicious activity.

## Incident Outcome

The investigation concluded that the phishing attempt was unsuccessful, with no confirmed credential compromise, malware execution, or further malicious activity identified in the available evidence.

Recommended response measures included blocking identified indicators, strengthening email authentication controls, improving phishing detection, and monitoring identity activity.

## Key Skills Demonstrated

Phishing Analysis · IOC Investigation · Email Authentication · Microsoft Sentinel · Entra ID Sign-in Analysis · Incident Response · Security Event Correlation

---

**Disclaimer:** This case study is based on a simulated investigation conducted in a corporate security training environment. Organisational details, indicators, and sensitive information have been anonymised or redacted.
