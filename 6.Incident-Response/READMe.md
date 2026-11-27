# Phishing Incident Investigation

Investigated a simulated phishing attempt impersonating a legitimate payment service provider, focusing on email analysis, indicators of compromise, and potential identity compromise.

## Incident Details

| Field | Details |
|---|---|
| Incident Type | Phishing |
| Severity | Medium |
| Status | Resolved |
| Outcome | No confirmed account compromise |

## Investigation

### Email Analysis

Reviewed sender information, email headers, SPF/DKIM/DMARC authentication results, sender domains, and embedded URLs to assess the legitimacy of the reported email.

### IOC Investigation

Identified a lookalike domain impersonating a legitimate service and a suspicious URL directing users to a fake login page.

### Identity Investigation

Reviewed Microsoft Entra ID sign-in activity to identify suspicious authentication attempts and potential credential misuse.

### Impact Assessment

Correlated available email and identity telemetry to determine whether the phishing attempt resulted in credential exposure or further suspicious activity.

## Key Findings

- Identified a lookalike phishing domain.
- Identified suspicious email authentication results.
- Identified a URL directing users to a fake authentication page.
- Found no evidence of successful authentication or subsequent suspicious identity activity.

## Incident Outcome

The investigation concluded that the phishing attempt was unsuccessful.

No evidence of credential compromise, malware execution, or further malicious activity was identified in the available telemetry.

Recommended response measures included blocking identified indicators, strengthening email authentication controls, and improving phishing detection and identity monitoring.

---

**Disclaimer:** This case study is based on a simulated investigation conducted in a corporate security training environment. Organisational details, indicators, and sensitive information have been anonymised or redacted.
