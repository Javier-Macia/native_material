# Native Material

A standalone Drupal module that serves **Google Material Symbols Outlined** and the classic **Material Icons** family 100% locally from your own web server with zero external dependencies.

## Features

- **100% Self-Hosted:** No requests made to `fonts.googleapis.com` or `fonts.gstatic.com`. Fully compliant with GDPR / European privacy regulations.
- **Zero FOUT (Flash of Unstyled Text):** Configured with `font-display: block` so ligature names (`settings`, `home`, `calendar_month`) never flash as plain text while fonts load.
- **Native Resource Preloading:** Automatically preloads `MaterialSymbolsOutlined.woff2` via `<link rel="preload">` in the HTML `<head>`, achieving optimal Core Web Vitals and instant rendering.
- **Modular Libraries:**
  - `native_material/symbols`: Material Symbols Outlined variable font.
  - `native_material/icons`: Classic Material Icons (Regular, Outlined, Round, Sharp, Two-Tone).
  - `native_material/all`: Complete bundle.

## Requirements

- Drupal 10, 11 or 12.

## Installation

Using Composer:

```bash
composer require javierms/native_material
drush en native_material -y
```

## Usage

In your custom theme or module `*.libraries.yml`:

```yaml
my_library:
  dependencies:
    - native_material/symbols
```

In your Twig templates or HTML:

```html
<!-- Material Symbols Outlined -->
<span class="material-symbols-outlined">settings</span>

<!-- Material Icons -->
<span class="material-icons">home</span>
```

## License

- Module code: GNU General Public License v2.0 or later (GPL-2.0-or-later).
- Font assets: Apache License 2.0 (Google LLC).
