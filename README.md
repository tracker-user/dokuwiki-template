# DokuWiki Fork Template

A fork of DokuWiki's default template, extracted from the [official repository](https://github.com/dokuwiki/dokuwiki/tree/master/lib/tpl/dokuwiki) using `git-filter-repo --subdirectory-filter` to isolate the template directory with full commit history.

Original template designed by Clarence Lee, maintained by Anika Henke.

## Features

- Optional sidebar
- Responsive layout (desktop, tablet, phone)
- HTML5
- Include hooks for adding content without modifying template files
- Action hooks for plugin integration via `TEMPLATE_PAGETOOLS_DISPLAY`

## Customization

### Width and Colors

Override style variables in `conf/tpl/dokufork/style.ini`:

```ini
[replacements]
__site_width__  = "100%"
```

Available variables: `__background_site__`, `__link__`, `__existing__`, `__missing__`, `__site_width__`, `__sidebar_width__`.

### Logo

Upload replacements via the Media Manager to override defaults:

- Logo: `:wiki:logo.png` or `:logo.png` (also `.svg`)
- Favicon: `:wiki:favicon.ico` or `:favicon.ico`
- Touch icon: `:wiki:apple-touch-icon.png` or `:apple-touch-icon.png`

### Include Hooks

Add HTML/PHP files to the template directory or `conf/` directory:

| File                 | Position                                           |
|----------------------|----------------------------------------------------|
| `meta.html`          | Inside `<head>` (styles, meta headers)             |
| `header.html`        | Top of page, above logo                            |
| `sidebarheader.html` | Top of sidebar                                     |
| `sidebarfooter.html` | Bottom of sidebar                                  |
| `pageheader.html`    | Top of content box, above content                  |
| `pagefooter.html`    | Bottom of content box, below content               |
| `footer.html`        | End of page, after all content                     |

## Fork Changes

No code changes from the upstream template. This fork adds:

- `LICENSE` (GPL-2.0)
- `.gitignore`
- Updated `template.info.txt` (renamed base to `dokufork`)

## License

GPL-2.0 &mdash; same as DokuWiki.
