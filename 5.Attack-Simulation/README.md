# Attack Simulation & Security Validation

Controlled attack simulations investigated from a defensive security perspective using Microsoft Defender XDR.

The project examines how common attacker techniques generate endpoint telemetry, how Defender identifies suspicious activity, and how security alerts can be investigated using process activity, incident timelines, and Advanced Hunting.

## Investigation Overview

Five attack scenarios were investigated across different MITRE ATT&CK tactics.

| Scenario | Defender Detection | Severity |
|---|---|---|
| Execution | Suspicious script content observed | Medium |
| Credential Access | Suspicious account and device activity | As reported |
| Privilege Escalation | UAC bypass detected | Medium |
| Defence Evasion | Attempt to disable Defender Antivirus | High |
| Lateral Movement | Compromised account conducting hands-on-keyboard attack | High |

## Attack Simulations

### 01. Execution

Investigated suspicious script execution detected on a Windows 11 device.

Microsoft Defender XDR generated a medium-severity alert: **"A script with suspicious content was observed."**

The investigation covered the affected device, user account, process activity, and command-line information.

The process investigation identified `cmd.exe` activity involving `csc.exe`, which was used to compile a C# file associated with the simulation.

![Attack Activity](screenshots/execution-activity.png)

![Defender Investigation](screenshots/execution-investigation.png)

![Investigation Evidence](screenshots/execution-evidence.png)

**MITRE ATT&CK:** T1059.003 – Windows Command Shell; T1218.014 – MMC.

### 02. Credential Access

Investigated suspicious account and device activity initially associated with a potential password-spray scenario.

The investigation reviewed affected accounts, device activity, authentication evidence, and related alerts.

Available Defender telemetry identified a compromised account and additional suspicious activity on the affected device. The initial password-spray hypothesis was not confirmed.

Advanced Hunting was used to investigate additional activity associated with the device.

![Attack Activity](screenshots/credential-access-activity.png)

![Defender Investigation](screenshots/credential-access-investigation.png)

![Investigation Evidence](screenshots/credential-access-evidence.png)

![Advanced Hunting](screenshots/credential-access-hunting.png)

**MITRE ATT&CK:** T1033 – System Owner/User Discovery; T1087 – Account Discovery; T1069 – Permission Groups Discovery.

### 03. Privilege Escalation

Investigated a simulated User Account Control (UAC) bypass detected on a Windows 11 device.

Microsoft Defender XDR generated a medium-severity alert: **"UAC bypass was detected."**

The investigation involved reviewing process activity, command-line information, registry modifications, and the process tree.

The evidence provided context for the attempted privilege escalation and how the activity was executed.

![Attack Activity](screenshots/privilege-escalation-activity.png)

![Defender Investigation](screenshots/privilege-escalation-investigation.png)

**MITRE ATT&CK:** T1548.002 – Bypass User Account Control; T1112 – Modify Registry.

### 04. Defence Evasion

Investigated an attempt to modify Microsoft Defender Antivirus security settings.

Microsoft Defender XDR generated a high-severity alert relating to an attempt to turn off Defender Antivirus protection.

The investigation identified PowerShell activity attempting to modify Defender configuration through registry changes.

Process, command-line, device, and user information were reviewed to establish the nature of the activity.

![Defender Alert](screenshots/defence-evasion-alert.png)

![Defender Investigation](screenshots/defence-evasion-investigation.png)

![Registry Evidence](screenshots/defence-evasion-registry.png)

**MITRE ATT&CK:** T1562.001 – Impair Defenses: Disable or Modify Tools.

### 05. Lateral Movement

Investigated a hands-on-keyboard incident involving a compromised account.

Microsoft Defender XDR generated a high-severity alert: **"Compromised account conducting hands-on-keyboard attack."**

The investigation covered the incident timeline, affected device, process activity, related alerts, and suspicious PowerShell execution.

Defender also detected and prevented execution of a malicious PowerShell component.

Additional evidence revealed domain controller discovery and account-related discovery activity.

![Attack Activity](screenshots/lateral-movement-activity.png)

![Defender Investigation](screenshots/lateral-movement-investigation.png)

![Investigation Evidence](screenshots/lateral-movement-evidence.png)

**MITRE ATT&CK:** T1033 – System Owner/User Discovery; T1087 – Account Discovery; T1069 – Permission Groups Discovery.

## Investigation Approach

Across the five scenarios, investigations focused on:

- Reviewing Defender alerts and incident severity.
- Identifying affected devices and user accounts.
- Analysing process trees and command-line activity.
- Reviewing incident timelines and related security events.
- Using Advanced Hunting to investigate additional activity.
- Mapping observed behaviour to MITRE ATT&CK.
- Identifying appropriate defensive improvements.

## Outcome

The simulations provided practical experience investigating attacker behaviour through Microsoft Defender XDR.

They demonstrated how endpoint telemetry, process activity, incident correlation, and Advanced Hunting can support the identification and investigation of suspicious activity.

A key focus throughout the project was validating alert findings against available evidence rather than relying solely on the initial detection description.
