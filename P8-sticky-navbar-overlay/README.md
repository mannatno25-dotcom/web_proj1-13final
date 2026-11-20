# P8 - Sticky navbar and card overlay using CSS positioning

**Aim:** use `position` values to build a navbar that stays on screen and cards with overlays.

| Value | Where used |
|---|---|
| `sticky` + `top:0` | `.navbar` stays pinned while scrolling |
| `relative` | `.card` - anchor for absolute children |
| `absolute` | `.card__badge` (corner) and `.card__overlay` (`inset:0`) |
| `fixed` | `.to-top` button |

Also: `z-index` tokens for stacking, `scroll-margin-top` so anchors are not hidden under the sticky bar, and `:focus-within` so keyboard users see the overlay.

**Run:** open `index.html`, scroll, then hover a card.
(Sticky behaviour needs live scrolling, so it cannot be shown in a still image.)

## Output
Top of page:

![P8 top](output-top.png)

Card hovered (overlay shown):

![P8 overlay](output-card-overlay.png)
