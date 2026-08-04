# Azure Naming Convention Standard

**Project:** SC500-LAB  
**Version:** 1.0  
**Author:** Sadiq  
**Purpose:** Define the naming standards used throughout the Cloud & AI Security Engineer Bootcamp.

---

# Naming Philosophy

Every Azure resource name should answer the following questions:

- What is it?
- What is its purpose?
- Which environment does it belong to?
- Is it unique?

The objective is to make Azure resources immediately understandable without needing additional documentation.

---

# General Naming Standard

```
<Environment>-<ResourceType>-<Purpose>-<Number>
```

Example:

```
LAB-VM-MANAGEMENT-01
```

Where:

| Component | Meaning |
|----------|---------|
| Environment | LAB / DEV / TEST / PROD |
| Resource Type | VM, VNET, NSG, KV etc. |
| Purpose | MANAGEMENT, HUB, DATA etc. |
| Number | 01, 02, 03... |

---

# Resource Type Abbreviations

| Resource | Abbreviation |
|----------|--------------|
| Resource Group | RG |
| Virtual Machine | VM |
| Virtual Network | VNET |
| Network Security Group | NSG |
| Azure Firewall | AFW |
| Key Vault | KV |
| Storage Account | ST |
| SQL Server | SQL |
| Log Analytics Workspace | LAW |
| Microsoft Sentinel | SENT |
| Managed Identity | MI |
| Application Gateway | AGW |
| Load Balancer | LB |
| Public IP | PIP |

---

# Standard Examples

## Resource Groups

```
RG-SC500-Network
RG-SC500-Identity
RG-SC500-Compute
RG-SC500-Security
```

---

## Virtual Machines

```
LAB-VM-MANAGEMENT-01
LAB-VM-MANAGEMENT-02
```

---

## Virtual Networks

```
LAB-VNET-HUB-01
LAB-VNET-SPOKE-01
```

---

## Azure Firewall

```
LAB-AFW-PERIMETER-01
```

---

## Network Security Groups

```
LAB-NSG-MANAGEMENT-01
```

---

## Key Vault

```
LAB-KV-IDENTITY-01
```

---

## Log Analytics Workspace

```
LAB-LAW-SECURITY-01
```

---

## Storage Accounts

Azure Storage Accounts have additional naming restrictions:

- Lowercase only
- No spaces
- No hyphens
- Globally unique
- Between 3 and 24 characters

Examples:

```
labstdata01
labstlogs01
```

---

# Naming Principles

- Prioritise clarity over short names.
- Use consistent abbreviations.
- Keep names descriptive and predictable.
- Apply the same convention across the entire Azure environment.
- Avoid personal names, dates or temporary labels.

---

# Future Expansion

This document will be updated throughout the bootcamp as additional Azure services are introduced.