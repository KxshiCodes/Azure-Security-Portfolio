# Azure Foundation

Built the foundational Azure environment used throughout this portfolio, establishing the infrastructure for centralised logging, security monitoring, and incident investigation.

## Architecture

![Azure Foundation Architecture](screenshots/architecture-diagram.jpg)

The environment includes Azure resources, a Log Analytics Workspace, Microsoft Sentinel, and a Windows virtual machine providing endpoint security telemetry.

## Implementation

### 01. Azure Infrastructure

Created the Azure resource group and deployed the core resources required for the security environment.

![Resource Group](screenshots/01-resource-group.png)

### 02. Log Analytics Workspace

Deployed a Log Analytics Workspace to centralise security telemetry and provide a foundation for log analysis using KQL.

![Log Analytics](screenshots/02-log-analytics.png)

### 03. Microsoft Sentinel

Enabled Microsoft Sentinel and connected it to the Log Analytics Workspace for security monitoring and incident investigation.

![Sentinel Enabled](screenshots/03-sentinel-enabled.png)

### 04. Security Data Connectors

Configured data connectors to ingest security telemetry from available Azure and Windows sources.

![Data Connectors](screenshots/04-data-connectors.png)

### 05. Virtual Machine Monitoring

Connected an Azure Windows virtual machine to the monitoring environment to provide endpoint security telemetry.

![VM Telemetry](screenshots/05-vm-telemetry.png)

### 06. Windows Security Auditing

Enabled Windows auditing policies to generate security events covering authentication and system activity.

![Windows Auditing](screenshots/06-windows-auditing.png)

### 07. KQL Validation

Used KQL queries to verify log ingestion and inspect available security events within the Log Analytics Workspace.

![KQL Validation](screenshots/07-kql-query.png)

## Outcome

Established a working Azure security environment with centralised log collection, Microsoft Sentinel integration, and Windows security telemetry.

Validated that security events were being ingested and could be queried for subsequent monitoring and investigation activities.

This environment serves as the foundation for the remaining security projects in this portfolio.
