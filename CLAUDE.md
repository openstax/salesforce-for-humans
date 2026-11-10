# CLAUDE.md

Guidance for anyone (human or agent) editing this repository.

## What this is

**Salesforce for Humans** is the OpenStax field guide to Salesforce, written by the Data Intelligence
team for everyday users: Customer Experience, Sales and the SDR, Marketing, Finance, Fundraising, and
leadership. It is a Jekyll site published by GitHub Pages from `main`:
https://openstax.github.io/salesforce-for-humans/

**The repo and the site are public.** Write every sentence as if a stranger will read it.

## Never publish

- Costs, contracts, renewals, vendor terms, or internal strategy about Salesforce itself.
- Staff names. Use roles and teams ("the Data Intelligence team", "CX", "the SDR").
- Bugs, outages, incidents, error rates, backlog sizes, or anything that reads as an internal post-mortem.
- Security and permission details (permission set names, integration users, API specifics), record IDs.
- Any personal data. Student data is FERPA-protected; donor data is restricted.
- Real institutions or real people as examples. Use the fictional cast below.

Internal links that need an OpenStax login (Slack channel names, Jira, Confluence page titles, Tableau)
are fine to name.

## Structure

```
_config.yml        Jekyll config; `modules` collection, jekyll-redirect-from plugin
_data/parts.yml    The five parts (number, title, blurb) used by the landing page and sidebar
_layouts/          default.html (header/footer), module.html (sidebar by part, In short box, prev/next)
_modules/NN-slug.md  One file per module; the filename is the URL (/modules/NN-slug/)
assets/css/style.css Brand tokens and all styles
assets/images/*.svg  Hand-written SVG illustrations
index.html         Landing page: modules grouped by part
```

Module front matter:

| Key | Meaning |
|---|---|
| `number` | Global sort order (1–21) |
| `part` | Part number from `_data/parts.yml` |
| `title`, `short_title`, `description` | Page title, sidebar label (≤ 26 chars), landing-card sentence |
| `key_points` | 3–4 bullets rendered as the "In short" box (Markdown allowed) |
| `redirect_from` | Old URLs that should land on this module. **Renaming a module file changes its URL: add the old path here.** |

Body conventions: `##` for sections, tables for reference values, callouts as
`<div class="callout callout-green|callout-orange|callout-blue" markdown="1">…</div>`
(green = try it, orange = hands off / caution, blue = good to know), images as
`![full description]({{ '/assets/images/file.svg' | relative_url }})`, cross-links as
`{{ '/modules/NN-slug/' | relative_url }}`.

## Content rules

- **Facts must be verified against the production org or the Data Intelligence team**, not written from
  memory or from older pages of this book. Org metadata is mirrored in the `openstax/salesforce` repo.
  Salesforce changes often; when a module describes a field, stage or value, use the label users see.
- Fictional cast for examples: **Cedar Bluff Community College** (2-year, Canvas), **Northgate State
  University** (4-year), **Willow Creek Unified School District** and **Willow Creek High School**,
  **Dr. Maya Rivera** (she, A&P instructor at Cedar Bluff), **Sam Okafor** (they, Biology at Northgate,
  new signup), **Ms. Dana Brooks** (she, Algebra 1 teacher at Willow Creek High). Example numbers are
  invented; label example dashboards "Example data".
- School years are written the way Salesforce stores them: `2026 - 27` (July 1 to June 30, the same as
  the fiscal year). Don't label adoptions with "FY".
- Don't quote mission-impact totals; they come from Tableau and change daily. Point to the official
  figures.
- Voice: plain, warm, confident, lightly wry. Short paragraphs. No hype, no filler openers, no
  "it's not X, it's Y" constructions.

## SVG conventions

~800px-wide `viewBox`, `font-family="Lato, -apple-system, sans-serif"`, `#F7F8FA` rounded background,
brand colors (blue `#0D2C6C`, green `#77AF42`, dark green `#0C9372`, orange `#F47641`, gold `#FDBD3E`,
gray text `#5E6062`, border `#E5E7EB`). Name new files after their module (`10-signup-to-contact.svg`).
Check that text fits its box and that the file parses (`xmllint --noout file.svg`).

## Commands

Needs Ruby 3.x (system Ruby 2.6 on macOS is too old for the gems).

```bash
bundle config set --local path vendor/bundle   # once
bundle install
bundle exec jekyll serve --livereload           # http://localhost:4000/salesforce-for-humans/
bundle exec jekyll build                        # what CI/Pages does
```

GitHub Pages builds `main` automatically (legacy build with the `github-pages` gem). Changes reach the
public site a few minutes after merge, so work on a branch and open a PR.
