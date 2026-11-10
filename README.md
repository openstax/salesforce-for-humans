# Salesforce for Humans

**How OpenStax Manages Relationships, Tracks Its Mission, and Turns Data Into Impact**

A field guide to Salesforce at OpenStax, for anyone who uses the system or wants to understand how their clicks become someone else's decisions. Read it at https://openstax.github.io/salesforce-for-humans/.

Built by the Data Intelligence team and published on GitHub Pages. Yes, a free textbook nonprofit wrote a free book about its own data.

Contributors: read [CLAUDE.md](CLAUDE.md) first. The site is public, and it explains what may and may not go in it.

## Local Development

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve --livereload

# Open http://localhost:4000/salesforce-for-humans/
```

Requires Ruby 3.x and Bundler (the macOS system Ruby is too old). Run `bundle config set --local path vendor/bundle` once to keep gems inside the repo.

## Deployment

GitHub Pages builds and publishes `main` automatically. Work on a branch and open a pull request; the public site updates a few minutes after merge.

## Structure

```
├── _config.yml          # Jekyll configuration (modules collection, redirects plugin)
├── _data/parts.yml      # The five parts that group the modules
├── _layouts/
│   ├── default.html     # Base layout (header, footer, brand bar)
│   └── module.html      # Module page layout (sidebar by part, In short box, prev/next nav)
├── _modules/            # 21 module files (Markdown + front matter)
├── assets/
│   ├── css/style.css    # OpenStax-branded styles
│   └── images/          # SVG illustrations
├── index.html           # Landing page, modules grouped by part
├── CLAUDE.md            # Contributor and agent guide (content rules)
├── Gemfile              # Ruby dependencies
└── README.md            # You are here
```

## Content

The `_modules/` directory contains 21 Markdown files in five parts. Each has front matter with:

- `number`: sort order (1-21)
- `part`: which part it belongs to (see `_data/parts.yml`)
- `title`, `short_title`, `description`: page title, sidebar label, landing-card summary
- `key_points`: 3-4 bullets shown in the "In short" box
- `redirect_from`: old URLs that should land on this module (the filename is the URL, so add the old path when you rename a file)

Edit module content directly in the Markdown files. The Jekyll collection handles navigation, ordering, and layout.

## Brand

Uses the OpenStax visual identity: Lato typography, the green/blue/orange palette, and the rainbow accent bar. Brand tokens are defined as CSS custom properties in `style.css` for easy updates.

## License

OpenStax resource authored by the Data Intelligence team.
