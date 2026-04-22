# 8) API Docs Page (Upload Integration)

Smart Dashboard includes an **API Docs** screen inside the app.

It provides ready-to-copy examples and explains which headers to send.

## Screen

![API docs](./images/09-api-docs.png)

## Two upload endpoints

### Recommended: JSON Upload

- **Endpoint:** `/api/upload-data`
- **Format:** JSON (`application/json`)
- Recommended for modern integrations.

### Legacy: XML Upload

- **Endpoint:** `/api/upload-xml`
- **Format:** XML (`application/xml`)
- Kept for backward compatibility (e.g., MOCA).

> Important: Smart Dashboard is a **push-based** system. Any system that can make HTTP requests can push data into dashboards.

## Authentication

Uploads authenticate using a tenant-scoped API key:

```
x-api-key: <your-tenant-api-key>
```

Get or rotate this key from **Data Management → API Key**.

## Supported ingestion formats

- **JSON** (recommended)
- **XML** (legacy)

Smart Dashboard does **not** directly connect to your database and does **not** pull data on a schedule.

## What the API expects (JSON)

The JSON endpoint accepts **application/json**.

The common payload shape is:

- `resultset.row`: array of objects (each object is one row)
- `fieldOrder`: optional array that controls column ordering (recommended)

## Required headers

The Upload APIs use headers to route and isolate your data.

| Header | Required? | Description |
|---|---|---|
| `x-api-key` | Required | Tenant API key |
| `X-Tenant-Id` | Required | Tenant ID (UUID) |
| `X-Data-Type` | Required | Dataset category name (e.g., Sales, Inventory) |
| `X-Dashboard-Id` | Either/Or | Target dashboard by GUID |
| `X-Dashboard-Title` | Either/Or | Create/find dashboard by title |
| `X-Display-Type` | Optional | Hint for initial UI rendering (e.g., grid/chart) |

### X-Display-Type values

`X-Display-Type` lets you set the initial visualization when the dataset first appears in the UI.

Common values:

- `grid` (renders as Table)
- `chart` (default behavior)
- `chart-line`
- `chart-bar`
- `chart-area`
- `chart-pie`

## Example (cURL, JSON)

```bash
curl -X POST "https://<your-app-domain>/api/upload-data" \
  -H "Content-Type: application/json" \
  -H "x-api-key: <apikey>" \
  -H "X-Data-Type: Sales" \
  -H "X-Tenant-Id: <tenant-uuid>" \
  -H "X-Dashboard-Id: <dashboard-uuid>" \
  --data-raw '{"resultset": {"row": [{"Month": "March", "Sales": 18500}]}, "fieldOrder": ["Month", "Sales"]}'
```

### Multi-series example (enables stacked/clustered options)

If you send more than one metric column, Smart Dashboard treats them as multiple series:

```json
{
  "resultset": {
    "row": [
      {"Month": "March", "Sales": 18500, "Returns": 900},
      {"Month": "April", "Sales": 15000, "Returns": 700}
    ]
  },
  "fieldOrder": ["Month", "Sales", "Returns"]
}
```

## Response

Successful uploads return a JSON response with `success: true` and processing details.

> The legacy XML endpoint returns a flat JSON response for compatibility.
