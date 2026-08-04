# Azure Tagging Standard

## Purpose

This document defines the mandatory Azure tagging standard for all resources deployed within the SC500-LAB environment.

---

## Mandatory Tags

| Tag | Example Value | Purpose |
|------|---------------|---------|
| Owner | Cloud Security | Operational ownership |
| Department | Security | Business ownership |
| CostCenter | Training | Cost reporting |
| Environment | LAB | Environment identification |

---

## Design Principles

- Every Azure resource must contain the mandatory tags.
- Tags must be applied consistently across all Resource Groups and resources.
- Team ownership is preferred over individual ownership.
- Azure Policy will be used to enforce compliance where possible.