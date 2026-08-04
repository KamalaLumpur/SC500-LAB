# Azure RBAC Standard

## Purpose

This document defines the Role-Based Access Control (RBAC) principles used throughout the SC500-LAB environment.

---

## Design Principles

- Follow the Principle of Least Privilege.
- Assign permissions at the smallest appropriate scope.
- Assign roles to Microsoft Entra groups instead of individual users whenever possible.
- Use built-in roles unless a business requirement justifies a custom role.
- Use Privileged Identity Management (PIM) for privileged roles where available.
- Review privileged role assignments regularly.

---

## Standard Roles

| Role | Typical Use |
|------|-------------|
| Owner | Platform administrators requiring full management and RBAC assignment permissions. |
| Contributor | Engineers responsible for managing Azure resources. |
| Reader | Auditors and users requiring read-only access. |
| User Access Administrator | Administrators responsible for managing RBAC assignments only. |

---

## Custom Roles

Create a custom role only when built-in roles grant excessive permissions or do not meet business requirements.

---

## Security Principles

- Minimise permanent privileged access.
- Avoid assigning Owner unless absolutely necessary.
- Prefer group-based assignments over direct user assignments.
- Apply permissions at Resource Group scope where appropriate rather than Subscription scope.