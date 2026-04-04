# Salesforce for Humans

**How OpenStax Manages Relationships, Tracks Its Mission, and Turns Data Into Impact**

An open, internal field guide to Salesforce at OpenStax — written for anyone who uses the system, is curious about how it works, or just wants to understand how their clicks become someone else's decisions.

Built by the Data Intelligence team. Hosted on GitHub Pages. Published with the full awareness that a free textbook company writing a free book is exactly the kind of thing we would do.

## Local Development

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve --livereload

# Open http://localhost:4000/salesforce-for-humans/
```

Requires Ruby 2.7+ and Bundler. If you're on macOS, `brew install ruby` will get you there.

## Deployment

This site is designed for GitHub Pages:

1. Push to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to the branch you want to deploy from (usually `main`)
4. Update `baseurl` in `_config.yml` to match your repo name

GitHub Pages will build and serve the site automatically on push.

## Structure

```
├── _config.yml          # Jekyll configuration
├── _layouts/
│   ├── default.html     # Base layout (header, footer, brand bar)
│   └── module.html      # Module page layout (sidebar TOC, prev/next nav)
├── _modules/            # 17 module content files (Markdown + front matter)
├── assets/
│   └── css/style.css    # OpenStax-branded styles
├── index.html           # Landing page with module grid
├── Gemfile              # Ruby dependencies
└── README.md            # You are here
```

## Content

The `_modules/` directory contains 17 Markdown files, one per module. Each has front matter with:

- `number` — Sort order (1-17)
- `title` — Full module title
- `short_title` — Abbreviated title for sidebar navigation
- `description` — One-line summary for the landing page cards

Edit module content directly in the Markdown files. The Jekyll collection handles navigation, ordering, and layout automatically.

## Brand

Uses the OpenStax visual identity: Lato typography, the green/blue/orange palette, and the rainbow accent bar. Brand tokens are defined as CSS custom properties in `style.css` for easy updates.

## License

Internal OpenStax resource. Content is authored by the Data Intelligence team for organizational use.
