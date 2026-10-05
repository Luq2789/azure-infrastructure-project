# Azure Infrastructure Project

A hands-on Microsoft Azure infrastructure project built to develop practical cloud and networking skills alongside AZ-900 preparation.

## Project Overview

This project demonstrates the deployment and configuration of core Azure infrastructure and governance services.

The environment was designed with a focus on networking, storage, security, access control, governance and cost management.

## Architecture

The project contains:

- Azure Resource Group
- Azure Virtual Network (VNet)
- Management subnet
- Server subnet
- Network Security Group (NSG)
- Azure Storage Account
- Azure Blob Storage container
- Azure RBAC
- Azure Resource Lock
- Azure Policy
- Azure Cost Management
- Azure Advisor

## Network Configuration

### Virtual Network

**Name:** `vnet-azure-infrastructure`

**Address space:**
`10.0.0.0/16`

### Subnets

| Subnet | Address Range | Purpose |
|---|---|---|
| `snet-management` | `10.0.1.0/24` | Management resources |
| `snet-server` | `10.0.2.0/24` | Server resources |

## Network Security

A Network Security Group named:

`nsg-server`

was associated with the server subnet.

An inbound RDP rule was configured to demonstrate Azure NSG traffic filtering.

## Storage

A StorageV2 account was created using:

- **Performance:** Standard
- **Redundancy:** LRS
- **Primary workload:** Azure Blob Storage
- **Container:** `portfolio-data`

The container was configured with private access and a test file was uploaded to demonstrate Blob Storage functionality.

## Identity and Access Management

Azure Role-Based Access Control (RBAC) was configured using:

**Storage Blob Data Contributor**

This demonstrates assigning permissions to Azure resources based on user roles rather than giving unnecessary full administrative access.

## Governance

### Resource Lock

A `CanNotDelete` resource lock was applied to protect the infrastructure from accidental deletion.

### Azure Policy

An **Allowed locations** policy was assigned to the project resource group to demonstrate Azure Policy-based governance.

### Azure Advisor

Azure Advisor was reviewed to demonstrate Azure recommendations for areas such as:

- Cost
- Security
- Reliability
- Performance
- Operational excellence

## Cost Management

Azure Cost Management was reviewed to monitor resource spending and ensure the project remained within the available Azure Free Account credit.

No unnecessary paid resources were intentionally deployed.

## VM Availability

A virtual machine was planned as part of the infrastructure design. However, the required VM SKUs were unavailable for the Azure subscription in the selected regions.

Rather than upgrading the subscription or creating unnecessary costs, the VM component was not deployed.

The rest of the networking, storage, security and governance components were implemented successfully.

## Skills Demonstrated

- Microsoft Azure
- Azure Virtual Networks
- IPv4 addressing and subnetting
- Network Security Groups
- Azure Storage
- Blob Storage
- Azure RBAC
- Azure Policy
- Resource Locks
- Azure Cost Management
- Azure Advisor
- Cloud networking
- Cloud security
- Cloud governance

## Evidence

Screenshots documenting the implementation are available in the [`screenshots`](screenshots/) folder.

## Key AZ-900 Concepts Practised

This project provided practical experience with:

- Azure resource hierarchy
- Virtual networking
- Subnetting
- Network security
- Storage services
- RBAC
- Governance
- Policy
- Resource locks
- Cost management
- Azure Advisor