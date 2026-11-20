# P9 - Responsive navbar and card grid using Flexbox

**Aim:** mobile-first navbar and card grid with Flexbox.

- Navbar: `display:flex; justify-content:space-between; align-items:center`. Below 48em the menu is hidden behind a CSS-only hamburger (hidden checkbox + `:checked ~ .navbar__menu`). From 48em it becomes one row.
- Cards: `.cards{display:flex;flex-wrap:wrap;gap}` and `.card{flex:1 1 18rem}` - cards wrap by themselves with no column media queries.
- Card footer uses `margin-top:auto` so buttons align at the bottom.

**Run:** open `index.html` and resize the window.

## Output
Desktop:

![desktop](output-desktop.png)

Mobile:

![mobile](output-mobile.png)

Mobile, menu open:

![menu](output-mobile-menu-open.png)
