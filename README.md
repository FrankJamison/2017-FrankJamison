# 2017 Frank Jamison Resume Site

A static, multi-page HTML/CSS resume website for Frank Jamison (2017). The site is organized into several resume sections (employment, education, skills, awards, and organizations) and uses a shared layout (header + navigation + content + contact sidebar) across pages.

## What’s in this project

### Pages

- **Home / About** — `index.html`
  - Intro/about text and a portrait image.
- **Employment** — `employment.html`
  - Employment history entries with job title/company/date range and bullet highlights.
- **Education** — `education.html`
  - Degree history plus training & certification entries.
- **Skills** — `skills.html`
  - Several grouped skill lists (soft skills, web design, programming, IT, office, etc.).
- **Awards** — `awards.html`
  - Military, scholastic, and employment honors/awards lists.
- **Organizations** — `organizations.html`
  - Professional, scholastic, and military affiliations.

### Shared layout

All pages follow the same overall structure:

- **Header top**: logo + name + subtitle
- **Banner**: background image + page title
- **Navigation**: links to each page/section
- **Main content**: the page’s primary resume section
- **Contact sidebar**: address, phone, email, and social links
- **Footer**: copyright notice

### Styling

- Main stylesheet: `css/myStyles.css`
- Fonts are loaded from Google Fonts:
  - Cantarell
  - Cardo
  - Exo 2

## Folder structure

```text
.
├─ index.html
├─ employment.html
├─ education.html
├─ skills.html
├─ awards.html
├─ organizations.html
├─ css/
│  └─ myStyles.css
└─ images/
   └─ (site images: logo, banner, portrait, etc.)
```

## How to view the site

### Option A: Open the HTML file directly

This is the simplest approach:

1. Open `index.html` in a browser.
2. Use the top navigation to move between sections.

### Option B: Run a small local web server (recommended)

Some browsers apply stricter rules to `file://` pages (especially around asset loading). Running a local server avoids those edge cases.

**Python (Windows):**

```bat
cd /d d:\Websites\2026-FCJamison\portfolio\2017-FrankJamison
py -m http.server 8000
```

Then open:

- `http://127.0.0.1:8000/`

Stop the server with `Ctrl+C`.

## Editing guide

### Updating navigation “current page” styling

Each page’s nav contains the same set of links. The current page is marked by adding the `current` class to its corresponding anchor.

Examples:

- Home page: the Home link includes `current`
- Employment page: the Employment link includes `current`

If you add a new page or duplicate a page as a template, ensure exactly one nav link has the `current` class on that page.

### Updating the contact sidebar

The contact sidebar is repeated on each HTML page. If you change address/phone/email/social links, apply the same edit to:

- `index.html`
- `employment.html`
- `education.html`
- `skills.html`
- `awards.html`
- `organizations.html`

(There is no shared include/templating system in this project—each page is standalone.)

### Images and alt text

Images live in `images/`. When replacing an image, keep filenames consistent if possible to avoid updating multiple pages, and verify:

- The `alt` attribute remains accurate and descriptive.
- Decorative images use `aria-hidden="true"` where appropriate (the banner background image is already treated as decorative).

## Deployment

This is a static site (HTML/CSS/images only), so it can be hosted on any static file host (examples: a standard web server, object storage static hosting, or static site hosting services).

Typical deployment is simply copying the folder contents so that `index.html` is at the web root and `css/` and `images/` are alongside it.

## Notes

- This repository contains personal resume content (including contact information). Review and redact as needed before publishing publicly.
- The content and copyright notice reflect the 2017 version of the resume site.
