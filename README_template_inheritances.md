# JKC Template Inheritance

## Versions
- CSS: bootstrap@5.3.2 (via CDN)
- JS: bootstrap@5.3.2 (via CDN)

## Overview

`src/...jkc/templates/`

- `djangocms_frontend/templates/djangocms_frontend.html` [details](#djangocms_frontend-djangocms_frontendhtml)
	- `djangocms_frontend/templates/bootstrap5/base.html` [details](#djangocms_frontend-bootstrap5basehtml)
		- `djcms_jks/templates/jkc_base.html`
			- `djcms_jks/templates/jkc_fullwidth.html` (Startseite)
		- `djcms_jks/templates/jkc_4_quadrate.html`
	
	
## (djangocms_frontend) djangocms_frontend.html

Location: `/venvs/juliakarrieceramics_venv/lib/python3.11/site-packages/djangocms_frontend/templates/`

Beinhaltet die Haupt-HTML-Struktur mit Platzhalter für 
- Seitentitel (title-Tag), 
- Metadaten, CSS und JS-Injection
- CMS-Toolbar
- Platzhalter "Page Content"

### blocks
#### head
- `meta`
- `canonical_url`
- `fb_meta`
- `title` (Seitentitel)
- `base_css` (leer, in `<head>`)
- `page_head` (leer, in `<head>`)
#### body
- `body_attrs`
- `navbar` (Navigation)
- `content`
	- placeholder "Page Content" (in `<section>`)
- `base_js`
- `end_js`
- `bottom_css`

## (djangocms_frontend) /bootstrap5/base.html

Location: `/venvs/juliakarrieceramics_venv/lib/python3.11/site-packages/djangocms_frontend/templates/bootstrap5/`
Overview:
- CSS and JS files
- Menu

### blocks
Overriding:

- `base_css` (injected `bootstrap.min.css`)
- `base_js` (injected `bootstrap.bundle.min.js`)
- `navbar`
	- `navbar_options`
	- `brand`
	- `menubar`
		- injected `show_menu`
	- `searchbar` (empty)
	
## (djcms_jks) jkc_base.html
- extends bootstrap5/base.html
- extends `bottom_css` (block.super)  with custom background image

## (djcms_jkc) jkc_fullwidth.html
- extends jkc_base.html

### blocks
- `content`
	- placeholder "content"
