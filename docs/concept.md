# Smart Dashboard Concepts

This section explains the key concepts used when connecting to Smart Dashboard APIs and posting data through the **Smart MOCA Client**. Understanding these concepts ensures your data is uploaded correctly and dashboards stay up to date.

---
 
## 1. HTTP POST Method

The **POST method** is used to send data to a server. In Smart Dashboard, it is primarily used to upload data to dashboards via the Smart MOCA Client.

Key points about POST:

- Sends data in the **request body** rather than the URL.  
- Used to **create or update resources** on the server.  
- Requires proper **headers** for authentication and identification.  
- The server responds with a **status code** indicating success or failure.

---

## 2. Request Components

When sending data via POST, a request typically includes:

### a. URL (Endpoint)
The API endpoint where the data will be sent.  
Example:  

```
https://dashboards.smart-is.com/api/upload-xml
```

### b. Headers
Headers provide metadata about the request. Common headers include:

| Header / Field Name   | Description |
|-----------------------|-------------|
| **x-api-key**         | Your API Key used for authentication. |
| **X-Data-Type**       | The header representing the type of data for your visual (e.g., Trailers, Shipments, Inventory). |
| **X-Tenant-Id**       | The Tenant ID assigned to your organization. |
| **X-Dashboard-Id**    | The Dashboard ID of the dashboard you created to upload data into. |

### c. Body
The body contains the actual data you are sending. This can be:

- XML (commonly used for dashboards)  

In Smart MOCA Client, the body is usually stored in a variable (e.g., `@x`) before sending.

---

## 3. Example: Smart MOCA Client POST Request

```moca
 {
    do http request
    where url = 'https://dashboards.smart-is.com/api/upload-xml'
    and method = 'post'
    and header = '<API-KEY>&X-Data-Type:<DATA TYPE>X-Tenant-Id:<TENANT ID>&X-Dashboard-Id:<DASHBOARD ID>'
    and body = @x 
    }
 ```   



