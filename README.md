# PaperCSS Hugo Theme (maintained fork)

This repository is a maintained fork of the original **papercss-hugo-theme** created by **zwbetz-gh**.

The upstream project is archived and no longer actively maintained. I’m maintaining this fork to keep the theme usable
with recent Hugo versions and to continue making incremental improvements while preserving the spirit and simplicity of
the original theme.

## Table of contents

- [Demo](#demo)
- [Minimum Hugo version](#minimum-hugo-version)
- [Installation](#installation)
- [Updating](#updating)
- [Run example site](#run-example-site)
- [Configuration](#configuration)
- [Favicons](#favicons)
- [Logo](#logo)
- [Internationalization (i18n)](#internationalization-i18n)
- [Shortcodes](#shortcodes)
- [Disable toc for a blog post](#disable-toc-for-a-blog-post)
- [Disable summary for a blog post](#disable-summary-for-a-blog-post)
- [Getting help](#getting-help)
- [Credits](#credits)
- [License](#license)

## Demo

https://papercss-hugo-theme.netlify.com/

## Minimum Hugo version

Hugo **Extended** is recommended.

## Installation

From the root of your site:

```bash
git submodule add https://github.com/behaska/papercss-hugo-theme.git themes/papercss-hugo-theme
git submodule update --init --recursive
````

Then set the theme in your Hugo config:

```toml
theme = "papercss-hugo-theme"
```

## Updating

From the root of your site:

```bash
git submodule update --remote --merge themes/papercss-hugo-theme
git add themes/papercss-hugo-theme
git commit -m "chore: bump papercss-hugo-theme"
```

## Run example site

From the root of `themes/papercss-hugo-theme/exampleSite`:

```bash
hugo server --themesDir ../..
```

## Configuration

Copy `config.yaml` from the `exampleSite`, then edit as desired.

## Favicons

## Favicons

This theme includes a favicon block in the HTML `<head>` (PNG favicons, Apple touch icon, manifest, Safari pinned tab).

### Quick setup

1) Generate a favicon package (e.g. via RealFaviconGenerator).
2) Copy the generated files into your Hugo site `static/` folder (site root), for example:

- `static/favicon-16x16.png`
- `static/favicon-32x32.png`
- `static/apple-touch-icon.png`
- `static/site.webmanifest`
- `static/safari-pinned-tab.svg`

That’s it: Hugo will publish them at the site root and the theme will reference them automatically.

## Logo

This theme supports an optional logo in the top navigation bar.

### 1) Put the logo file in your site

Place your logo in your Hugo site `static/` directory, for example:

- `static/img/logo.png`  → available as `/img/logo.png`
- `static/img/logo.svg`  → available as `/img/logo.svg`

> Tip: SVG is ideal for crisp rendering.

### 2) Configure the logo in `config.yaml`

Add these params:

```yaml
params:
  navLogo: /img/logo.png
  navLogoAlt: HerDev Blog
  navLogoHeight: 28
```

- `navLogo`: path to your logo (absolute site path recommended)
- `navLogoAlt`: accessible alt text (defaults to site title if omitted)
- `navLogoHeight`: recommended height in pixels (keeps nav compact)

### 3) Styling

The theme renders the logo next to the site title in the nav.
If you want it smaller/bigger, adjust navLogoHeight and/or override CSS in your custom.css.

## Internationalization (i18n)

This theme supports Hugo multilingual sites.

### Enable multiple languages

In your site config, define `defaultContentLanguage` and a `languages` block.

Minimal example:

```yaml
defaultContentLanguage: en

languages:
  en:
    languageName: English
    weight: 1
    title: HerDev Blog
    menu:
      nav:
        - name: Blog
          url: /
          weight: 1
        - name: Tags
          url: /tags/
          weight: 2

  fr:
    languageName: Français
    weight: 2
    title: HerDev Blog
    menu:
      nav:
        - name: Blog
          url: /fr/
          weight: 1
        - name: Tags
          url: /fr/tags/
          weight: 2
```

### 1) Language switcher in the navbar

When you have **2+ languages**, the theme displays a minimal language switcher in the navigation bar.
It links to the current page translation when available, otherwise it falls back to the language home.

### 2) Content structure

You can use any **Hugo-supported structure**, for example:

- content/post/my-article.md with language-specific front matter
- or split by language:
    - content/en/post/my-article.md
    - content/fr/post/my-article.md

See [Hugo documentation](https://gohugo.io/documentation/) for **translation** linkage (translationKey, same filename,
etc.).

## Footer

A small footer can be enabled by default with:

      Powered by Hugo and PaperCSS

To disable it (in blog config file, not in theme config file  ) :

```toml
params:
   hideFooter: true
```

## Shortcodes

See the example site for the full list of supported shortcodes.

## Disable toc for a blog post

Blog posts that have two or more subheadings (`<h2>`s) automatically get a table of contents. To disable this set `toc`
to `false`. For example:

```yaml
---
title: "My page with a few headings"
toc: false
---
```

## Disable summary for a blog post

The homepage blog post listing shows a summary for each post. To disable this for an individual post set `show_summary`
to `false`. For example:

```yaml
---
title: "My page with some stellar content"
show_summary: false
---
```

## Getting help

If you run into an issue that isn't answered by this documentation or the `exampleSite`, then visit the Hugo forum. The
folks there are helpful and friendly. Before asking your question, be sure to read the forum’s requesting help
guidelines.

## Credits

Thank you to [Rhyne Vlaservich](https://www.vlaservich.com/) for creating [PaperCSS](https://www.getpapercss.com/), and
all the contributors.

## License

MIT. See [LICENSE](LICENSE) for details.


