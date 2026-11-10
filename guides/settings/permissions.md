---
description: Control what your team members can access in AeroQuote.
---

# 🔐 Permissions

The Permissions page lets you manage user accounts and control what each team member can see and do in AeroQuote.

---

## Accessing Permissions

1. Go to **Settings** from the sidebar
2. Click **Permissions** (or navigate to Settings → Permissions)

---

## User List

The Permissions page shows all users with access to your AeroQuote account:

| Column | Description |
|--------|-------------|
| **Name** | User's full name |
| **Email** | Login email address |
| **Role** | Their permission level |
| **Status** | Active or inactive |
| **Last Login** | When they last accessed AeroQuote |

---

## Adding a New User

1. Click **Add User**
2. Enter the user's details:
   - **Name** — Full name
   - **Email** — Their login email (must be unique)
   - **Role** — Select their permission level
3. Click **Save**

The user receives an email invitation to set up their password.

---

## User Roles

AeroQuote uses role-based permissions:

| Role | Access Level |
|------|--------------|
| **Owner** | Full access to everything including billing |
| **Admin** | Full access except billing and account deletion |
| **Manager** | Create and manage quotes, bookings, and contacts |
| **User** | View and work with assigned items |
| **Read-only** | View only, no editing capabilities |

{% hint style="info" %}
Role names and permissions may vary based on your subscription plan. Contact support for custom role configurations.
{% endhint %}

---

## Editing User Permissions

1. Find the user in the list
2. Click **Edit**
3. Update their role or details
4. Click **Save**

---

## Deactivating a User

When someone leaves your organization:

1. Find their account
2. Click **Deactivate** (or toggle Status to Inactive)
3. Confirm the change

{% hint style="warning" %}
Deactivated users cannot log in but their activity history is preserved. Use this instead of deleting to maintain audit trails.
{% endhint %}

---

## Reactivating a User

To restore access:

1. Find the deactivated user
2. Click **Activate** (or toggle Status to Active)
3. They can log in again with their existing credentials

---

## Best Practices

{% hint style="success" %}
**Principle of least privilege** — Give users only the access they need to do their job.
{% endhint %}

- Review permissions quarterly
- Deactivate users immediately when they leave
- Use Admin role sparingly
- Keep at least two Owner accounts for redundancy

---

## Aircraft - Maintenance Totals

The **Aircraft - Maintenance Totals** permission controls who can set or update a dated maintenance baseline on the web and in the Crew app. Aircraft edit permission also allows this.

By default it is granted to the account administrator, manager, chief pilot and crew roles. An account administrator can add or remove it from a role on this page.

See [Update a baseline](../aircraft/maintenance-limits.md#update-a-baseline).

---

## Maintenance - Sign Off

The **Maintenance - Sign Off** permission controls who can record a program-item sign-off on the Maintenance Tracker. It is granted by default to every role that has aircraft edit permission. An account administrator can add or remove it from a role on this page.

See [Record a sign-off](../aircraft/maintenance-tracker.md#record-a-sign-off).

---

## Maintenance - View Records

The **Maintenance - View Records** permission controls who can open **Record history** and export it as CSV or PDF. It is granted by default to every role that has aircraft edit permission. An account administrator can add or remove it from a role on this page.

See [Record history](../aircraft/maintenance-tracker.md#record-history).

