# Dashboards

The Dashboards page displays datasets (data files) as **charts** or a **grid (table)**.

## Screen

![Dashboards page](./images/04-dashboards.png)

## Select a dashboard

At the top, use the dashboard dropdown to select which dashboard to view.

If you have no dashboards yet, create one in **Data Management → Dashboard**.

## What you can do on this page

### Refresh

Use **Refresh** to reload the latest data that has already been uploaded for the selected dashboard.

> Smart Dashboard is a **push-based** system: data updates happen when your integration uploads new data.

### Edit / Reorder charts

Use **Edit** to enable drag-and-drop reordering of charts.

### Toggle chart vs grid

Some datasets can be viewed as either:

- **Chart** (line/bar/area/pie)
- **Grid/Table** (tabular view)

Notes:

- If a dataset’s saved chart type is **Table**, it always renders as a grid.
- Otherwise, you can temporarily switch between **Chart** and **Table** for readability.

### Change chart type

You can select a chart type per dataset. The selected chart type is stored per dataset.

Available types:

- Line
- Area
- Bar
- Pie
- Table

#### Stacked vs clustered bar charts

If your dataset has **multiple metric columns** (multi-series), the Bar option expands to:

- **Bar (Stacked)**
- **Bar (Clustered)**

> Tip: When you upload multi-series data, use multiple numeric columns after the first “category/X-axis” column.

## Empty dashboard

If there is no data yet, the page shows “No Data Available”. Upload datasets via integration or manually using Data Management.
