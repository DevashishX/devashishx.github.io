# Devashish's Personal Profile

This repository is a Jekyll site with manual multilingual pages (English and German) for non-post content.

## Quick Start

1. Install dependencies:
	- `bundle install`
2. Run locally:
	- `bundle exec jekyll serve`
3. Build static output:
	- `bundle exec jekyll build`

Generated output goes to `_site/`. Do not edit files there.

## Project Structure

- `_posts/`: blog posts (single set, language as written)
- `_projects/`: project source files (single set, reused in EN/DE pages)
- `_pages/en/`: English pages (`/en/`, `/en/projects/`, `/en/archive/`)
- `_pages/de/`: German pages (`/de/`, `/de/projects/`, `/de/archive/`)
- `_includes/navigation.html`: shared top navigation and language switch
- `_includes/project-rows.html`: shared project list layout used by EN/DE pages
- `index.md`: root landing page with browser language detection and redirect
- `_pages/projects.md` and `archive.html`: legacy routes that redirect to EN paths

## What To Edit For Common Tasks

### Add a new blog post

1. Create a file in `_posts/` using `YYYY-MM-DD-title.md`
2. Add front matter and content

You only create one post file.

### Add a new project

1. Create one file in `_projects/`
2. Add front matter fields like:
	- `title`
	- `description`
	- `main_page_display_description`
3. Optional German list text in the same file:
	- `main_page_display_description_de`
	- `description_de`

You usually do not add projects twice.

### Update homepage content

- English text: `_pages/en/index.md`
- German text: `_pages/de/index.md`
- Shared project section layout: `_includes/project-rows.html`

Text changes are typically done in both language files.
Shared UI changes are usually done once in includes/styles.

### Update projects page layout

- Shared layout logic: `_includes/project-rows.html`
- Styles: `assets/css/_sass/projects.scss`

### Update navigation or language switch

- Edit `_includes/navigation.html`
- Style in `assets/css/_sass/footer.scss`

## Multilingual Behavior

- Root (`/`) detects browser language on first visit and redirects to `/en/` or `/de/`
- Preference is saved in `localStorage` as `preferredLang`
- Language switcher updates this saved preference
- Blog/posts remain at `/blog/...` and are not split into EN/DE trees

## Front Matter Tips

Use these fields where relevant:

- `lang: en` or `lang: de` for language-specific pages
- `permalink:` for explicit routes
- For projects:
  - `main_page_display_description`
  - `main_page_display_description_de` (optional)

## Maintenance Checklist Before Commit

1. Run `bundle exec jekyll build`
2. Verify key pages render:
	- `/en/`, `/de/`
	- `/en/projects/`, `/de/projects/`
	- `/blog/`
3. Confirm no manual edits were made in `_site/`
4. Commit source changes only

## Important Rule

If a change disappears after rebuild, it was probably made in `_site/` instead of source files.

