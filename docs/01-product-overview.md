
# Product Overview

**Smart Dashboard** is a lightweight dashboarding / KPI tool.

It is a **push-based** system:

- You push data from your systems (via API)
- Smart Dashboard stores it per tenant and displays it as charts or tables

It is designed for:

- Teams that want an easy way to view dashboards without building custom UI.
- Integrations that push periodic data updates (JSON recommended; XML supported for legacy).
- Organizations that require **tenant isolation** (each tenant’s data is separated).

## How data gets into Smart Dashboard

Smart Dashboard is a **push system**:

- Your organization pushes data into Smart Dashboard using the Upload APIs.
- Smart Dashboard stores it per tenant and displays it.

This design keeps integrations flexible:

- If your data lives in another system (including internal apps, reporting pipelines, or exports), your integration can transform it and push updates whenever you need.
- The dashboard updates in the UI when new data is pushed (and when users refresh their view).

## Key Concepts

### Tenant

A **tenant** is an organization/workspace inside Smart Dashboard. Every dashboard and dataset belongs to exactly one tenant.

You may have access to **multiple tenants** depending on your role.

### Dashboard

A **dashboard** is a container that holds one or more datasets (**data files**). In the UI, a dashboard is selected from a dropdown.

### Data File (Dataset)

A **Data File** is a dataset (for example: Sales, Inventory, Orders) uploaded into a specific dashboard. Each dataset renders as:

- a chart (line/bar/area/pie)
- or a table/grid

### Data Type

Each dataset has a **Data Type** (e.g., `Sales`, `Inventory`). Data Type is used to label and replace datasets.

### Upload API Key

Uploads from external systems use a **tenant-scoped API key**.

- Only authorized admin roles can view/rotate this key.
- Rotating the key revokes the old key immediately.

---

## How the pages connect (recommended reading)

If you’re reading this guide end-to-end, the typical flow is:

1. [Getting Started](./02-getting-started.md)
2. [Login](./03-login.md)
3. [Tenant Selection](./04-tenant-selection.md)
4. [Home Page](./05-home-page.md)
5. [Dashboards](./06-dashboards-page.md)
6. (Admin) [Data Management](./07-data-management.md)
7. (Integration) [API Integration (Upload API)](./08-api-docs.md)

---

## What you can do

- Select your tenant
- View dashboards and data visualizations
- Create/edit/reorder dashboards
- Add or delete datasets
- Choose how a dataset should be displayed (chart or grid/table)
- Choose chart types per dataset (Line, Bar, Area, Pie, Table)
- Use **Stacked** or **Clustered** bars for multi-series datasets
- Manage tenant settings (key/value)
- Generate/reveal/rotate tenant Upload API key
- View API documentation and copy/paste integration examples
- Share dashboards via a public link (read-only)
- Use TV Mode to auto-cycle through charts for display screens
