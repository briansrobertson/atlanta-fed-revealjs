# Atlanta Fed RevealJS Quarto Theme

A [Quarto](https://quarto.org) extension providing a [RevealJS](https://revealjs.com) presentation theme that matches the Federal Reserve Bank of Atlanta's official PowerPoint template.

## Installation

Install the extension into an existing Quarto project:

```bash
quarto add briansrobertson/atlanta-fed-revealjs
```

Or use this repo as a template to start a new presentation:

```bash
quarto use template briansrobertson/atlanta-fed-revealjs
```

## Usage

Add the following YAML front matter to your `.qmd` file:

```yaml
---
title: "Presentation Title"
subtitle: "Subtitle or Author Name"
date: "March 14, 2023"
format:
  atlanta-fed-revealjs: default
---
```

Use `##` headings to create content slides:

```markdown
## Slide Title

Body text here.

- Bullet point one
- Bullet point two
- Bullet point three
```

> **Note:** `logo.png` and `title_background.jpg` are embedded directly in the extension — no external asset files are required in your project directory.

## Slide Types

### Title Slide
Automatically generated from YAML front matter. Displays the date, title, subtitle, and Atlanta Fed logo over the branded background image — all embedded in the extension.

### Content Slide (`##`)
Blue gradient header bar with white heading, white body area, and slide number in the bottom-right corner.

### Two-Column Layout
Use Quarto's built-in `.columns` div:

```markdown
## Slide Title

::: {.columns}
::: {.column}
Left column content
:::
::: {.column}
Right column content
:::
:::
```

### Tables
Standard Markdown tables are styled automatically with the Atlanta Fed blue header.

```markdown
## Slide Title

| Column A | Column B | Column C |
|----------|----------|----------|
| Value 1  | Value 2  | Value 3  |
```

## Design Specifications

| Element | Font | Size | Color | Position |
|---|---|---|---|---|
| Date (title slide) | IBM Plex Sans | 20pt | White | 0.625" from left, 1.35" from top |
| Title (title slide) | IBM Plex Sans Bold | 48pt | White | 0.625" from left, 2.75" from top |
| Subtitle (title slide) | IBM Plex Sans | 24pt | White | 0.625" from left, 3.94" from top |
| Logo (title slide) | — | 64px tall | — | 0.625" from left, 6.25" from top |
| Heading (content slides) | IBM Plex Sans | 36pt | White | 1" from left, centered in 1.75" bar |
| Body text | IBM Plex Sans | 28pt | Black | 1" from left, 2" from top |
| Slide number | IBM Plex Sans | 12pt | Black | Bottom-right |

- **Slide canvas:** 1280 × 720px (16:9 widescreen)
- **Header bar:** Blue gradient (`#1065A2` → `#7AACC8`), 1.75" tall, full width
- **Body padding:** 1" (96px) left and right
- **Font:** [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) (loaded from Google Fonts)

## Rendering

```bash
quarto render your-presentation.qmd
```

### Export as PDF (one slide per page)

```bash
quarto render your-presentation.qmd --to pdf
```

Or open the rendered HTML in your browser and use **File → Print → Save as PDF**, setting paper size to landscape.

## Keyboard Navigation

The rendered presentation supports standard RevealJS keyboard shortcuts:

| Key | Action |
|---|---|
| `→` / `Space` | Next slide |
| `←` | Previous slide |
| `F` | Toggle fullscreen |
| `Esc` | Exit fullscreen |
| `?` | Show all shortcuts |

## License

Internal use — Federal Reserve Bank of Atlanta.
