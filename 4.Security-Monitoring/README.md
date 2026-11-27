# Microsoft Sentinel Alert Investigation

Investigated a Microsoft Sentinel security incident involving repeated authentication attempts against disabled user accounts from an external IP address.

The investigation focused on analysing authentication activity, validating alert evidence, assessing potential risk, and documenting findings for escalation.

## Incident Details

| Field | Details |
|---|---|
| Incident Type | Suspicious Authentication Activity |
| Severity | Medium |
| Status | Escalated |
| Detection Source | Microsoft Sentinel |
| MITRE ATT&CK | As mapped in Sentinel |

## Investigation

### 01. Incident Triage

Reviewed the Sentinel incident to establish the alert context, severity, affected entities, associated alerts, and MITRE ATT&CK mappings.

![Incident Overview](screenshots/incident-overview.png)

![Incident Details](screenshots/incident-details.png)

### 02. Timeline Analysis

Reviewed the incident timeline to understand the sequence and frequency of authentication attempts.

Focused on source IP activity, targeted accounts, event timestamps, and authentication results.

![Incident Timeline](screenshots/incident-timeline.png)

### 03. Authentication Log Analysis

Pivoted into Log Analytics to investigate the underlying authentication events using KQL.

Reviewed source IP addresses, targeted accounts, authentication results, and related sign-in activity to validate the Sentinel alert.

![Log Analytics Query Results](screenshots/laq.png)

### 04. Entity Investigation

Investigated the associated IP address and affected user accounts to gather additional context.

Reviewed available IP information, geolocation data, account details, and related authentication activity.

![Entity Investigation](screenshots/entity-investigation.png)

![IP Details](screenshots/ip-analysis.png)

## Key Findings

| Indicator | Finding |
|---|---|
| Source IP | 175.45.176.99 |
| Target Accounts | Disabled user accounts |
| Authentication Activity | Multiple failed sign-in attempts |
| Detection | Sign-ins from IPs attempting authentication to disabled accounts |

The activity was considered suspicious and required further investigation to establish its scope and potential impact.

## Incident Outcome

The investigation was documented and an escalation task was created for the SOC Level 2 team.

The escalation included the identified indicators, affected accounts, authentication activity, and supporting investigation evidence for further threat hunting.

![SOC Level 2 Escalation](screenshots/escalation-task.png)

## Recommendations

- Continue monitoring authentication attempts associated with the identified IP.
- Investigate related activity across other user accounts.
- Review detection coverage for suspicious authentication patterns.
- Enrich alerts with threat intelligence and IP reputation data.
