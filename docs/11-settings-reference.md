# 11) Settings Reference

This page explains the **tenant settings** that affect Smart Dashboard behavior.

You can manage settings in **Data Management → Settings**.

> Settings are **tenant-specific**. Changing a setting affects only the currently selected tenant.

> Note: TV mode also has **viewer settings** (slide duration, refresh interval, etc.). Those are not tenant settings and are saved locally in your browser. See: [Sharing & TV Mode](./09-sharing-and-tv-mode.md).

## allow_public_sharing

**Purpose**: Controls whether dashboards in the tenant can be shared publicly (read-only).

- `true` → users can generate public share links
- `false` → public sharing is disabled (default)

Where it is used:

- The **Share Dashboard** dialog checks this setting and disables public sharing when it is `false`.
- Public routes under `/shared/<token>` are blocked if this setting is disabled.

## Dashboard-Title

**Purpose**: Sets the default dashboard title used in places like TV mode headers.

Notes:

- This key is **case-sensitive** and should be exactly `Dashboard-Title`.
- Some older tenants may have a legacy key `dashboard-title`. If you see both, prefer `Dashboard-Title`.

Recommended value:

- A short label like `Dashboard`, `KPI Dashboard`, or your organization name.

## Other settings

Your tenant may have additional settings that are specific to your organization’s setup.
If you are unsure what a setting does, contact your administrator or support.
