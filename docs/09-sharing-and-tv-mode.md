# 9) Sharing & TV Mode

Smart Dashboard supports sharing dashboards via a public link and viewing charts in TV mode.

## Public sharing (read-only)

If your tenant enables sharing, you may generate a share link that looks like:

```
/shared/<token>
```

Behavior:

- Anyone with the link can view the dashboard **without signing in**.
- Public links are **read-only** (no edits).
- Links may have an expiry date/time.

## TV Mode

TV mode is optimized for wall displays.

## Screenshot

![TV mode](./images/10-tv-mode.png)

Two variants exist:

1. **Authenticated TV mode** (inside tenant, requires login)
2. **Public TV mode** (under a share token)

Public TV mode route:

```
/shared/<token>/tv-mode
```

## Best practices

- Use a dedicated display account or share link with controlled distribution.
- If you rotate datasets frequently, set up automated uploads.
