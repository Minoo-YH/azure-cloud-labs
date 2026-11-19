# ☁️ Azure Cloud Labs

### Hands-on Microsoft Azure Cloud Computing Portfolio

A collection of practical cloud computing labs focused on deploying, configuring, managing, and documenting Microsoft Azure services.

This repository demonstrates my hands-on learning journey in cloud infrastructure, virtual machines, networking, storage, databases, and command-line administration using **Microsoft Azure for Students**.

The goal is to develop practical cloud engineering skills and document real-world configurations, technical decisions, security considerations, and lessons learned.

---

## 🎯 Project Objectives

- Gain practical experience with Microsoft Azure services.
- Deploy and manage cloud infrastructure through the Azure Portal.
- Understand virtual networking, subnets, and IP addressing.
- Explore cloud storage and managed database services.
- Learn Azure CLI for command-line resource management.
- Apply basic cloud security and cost management practices.
- Build a documented technical portfolio for entry-level cloud engineering and IT infrastructure roles.

## 🛠️ Technologies & Tools

| Technology | Purpose |
|---|---|
| Microsoft Azure | Cloud computing platform |
| Azure Portal | Resource deployment and management |
| Azure Virtual Machines | Compute infrastructure |
| Azure Virtual Network | Private cloud networking |
| Network Security Groups | Network traffic control |
| Azure Blob Storage | Object storage (planned) |
| Azure SQL Database | Managed relational database (planned) |
| Azure CLI | Command-line management (planned) |
| Linux (Ubuntu) | Virtual machine operating system |
| Git & GitHub | Version control and documentation |

## 📚 Hands-on Labs

| Lab | Description | Status |
|---|---|---|
| [01 — Azure Virtual Machine](01-azure-virtual-machine/) | Deploy and configure a Linux virtual machine | 🟡 Deployed; operational verification pending |
| 02 — Azure Virtual Network | Configure a VNet and subnet, and verify VM network association | 🟢 Configuration verified; documentation pending |
| 03 — Azure Blob Storage | Create a storage account and manage blob containers | ⚪ Planned |
| 04 — Azure SQL Database | Deploy a managed SQL database and explore basic queries | ⚪ Planned |
| 05 — Azure CLI | Manage Azure resources using command-line tools | ⚪ Planned |

Lab statuses reflect verified progress and will be updated as additional implementation and testing steps are completed.

---

## 🏗️ Current Azure Infrastructure

The current lab environment uses an Azure for Students subscription, with resources deployed in the **Sweden Central** region.

### Resource Configuration

| Resource | Configuration |
|---|---|
| Resource Group | `rg-azure-portfolio` |
| Region | Sweden Central |
| Virtual Machine | `vm-ubuntu-lab01` |
| Operating System | Linux |
| VM Size | `Standard_B2ats_v2` |
| Virtual Network | `vnet-swedencentral-1` |
| VNet Address Space | `172.16.0.0/16` |
| Subnet | `snet-swedencentral-1` |
| Subnet Address Range | `172.16.0.0/24` |
| DNS | Azure-provided DNS |
| VM State at Last Review | Stopped (deallocated) |

### Network Architecture

```text
Microsoft Azure
│
└── Resource Group: rg-azure-portfolio
    │
    └── Region: Sweden Central
        │
        ├── Virtual Network
        │   vnet-swedencentral-1
        │   172.16.0.0/16
        │   │
        │   └── Subnet
        │       snet-swedencentral-1
        │       172.16.0.0/24
        │       │
        │       └── Virtual Machine
        │           vm-ubuntu-lab01
        │           Linux
        │
        ├── Network Security Group
        │   vm-ubuntu-lab01-nsg
        │
        └── Public IP Resource
            vm-ubuntu-lab01-ip
```

This architecture represents the resources identified in the Azure Portal. Network Security Group rule validation, SSH connectivity, and end-to-end traffic testing are not yet documented.

---

## 🔬 Lab Highlights

### Lab 01 — Azure Virtual Machine

**Objective:** Deploy and manage a Linux virtual machine using the Azure Portal.

**Implementation progress:**
- Created a Linux virtual machine.
- Selected the Sweden Central Azure region.
- Configured the virtual machine size.
- Provisioned associated networking resources.
- Reviewed the VM state in Azure Portal.
- Deallocated the VM to avoid unnecessary compute usage.

**Verification:** The VM resource exists in Azure, but successful SSH access and operating system functionality have not yet been verified.

[View Lab 01](01-azure-virtual-machine/)

### Lab 02 — Azure Virtual Network

**Objective:** Configure private cloud networking for Azure resources.

**Implementation progress:**
- Created an Azure Virtual Network.
- Configured the address space `172.16.0.0/16`.
- Created a subnet using `172.16.0.0/24`.
- Reviewed available subnet IP addresses.
- Verified the VM's association with the VNet and subnet in Azure Portal.

**Verification:** Virtual network configuration and VM network association confirmed. Connectivity testing remains outside the current verification scope.

### Lab 03 — Azure Blob Storage

**Planned activities:**
- Create an Azure Storage Account.
- Configure a blob container.
- Upload and manage files.
- Review access permissions and storage security.

### Lab 04 — Azure SQL Database

**Planned activities:**
- Deploy an Azure SQL Database.
- Configure database access.
- Connect to the database.
- Execute basic SQL queries.
- Review database security and cost considerations.

### Lab 05 — Azure CLI

**Planned activities:**
- Access Azure Cloud Shell or install Azure CLI.
- Explore resource management commands.
- List and inspect Azure resources.
- Practice command-line infrastructure administration.

---

## 🔐 Security Best Practices

Security is considered throughout the labs.

- Avoid committing passwords, private SSH keys, access tokens, and database connection strings.
- Review Network Security Group rules and restrict inbound access.
- Apply least-privilege access principles.
- Avoid unnecessary exposure of services to the public internet.
- Remove or redact sensitive information from screenshots.
- Review Azure resource permissions and configuration before sharing documentation.

## 💰 Cost Management

The labs use an Azure for Students subscription.

Cost-awareness practices include:

- Selecting appropriately sized resources for learning.
- Reviewing estimated costs before deployment.
- Deallocating unused virtual machines.
- Monitoring Azure credit consumption.
- Removing unnecessary resources after exercises.
- Considering persistent storage and public IP costs even when a VM is deallocated.

## 📂 Repository Structure

```text
azure-cloud-labs/
│
├── README.md
│
├── 01-azure-virtual-machine/
│
├── 02-virtual-network/        # To be documented
│
├── 03-blob
