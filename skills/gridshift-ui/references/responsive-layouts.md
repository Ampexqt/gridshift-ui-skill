# Responsive Layouts

## Desktop

- Use the available width for a deliberate multi-column workspace.
- Keep a clear visual focal point and align module edges.
- Avoid excessive empty space and oversized headings.
- Keep primary metrics and node status visible without requiring unnecessary scrolling.
- Constrain terminal/log height and allow its content to scroll independently when needed.

## Tablet

- Reduce the number of columns as space narrows.
- Preserve the order of importance rather than shrinking every module equally.
- Move secondary modules below the node controls and personal metrics.
- Ensure chart labels and table columns remain readable.

## Mobile

Recommended order:
1. Header and primary navigation.
2. Node status and essential action.
3. Personal points/contribution summary.
4. Key network metrics.
5. Contribution history.
6. Leaderboard and terminal logs.
7. Secondary features.

Implementation guidance:
- Prevent page-level horizontal overflow.
- Make controls comfortably tappable.
- Keep technical labels from colliding with values.
- Allow long identifiers to wrap or truncate with a way to inspect the full value.
- Use a scrollable table region or a compact alternative if the table cannot fit.
- Collapse secondary content when that improves scanning.
- Avoid forcing desktop-sized charts into narrow viewports.

## Validation

Test at representative narrow mobile, wide mobile, tablet, laptop, and desktop widths. Check actual content—not only empty placeholder cards. Verify menus, tables, terminal logs, chart tooltips, and long numeric values.
