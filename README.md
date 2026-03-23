# sisy.world

The main SISY platform landing page. Built with [Hugo](https://gohugo.io/) — no theme, layouts only.

**Live site:** [https://sisy.world](https://sisy.world)
**Notion:** https://www.notion.so/32b81018ea0381a6a304c2d80ed423dc

## About

SISY is visibility infrastructure for women experts. sisy.world is the primary landing page connecting experts and organizers to the full SISY ecosystem.

## SISY Ecosystem

| Site | Purpose |
|------|---------|
| [sisy.world](https://sisy.world) | Main platform landing page (this repo) |
| [sisy.social](https://sisy.social) | Community hub & framework docs |
| [sisy.my](https://sisy.my) | Expert profiles |
| [sisy.video](https://sisy.video) | Speaker reels |
| [sisy.courses](https://sisy.courses) | Expert learning |
| [sisy.today](https://sisy.today) | Live opportunities feed |
| [sisy.team](https://sisy.team) | Organizer tools |

## Development

```bash
# Install Hugo extended (v0.142+)
brew install hugo

# Serve locally
hugo server -D

# Build for production
hugo --gc --minify
```

## Structure

```
sisy.world/
├── hugo.toml                    # Site configuration
├── content/
│   └── _index.md                # Home page front matter
├── layouts/
│   ├── _default/
│   │   └── baseof.html          # Base shell (nav + footer)
│   └── index.html               # Landing page sections
├── static/
│   ├── css/
│   │   └── style.css            # Single-file CSS, CSS custom properties
│   └── CNAME                    # Custom domain
└── .github/
    └── workflows/
        └── deploy.yml           # Hugo extended → GitHub Pages
```

## Design System

Matches sisy.social's visual language exactly:
- **Fonts:** Inter (body) + Playfair Display (display/headings) via Google Fonts
- **Icons:** Lucide via CDN (`unpkg.com/lucide@latest`)
- **Colors:** `--clr-accent: #b44d8c` (light) / `#d4699e` (dark)
- **BG:** `#fdf6f9` (light) / `#1a1020` (dark)
- **Dark mode:** `data-theme="dark"` on `<html>`, persisted in `localStorage`
- **Radius:** `--radius: 12px`

## Deployment

Deployed via GitHub Actions to GitHub Pages on every push to `main`. See `.github/workflows/deploy.yml`.

To set up: enable GitHub Pages in repo settings → source: GitHub Actions.

---

Built with care by [@mzzavaa](https://github.com/mzzavaa) · Part of the [SISY](https://sisy.world) project
