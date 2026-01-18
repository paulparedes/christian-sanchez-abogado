# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Development server (includes drafts)
hugo server -D

# Production build
hugo --gc --minify

# Create new blog post
hugo new blog/post-name.md

# Create new publication
hugo new publications/publication-name.md

# Initialize theme after clone
git submodule update --init --recursive
```

## Architecture

This is a Hugo static site for a labor law attorney, using the PaperMod theme.

**Theme**: PaperMod (Git submodule in `themes/PaperMod/`). Requires Hugo v0.146.0+.

**Content sections**:
- `content/blog/` - Blog posts about labor law topics
- `content/publications/` - Academic articles and publications
- Static pages: `about.md`, `services.md`, `contact.md`

**Customization layers**:
- `assets/css/extended/custom.css` - Custom styles (color palette: navy #1a365d, gold #c9a227)
- `layouts/partials/extend_head.html` - SEO meta tags, Schema.org markup
- `layouts/partials/extend_footer.html` - Footer customization

**Forms**: Contact and newsletter forms use Netlify Forms (`data-netlify="true"` attribute in `contact.md`).

**Deployment**: Netlify auto-deploys from main branch. Configuration in `netlify.toml`.

## Content Frontmatter

Blog/publication posts require:
```yaml
---
title: "Title"
date: 2026-01-17
description: "Brief description"
tags: ["derecho laboral", "tag2"]
categories: ["Category"]
author: "Christian Sánchez"
draft: false
---
```

## Configuration

Main config: `hugo.toml` (Spanish language, homeInfoParams for homepage text, menu items, social icons).
