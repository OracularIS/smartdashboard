# Troubleshooting & FAQ

## I signed in, but I don’t see any tenants

Possible causes:

- Your organization request is still pending approval.
- Your user has not been granted access to a tenant.

Actions:

- Use **Check Again** on tenant selection.
- Contact your administrator.

## I see “Access Denied” when opening a tenant link

You don’t have permission for that tenant. Choose another tenant you have access to.

## My dashboard is empty

Dashboards only show data after datasets are uploaded.

- If you manage the integration, push a fresh upload (see: [API Integration](./08-api-docs.md)).
- If you don’t manage the integration, ask your integration owner to push data for this tenant/dashboard.
- Click **Refresh** to reload the latest stored data.

Note: Smart Dashboard is **push-based**. If you have not uploaded data yet, the dashboard will be empty.

## Which data formats are supported?

Smart Dashboard supports **push uploads** through the Upload APIs.

Supported ingestion formats:

- **JSON** (recommended)
- **XML** (legacy)

This is a **push system**: you push data via API and Smart Dashboard displays it.

## How often is data refreshed?

Smart Dashboard does not pull data on a schedule.

Because this is a **push system**, the refresh frequency depends on **how frequently your system pushes data** to the Upload APIs.

In the UI you can use **Refresh** to reload the latest stored data.

## Upload fails with Unauthorized (401)

Your API key may be missing or invalid.

- Make sure your integration is using the correct API key.
- If the key was rotated, update it in your integration secrets.

See: [API Integration (Upload API)](./08-api-docs.md)

## Upload succeeds but data is not visible

- Make sure you’re uploading to the correct tenant and dashboard.
- Make sure you’re using the intended dataset category (data type).
- Refresh the dashboard page.

See: [API Integration (Upload API)](./08-api-docs.md)

## Who can view/rotate the API key?

Only admin roles can access the API Key tab.

---

## Need help?

Contact your support channel or administrator for tenant access and integration help.
