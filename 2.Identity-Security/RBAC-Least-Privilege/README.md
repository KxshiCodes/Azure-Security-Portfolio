# RBAC & Least Privilege

Implemented a group-based access control model using Microsoft Entra ID security groups and Azure RBAC.

The project uses a simulated Service Desk scenario to demonstrate how Azure permissions can be assigned according to operational responsibilities while limiting unnecessary access.

## Scenario

A Service Desk team requires permissions to manage Azure Virtual Machines as part of its daily operations.

Rather than assigning permissions directly to individual users, access was managed through Microsoft Entra ID security groups and Azure RBAC.

## Architecture

![RBAC architecture](screenshots/rbac-architecture-diagram.png)

**Access model:**

User → Entra ID Security Group → Azure RBAC Role Assignment → Azure Resource

## Implementation

### 01. Security Group Configuration

Created Microsoft Entra ID security groups to represent operational responsibilities and manage access centrally.

![Group Configuration](screenshots/group-config.png)

### 02. Azure RBAC Assignment

Assigned the **Virtual Machine Contributor** role to the Service Desk security group.

This provided virtual machine management permissions without granting unnecessary subscription-level administrative access.

![RBAC Assignment](screenshots/rbac-assignment.png)

![RBAC Assignment](screenshots/rbac-assignment2.png)

### 03. PowerShell Administration

Used Azure PowerShell to demonstrate identity and access management workflows.

![PowerShell Administration](screenshots/powershell-admin.png)

![PowerShell Administration](screenshots/powershell-admin2.png)

### 04. Azure CLI Administration

Used Azure CLI to manage and review RBAC assignments through command-line administration.

![Azure CLI Administration](screenshots/azure-cli.png)

![Azure CLI Administration](screenshots/azure-cli2.png)

## Validation

Verified the access configuration by:

- Reviewing group membership and role assignments.
- Confirming permissions were assigned through the security group.
- Checking the Service Desk group's assigned role and scope.
- Reviewing assigned permissions to identify unnecessary administrative access.

## Outcome

Established a group-based RBAC model that provides the Service Desk team with the permissions required to manage Azure Virtual Machines without granting broader administrative access.

The implementation demonstrates how group-based assignments and role scoping support least-privilege access management.
