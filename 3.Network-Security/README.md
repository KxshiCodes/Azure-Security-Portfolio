# Network Security

Implemented a layered network security environment in Azure, using network segmentation, traffic filtering, and centralised firewall controls to restrict access to cloud workloads.

## Architecture

![Network Security Architecture](screenshots/network-architecture.png)

The environment combines Azure Virtual Networks, subnets, Network Security Groups, Application Security Groups, Azure Firewall, and route tables to control network access and traffic flow.

## Implementation

### 01. Virtual Network & Subnet Configuration

Created the Azure Virtual Network and subnets to organise workloads and establish network boundaries.

![Virtual Network](screenshots/vnet.png)

### 02. Application Security Groups

Created Application Security Groups (ASGs) to logically group workloads based on their function, allowing security rules to reference application roles rather than individual IP addresses.

![Application Security Groups](screenshots/appsec-groups.png)

### 03. Network Security Groups

Configured Network Security Groups (NSGs) and associated them with the relevant network resources.

Rules were created to control inbound and outbound traffic, restrict management access, and allow required communication.

![Network Security Groups](screenshots/netsec-group.png)

![NSG Association](screenshots/associate-group.png)

![NSG Rules](screenshots/rules-based.png)

### 04. Azure Firewall

Deployed Azure Firewall as a centralised traffic filtering control for the environment.

![Azure Firewall](screenshots/firewall.png)

### 05. Routing & Firewall Policies

Configured route tables to direct selected traffic through Azure Firewall.

Created application and network rules to control outbound access based on destination domains, IP addresses, ports, and protocols.

![Default Route](screenshots/droute.png)

![Application Rules](screenshots/app-rule.png)

![Network Rules](screenshots/net-rule.png)

DNS settings were also configured to support domain resolution within the environment.

![DNS Configuration](screenshots/dservers.png)

## Validation

Tested the network security configuration to verify that access controls and firewall policies behaved as expected.

**Management Access**

Established an RDP connection to the management virtual machine.

![RDP Validation](screenshots/VMMgmt.png)

**Firewall Policy Testing**

Tested outbound connectivity from the internal workload.

- Permitted destinations were accessible.
- Restricted destinations were blocked by firewall policy.

![Firewall Validation](screenshots/test-valid.png)

![Firewall Validation](screenshots/test-valid1.png)

## Outcome

Established a segmented Azure network with NSG-based access controls, workload grouping, and centralised firewall filtering.

Validated management connectivity and outbound traffic restrictions, demonstrating how network security controls can be combined to limit workload exposure and control communication within a cloud environment.
