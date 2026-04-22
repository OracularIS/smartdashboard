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

## Upload fails with Unauthorized (401)

Your API key may be missing or invalid.

- Confirm you are sending `x-api-key`.
- If the key was rotated, update your integration secret.

## Upload succeeds but data is not visible

- Confirm the dataset was uploaded to the correct dashboard (by ID or title).
- Confirm `X-Data-Type` matches what you expect.
- Refresh the dashboard page.

## Who can view/rotate the API key?

Only admin roles can access the API Key tab.

---

## Need help?

Contact your support channel or administrator for tenant access and integration help.
