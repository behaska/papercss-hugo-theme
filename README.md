# PaperCSS Hugo Theme (maintained fork)

This repository is a maintained fork of the original **papercss-hugo-theme** created by **zwbetz-gh**.

The upstream project is archived and no longer actively maintained. I’m maintaining this fork to keep the theme usable with recent Hugo versions and to continue making incremental improvements while preserving the spirit and simplicity of the original theme.

## Table of contents

- [Demo](#demo)
- [Minimum Hugo version](#minimum-hugo-version)
- [Installation](#installation)
- [Updating](#updating)
- [Run example site](#run-example-site)
- [Configuration](#configuration)
- [Favicons](#favicons)
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

Upload your image to RealFaviconGenerator, then copy-paste the generated favicon files under `static`.

## Shortcodes

See the example site for the full list of supported shortcodes.

## Disable toc for a blog post

Blog posts that have two or more subheadings (`<h2>`s) automatically get a table of contents. To disable this set `toc` to `false`. For example:

```yaml
---
title: "My page with a few headings"
toc: false
---
```

## Disable summary for a blog post

The homepage blog post listing shows a summary for each post. To disable this for an individual post set `show_summary` to `false`. For example:

```yaml
---
title: "My page with some stellar content"
show_summary: false
---
```

## Getting help

If you run into an issue that isn't answered by this documentation or the `exampleSite`, then visit the Hugo forum. The folks there are helpful and friendly. Before asking your question, be sure to read the forum’s requesting help guidelines.

## Credits

Thank you to [Rhyne Vlaservich](https://www.vlaservich.com/) for creating [PaperCSS](https://www.getpapercss.com/), and all the contributors.

## License

MIT. See [LICENSE](LICENSE) for details.


