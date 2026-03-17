# Devashish Gaikwad - Personal Website

This repository contains a multilingual Jekyll portfolio site with:

- English and German navigation/pages (`/en/` and `/de/`)
- Blog posts under `/blog/`
- Project pages and homepage project tiles
- Experience pages and homepage experience tiles

It is structured so content editors can update markdown files without touching generated HTML.

## Getting Started

1. Install dependencies:
	- `bundle install`
2. Start local server:
	- `bundle exec jekyll serve`
3. Build static output:
	- `bundle exec jekyll build`

Output is generated into `_site/`.
Do not edit `_site/` manually, it will be overwritten on build.

## Site Structure

### Content Sources

- `_posts/`: blog posts (single set, language as authored)
- `_projects/`: project entries (single source for EN/DE)
- `_experiences/`: experience entries (single source for EN/DE)

### Language Pages

- `_pages/en/`: English pages
  - `/en/`
  - `/en/projects/`
  - `/en/experiences/`
  - `/en/archive/`
- `_pages/de/`: German pages
  - `/de/`
  - `/de/projects/`
  - `/de/experiences/`
  - `/de/archive/`

### Shared Templates

- `_includes/navigation.html`: top nav + language switch
- `_includes/project-tiles.html`: homepage project tile grid
- `_includes/experience-tiles.html`: homepage experience tile grid
- `_includes/project-rows.html`: detailed project list layout (used on projects pages)
- `_includes/experience-timeline.html`: chronological detailed experience layout

### Styling

- `assets/css/main.scss`: Sass entry point (must keep valid front matter)
- `assets/css/_sass/projects.scss`: project/tile styles
- `assets/css/_sass/experiences.scss`: experience styles
- `assets/css/_sass/footer.scss`: nav and language-switch styles
- `assets/css/_sass/style.scss`: global typography/layout styles

## Common Tasks

### Add a Blog Post

1. Create a new file in `_posts/` using `YYYY-MM-DD-title.md`
2. Add front matter and markdown content

### Add a Project

1. Create one file in `_projects/`
2. Recommended front matter fields:
	- `title`
	- `description`
	- `main_page_display_description`
3. Optional German fields:
	- `description_de`
	- `main_page_display_description_de`
4. Optional tile images:
	- `tile_image`
	- `tile_image_de`

You usually add each project only once.

### Add an Experience

1. Create one file in `_experiences/`
2. Recommended front matter fields:
	- `title`
	- `organization`
	- `type`
	- `location`
	- `start_date`
	- `end_date` (optional for current role)
	- `summary`
3. Optional German fields:
	- `title_de`
	- `organization_de`
	- `type_de`
	- `location_de`
	- `summary_de`
4. Optional tile images:
	- `tile_image`
	- `tile_image_de`

Experiences are shown chronologically on the detailed experience pages.

### Update Homepage Sections

- English homepage content: `_pages/en/index.md`
- German homepage content: `_pages/de/index.md`
- Homepage tile behavior:
  - Projects: `_includes/project-tiles.html`
  - Experiences: `_includes/experience-tiles.html`

### Update Detailed List Pages

- Projects detail layout: `_includes/project-rows.html`
- Experiences detail layout: `_includes/experience-timeline.html`

## Multilingual and Routing Behavior

- Root (`/`) detects browser language on first visit and redirects to `/en/` or `/de/`
- User preference is saved in `localStorage` as `preferredLang`
- Language switch updates this saved preference
- Blog posts remain under `/blog/` and are not duplicated by language

## Front Matter Reference

### Page-level

- `lang: en` or `lang: de`
- `permalink: /path/`
- `published: true`

### Project fields (common)

- `title`, `description`
- `main_page_display_description`
- `tile_image`
- Optional DE variants: `description_de`, `main_page_display_description_de`, `tile_image_de`

### Experience fields (common)

- `title`, `organization`, `type`, `location`
- `start_date`, `end_date`
- `summary`, plus markdown body content
- Optional DE variants: `*_de`

## Pre-Commit Checklist

1. Run `bundle exec jekyll build`
2. Verify these pages:
	- `/en/`, `/de/`
	- `/en/projects/`, `/de/projects/`
	- `/en/experiences/`, `/de/experiences/`
	- `/blog/`
3. Confirm styles are compiled to `_site/assets/css/main.css`
4. Commit source files only (not `_site/`)

## Troubleshooting

### Site looks like plain HTML (no styling)

Check `assets/css/main.scss` first.
It must begin with valid front matter:

```scss
---
# comment (optional)
---
```

If that front matter is broken, Sass will not compile and the site will appear unstyled.

### Changes disappear after rebuild

You likely edited files in `_site/`.
Always edit source files under `_pages/`, `_projects/`, `_experiences/`, `_posts/`, `_includes/`, or `assets/css/_sass/`.

