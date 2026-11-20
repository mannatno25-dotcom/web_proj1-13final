# Programming for Web Development - I: Laboratory

Replace "Mannat Agarwala", `mannatno25@gmail.com` and `mannatno25-dotcom` with your own details before submitting.

| # | Practical | Folder |
|---|---|---|
| P1 | Project folder and terminal navigation | [P1-terminal-navigation](P1-terminal-navigation/README.md) |
| P2 | Portfolio repo with an initial commit | [P2-initial-commit](P2-initial-commit/README.md) |
| P3 | Feature-branch Git workflow | [P3-feature-branch](P3-feature-branch/README.md) |
| P4 | GitHub README and version tags | [P4-readme-and-tags](P4-readme-and-tags/README.md) |
| P5 | Semantic bio page | [P5-semantic-bio](P5-semantic-bio/README.md) |
| P6 | Full portfolio structure (semantic HTML) | [P6-portfolio-structure](P6-portfolio-structure/README.md) |
| P7 | Design tokens and typography | [P7-design-tokens](P7-design-tokens/README.md) |
| P8 | Sticky navbar and card overlay | [P8-sticky-navbar-overlay](P8-sticky-navbar-overlay/README.md) |
| P9 | Responsive navbar and card grid (Flexbox) | [P9-flexbox-navbar-cards](P9-flexbox-navbar-cards/README.md) |
| P10 | Header and footer (advanced Flexbox) | [P10-flexbox-header-footer](P10-flexbox-header-footer/README.md) |
| P11 | Newspaper three-column layout (Grid) | [P11-grid-newspaper](P11-grid-newspaper/README.md) |
| P12 | Projects grid (advanced Grid) | [P12-grid-projects](P12-grid-projects/README.md) |
| P13 | Flexbox vs Grid for a shared layout | [P13-flexbox-vs-grid](P13-flexbox-vs-grid/README.md) |

## How to run
- **P1-P4 (Git):** each folder has a README containing the real terminal output. The repository from P2-P4 is `portfolio/` (run `git log --oneline --graph --decorate --all` and `git tag` inside it).
- **P5-P13 (web):** open the folder's `index.html` in any modern browser. No build step, no dependencies. Each folder has `output*.png` screenshots.
- To publish the Git repo: create an empty repo on GitHub, then `git remote add origin <url>`, `git push -u origin main`, `git push origin --tags`.

## Notes
- Git identity in the repo is a placeholder; set yours with `git config user.name` / `user.email` for new commits.
- Screenshots were captured with headless Chrome. CSS uses modern features (`:has()`, `clamp()`, `inset`) supported by current Chrome, Edge, Firefox and Safari.
