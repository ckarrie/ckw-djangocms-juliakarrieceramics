# JKC Template Inheritance

## Versions
- CSS: bootstrap@5.3.2 (via CDN)
- JS: bootstrap@5.3.2 (via CDN)

## jkc_base.html

`src/...jkc/templates/`

- djangocms_frontend/templates/djangocms_frontend.html
	- 
	
	
## (djangocms_frontend) djangocms_frontend.html

Location: `/venvs/juliakarrieceramics_venv/lib/python3.11/site-packages/djangocms_frontend/templates/`

Beinhaltet die Haupt-HTML-Struktur mit Platzhalter für 
- Seitentitel (title-Tag), 
- Metadaten, CSS und JS-Injection

### Blocks
#### head
- meta
- canonical_url
- fb_meta
- title (Seitentitel)
- base_css
- page_head (Zusätzlicher header-Block)
#### body
- body_attrs
- navbar
- content
	- placeholder "Page Content"
- base_js
- end_js
- bottom_css

## (djangocms_frontend) /bootstrap5/base.html

Location: `/venvs/juliakarrieceramics_venv/lib/python3.11/site-packages/djangocms_frontend/templates/bootstrap5/`



### blocks
Overriding:
- base_css
- base_js
- navbar
