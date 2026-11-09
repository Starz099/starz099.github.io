# Mayank — Personal Portfolio Website

A fast, static portfolio and personal blog built with [Hugo](https://gohugo.io/), heavily inspired by the minimal, painterly aesthetic of [Aras Pranckevičius's website](https://aras-p.info/).

Designed for zero-dependency static hosting on [GitHub Pages](https://pages.github.com/) at [starz099.github.io](https://starz099.github.io/).

---

## ✨ Features & Design

- **Aras-Inspired Aesthetic**:
  - **Painterly Blue Header Banner**: Deep sky blue (`#16a0d4`) top bar with a torn brush bottom edge (`brush-mask-hor.png`), button nav items, and RSS subscribe link.
  - **Warm Yellow Sidebar Rail**: Translucent yellow column (`rgba(254, 186, 72, 0.75)`) with a torn brush left margin (`brush-mask-ver.png`), recent posts, categories, and elsewhere social links.
  - **Aras Overview Bio Table**: Clean square avatar and bulleted icon lines (Blog, Codeforces, Projects, X, CV, Contact).
  - **Aras-style Blue Blockquotes**: Sky-blue tinted callouts with left accent border.
- **Projects Showcase**: 11 desktop, systems (Rust/Tauri), and web applications categorized into *Systems & Desktop Tools* and *Web Platforms & Applications*.
- **Technical Writing / Blog**: Built-in essays with syntax highlighting, diagram illustrations, reading time, and tags.
- **Dedicated Pages**:
  - `/` — Aras bio overview, featured projects, recent essays, and GitHub activity chart.
  - `/projects/` — Full project catalogue with code, demo, and writeup links.
  - `/blog/` — Technical essays and articles.
  - `/work/` — Systems engineering and work experience.
  - `/resume/` — Curriculum Vitae with role, core focus, and contact links.
  - `/contact/` — Direct email and social contact links.
  - `/tags/` — Tag taxonomy cloud.
- **Blazing Fast**: Builds in under 50ms with zero client-side JavaScript required for navigation.
- **RSS & LLM Friendly**: Complete Atom/RSS feed at `/index.xml`, plus `/llm.txt` for AI crawlers.

---

## 🛠️ Local Development

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (v0.120+ or latest extended edition, tested on v0.168.0 extended).

### Commands

```bash
# Clone the repository
git clone git@github.com:Starz099/starz099.github.io.git
cd starz099.github.io

# Start local dev server with live reload
hugo server -D

# Build production static files into public/
hugo --minify
```

Open `http://localhost:1313/` in your browser.

---

## 🚀 Free Deployment on GitHub Pages

This repository is preconfigured for automatic, free static deployment to GitHub Pages via GitHub Actions:

1. Push this repository to GitHub as `Starz099/starz099.github.io`:
   ```bash
   git remote add origin git@github.com:Starz099/starz099.github.io.git
   git push -u origin main
   ```
2. In your GitHub repository:
   - Go to **Settings** → **Pages**.
   - Under **Build and deployment** → **Source**, select **GitHub Actions**.
3. Every push to the `main` branch automatically triggers `.github/workflows/deploy.yml`, builds Hugo with `--minify`, and deploys to `https://starz099.github.io/`!

*(If you attach a custom domain like `starzz.dev`, update `baseURL` in `hugo.yaml` and add your custom domain in GitHub Pages settings).*

---

## 📁 Repository Structure

```text
├── .github/workflows/deploy.yml # GitHub Actions workflow for Pages deployment
├── archetypes/                  # Hugo post archetypes
├── content/                     # Markdown content
│   ├── _index.md                # Home page
│   ├── blog/                    # Essays & articles
│   ├── contact.md               # Contact info
│   ├── projects/                # Projects page
│   ├── resume.md                # Curriculum Vitae
│   └── work.md                  # Work & experience
├── data/
│   ├── home.yaml                # Bio lines on the home page
│   └── projects.yaml            # Project catalogue metadata
├── layouts/                     # HTML templates & partials
│   ├── _default/                # Base, list, single, resume, contact
│   ├── blog/                    # Blog list & single
│   ├── partials/                # Header, sidebar, footer, head, icon, etc.
│   └── index.html               # Home page template
├── static/                      # Static assets
│   ├── css/main.css             # Main stylesheet (Aras aesthetic)
│   ├── images/                  # Avatars, brush masks, project & blog images
│   ├── favicon.ico
│   ├── llm.txt
│   └── robots.txt
└── hugo.yaml                    # Hugo configuration
```

---

## 📄 License

- Text content and essays &copy; Mayank ([@Starz099](https://github.com/Starz099)).
- Code snippets and theme styling are open source under the MIT License.
