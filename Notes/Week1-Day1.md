# Week 1 - Day 1
## Azure Hierarchy & Resource Groups

---

# Azure Hierarchy

Azure follows a hierarchical structure:

```text
Management Group
        │
Subscription
        │
Resource Group
        │
Resources
```

- **Management Group** – Used to organise multiple Azure subscriptions.
- **Subscription** – Billing and management boundary.
- **Resource Group** – Logical container for Azure resources.
- **Resources** – Virtual Machines, Storage Accounts, Key Vaults, VNets, Firewalls, etc.

---

# Subscription vs Resource Group

## Subscription

- Highest billing and management boundary I work with.
- Contains one or more Resource Groups.
- Associated with an Azure tenant.
- My subscription:

```
SC500-LAB
```

---

## Resource Group

A Resource Group is a **logical container** for Azure resources.

Resources inside a Resource Group should generally share:

- Purpose
- Lifecycle
- Management requirements

A Resource Group is:

- ✅ Logical container
- ❌ Not a security boundary
- ❌ Not a physical location

Example:

```text
SC500-LAB
│
├── RG-SC500-Management
├── RG-SC500-Network
├── RG-SC500-Identity
└── RG-SC500-Monitoring
```

---

# Can a Resource Group contain multiple Azure regions?

**Yes.**

A Resource Group is **logical**, not geographical.

Example:

```text
RG-SC500-Management

VM               → UK South
Storage Account  → UK South
Key Vault        → West Europe
```

Although Azure allows multiple regions within the same Resource Group, most organisations keep related resources in the same region for simplicity, performance and compliance.

For this lab, almost everything will be deployed in **UK South**.

---

# Why use multiple Resource Groups?

Using multiple Resource Groups provides:

- Better organisation
- Easier administration
- Better visibility
- Simpler deployments
- Easier deletion of related resources
- Cleaner monitoring
- Better RBAC management
- Improved cost management

Example:

```text
RG-SC500-Network

- Virtual Network
- Azure Firewall
- NSGs
- Public IPs
```

```text
RG-SC500-Monitoring

- Log Analytics
- Microsoft Sentinel
- Automation Account
```

Resources that share the same lifecycle should generally be placed in the same Resource Group.

---

# Azure CLI Commands Learned

## Login to Azure

```powershell
az login
```

Authenticates to Azure.

---

## Show current subscription

```powershell
az account show --output table
```

Displays the active Azure subscription.

---

## List all Resource Groups

```powershell
az group list --output table
```

Lists every Resource Group in the current subscription.

---

## Show one specific Resource Group

```powershell
az group show --name RG-SC500-Management --output table
```

Displays information about a single Resource Group.

---

# Key Takeaways

- Azure uses a hierarchy:
  - Management Group
  - Subscription
  - Resource Group
  - Resources

- A Resource Group is a logical container, not a security boundary.

- Resources in the same Resource Group should generally share the same purpose and lifecycle.

- A Resource Group can contain resources deployed in multiple Azure regions.

- Azure Portal and Azure CLI both communicate with Azure Resource Manager (ARM).

---

# Interview Notes

### What is a Resource Group?

A Resource Group is a logical container for Azure resources that share a common purpose, lifecycle and management requirements. It simplifies deployment, organisation, monitoring, RBAC and resource management. A Resource Group is **not** a security boundary and can contain resources deployed across multiple Azure regions.

---

# Commands to Remember

```powershell
az login

az account show --output table

az group list --output table

az group show --name RG-SC500-Management --output table
```

---

# Lab Completed

- ✅ Created first Azure Resource Group
- ✅ Used Azure Portal
- ✅ Used Azure CLI
- ✅ Verified Azure subscription
- ✅ Queried Resource Groups using Azure CLI
- ✅ Queried a specific Resource Group using Azure CLI