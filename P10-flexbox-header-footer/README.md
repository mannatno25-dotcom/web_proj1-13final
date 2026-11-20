# P10 - Portfolio header and footer with advanced Flexbox

**Aim:** a professional header and footer using advanced Flexbox features.

- Header: logo left, nav centred (`flex:1`), search + button right (`justify-content:space-between`, `align-items:center`).
- Mobile: `flex-wrap` + `order` move the actions beside the logo and the nav onto its own row - without changing the HTML.
- Footer: columns with `flex: 2 1 18rem` (brand) and `flex: 1 1 9rem` (links); bottom bar uses `space-between`.
- Sticky footer: `body{display:flex;flex-direction:column;min-height:100vh}` and `main{flex:1}`.

**Run:** open `index.html`, resize.

## Output
Desktop:

![desktop](output-desktop.png)

Mobile:

![mobile](output-mobile.png)
