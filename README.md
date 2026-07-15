# My Personal Website

Personal research portfolio and academic CV, built as a static [Jekyll](https://jekyllrb.com/) site and hosted on GitHub Pages.

**Live site:** [vadim-atl.github.io](https://vadim-atl.github.io)

## Overview

Single-page portfolio covering publications, projects, and academic background in generative AI, vision-language models, and their applications to medical imaging and structural health monitoring.

- Profile header with bio and research interests
- Publications & preprints
- Selected projects

## Tech stack

- **Jekyll** static site generator, `kramdown` markdown renderer, no theme (`theme: null` in `_config.yml`) — layout and styling are hand-rolled
- Content lives almost entirely in `index.md`: inline `<style>` block plus raw HTML for structured content (cards, tags, contact links), since Jekyll/kramdown alone can't express the card layouts
- Small vanilla-JS snippet at the bottom of `index.md` makes each publication card clickable (opens its primary link — DOI, code repo, or dataset — while still letting internal links like "Code" / "Paper" work independently)

## Structure

```
.
├── _config.yml       # site title, description, url, markdown engine
├── _layouts/         # Jekyll layout(s) used by index.md
├── assets/           # profile photo, paper preview images
├── index.md          # the entire site: styles + content
└── .gitignore
```

## Deployment

GitHub Pages builds automatically from the `main` branch on push — no CI config needed.

## Contact

- [LinkedIn](https://www.linkedin.com/in/vadim-atlassov)
- [GitHub](https://github.com/Vadim-ATL)
- [Google Scholar](https://scholar.google.com/citations?hl=ko&user=1IG1kf0AAAAJ)
- vadim.atlassov@nu.edu.kz