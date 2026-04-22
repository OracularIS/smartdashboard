# 1) Product Overview

**Smart Dashboard** helps you visualize business/operational data as interactive charts and tables.

It is designed for:

- Teams that want an easy way to view dashboards without building custom UI.
- Integrations that send periodic data updates (XML/JSON) from an external system.
- Organizations that require **tenant isolation** (each tenant’s data is separated).

## Key Concepts

### Tenant

A **tenant** is an organization/workspace inside Smart Dashboard. Every dashboard and dataset belongs to exactly one tenant.

You may have access to **multiple tenants** depending on your role.

### Dashboard

A **dashboard** is a container that holds one or more datasets (Data Files). In the UI, a dashboard is selected from a dropdown.

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

## What you can do

- Select your tenant
- View dashboards and data visualizations
- Create/edit/reorder dashboards
- Add or delete datasets
- Choose how a dataset should be displayed (chart or grid)
- Manage tenant settings (key/value)
- Generate/reveal/rotate tenant Upload API key
- View API documentation and copy/paste integration examples
- Share dashboards via a public link (read-only)
- Use TV Mode to auto-cycle through charts for display screens
