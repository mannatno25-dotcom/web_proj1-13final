# P13 - Choosing between Flexbox and Grid for a shared layout

**Aim:** build one page that uses both systems, each where it fits best, and justify the choice.

| Part of the page | Tool | Reason |
|---|---|---|
| Page shell (header/sidebar/main/footer) | **Grid** | Rows and columns together, named areas, one rule re-arranges it on mobile |
| Header, nav, button group, chips, footer | **Flexbox** | Single row; content decides size |
| Sidebar nav | **Flexbox** | One axis - column on desktop, row on mobile (same code, different `flex-direction`) |
| Stats and project gallery | **Grid** | Equal tracks that wrap with `auto-fit` |
| Inside each card | **Flexbox** | Column; `margin-top:auto` aligns footers across cards |
| Decision guide | **Grid** | Two equal columns |

**Rule of thumb:** Grid for the outside (page, sections), Flexbox for the inside (components). Nesting them is normal.

**Extra:** the "Show layout labels" checkbox uses `:has(#labels:checked)` and absolutely positioned pseudo-elements to outline and label every flex (orange) and grid (purple) container. Untick it to hide them.

## Output
Desktop (labels on):

![desktop](output-desktop.png)

Mobile:

![mobile](output-mobile.png)
