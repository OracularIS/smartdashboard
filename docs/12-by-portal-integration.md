# Integrating Smart Dashboard with BY Portal

This guide walks you through embedding **Smart Dashboard** into your **BY Portal** using the **Page Builder** and **Menu Editor**.

> Notes
>
> - This integration uses a **Public Share Link** from Smart Dashboard.
> - Public links are **read-only**.
> - Public sharing may need to be enabled for your tenant. See: [Sharing & TV Mode](./09-sharing-and-tv-mode.md#public-sharing-read-only)

---

## Step 1: Get the Public Share Link from Smart Dashboard

1. Log in to your Smart Dashboard account.
2. Navigate to the **View Dashboard** screen.

![View Dashboard screen](./images/by-portal-01-view-dashboard.png)

3. Select the warehouse you want the dashboards for, then click **Share**.

![Click Share](./images/by-portal-02-click-share.png)

4. Copy the **Public Share Link** that is generated.

![Copy Public Share Link](./images/by-portal-03-copy-public-share-link.png)

---

## Step 2: Add an External Page in BY Portal

1. Log in to your BY Portal.
2. Go to **Extensions** from the main navigation.

![BY Portal Extensions menu](./images/by-portal-04-extensions-menu.png)

3. Select **Page Builder**.

![Open Page Builder](./images/by-portal-05-page-builder.png)

4. Under **Actions**, click **Add External Page**.

![Add External Page action](./images/by-portal-06-add-external-page.png)

5. Fill in the following fields:

   - **Title:** Enter a descriptive name for the page
   - **Description:** (Optional) Enter a short description
   - **URL:** Paste the Public Share Link copied from Smart Dashboard

![External Page fields](./images/by-portal-07-external-page-fields.png)

6. Save the page.

---

## Step 3: Add the Page to a Menu

1. In the BY Portal, navigate to **Menu Editor**.

![Open Menu Editor](./images/by-portal-09-menu-editor.png)

2. Create a new **Menu Group** (or select an existing one where you want the dashboard to appear).

![Create/select Menu Group](./images/by-portal-10-menu-group.png)

3. Assign the external page you created in Step 2 to that menu group.

![Assign external page to menu group](./images/by-portal-11-assign-external-page.png)

4. From the **Review** section, add the **Roles**.

![Assign roles in Review section](./images/by-portal-12-roles-review.png)

5. Save your changes.

![Save Menu Editor changes](./images/by-portal-13-save-menu.png)

---

## Result

The Smart Dashboard will now appear as a menu item in your BY Portal, accessible to users.

![Smart Dashboard appears in BY Portal menu](./images/by-portal-14-menu-item-result.png)
