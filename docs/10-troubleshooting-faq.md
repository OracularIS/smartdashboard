# 10) Troubleshooting & FAQ

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

- Confirm your integration is posting to `/api/upload-data` or `/api/upload-xml`.
- Confirm headers include the correct `X-Tenant-Id` and dashboard selection.
- Try refreshing the dashboard.

Note: Smart Dashboard is **push-based**. If you have not uploaded data yet, the dashboard will be empty.

## Which data formats are supported?

Smart Dashboard supports **push uploads** through the Upload APIs.

Supported ingestion formats:

- **JSON** (recommended)
- **XML** (legacy)

We do **not** directly support uploading spreadsheet files (for example Excel/XLS) and we do **not** directly connect to databases.

## How often is data refreshed?

Smart Dashboard does not pull data on a schedule.

Because this is a **push system**, the refresh frequency depends on **how frequently your system pushes data** to the Upload APIs.

In the UI you can use **Refresh** to reload the latest stored data.

## Upload fails with Unauthorized (401)

Your API key may be missing or invalid.

- Confirm you are sending `x-api-key`.
- If the key was rotated, update your integration secret.

## Upload succeeds but data is not visible

- Confirm the dataset was uploaded to the correct dashboard (by ID or title).
- Confirm `X-Data-Type` matches what you expect.
- If you want a dataset to open as a table by default, send `X-Display-Type: grid`.
- Refresh the dashboard page.

## I expected CSV/Excel uploads or a database connection

Smart Dashboard is a **push-based** system.

Push your data to the Upload API in JSON (recommended) or XML (legacy).

## Who can view/rotate the API key?

Only admin roles can access the API Key tab.

---

## Need help?

Contact your support channel or administrator for tenant access and integration help.
