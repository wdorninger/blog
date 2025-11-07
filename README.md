# Blog

A simple blog built with Jekyll, a static site generator.

## Features

- Static site generation with Jekyll
- Blog-aware (posts, pages, layouts)
- RSS feed support
- Clean and responsive design with Minima theme

## Prerequisites

- Ruby (version 3.0 or higher)
- Bundler

## Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   bundle install
   ```

## Usage

### Build the site

To build the site and generate static files in the `_site` directory:

```bash
bundle exec jekyll build
```

### Serve locally

To serve the site locally with auto-regeneration:

```bash
bundle exec jekyll serve
```

Then visit `http://localhost:4000` in your browser.

### Create a new post

Create a new file in the `_posts` directory with the format:
```
YYYY-MM-DD-title-of-post.md
```

Add front matter at the top of the file:
```yaml
---
layout: post
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS +0000
categories: category1 category2
---

Your post content here...
```

## Project Structure

```
.
├── _config.yml          # Jekyll configuration
├── _posts/              # Blog posts
├── _layouts/            # Custom layouts (optional)
├── _includes/           # Reusable components (optional)
├── index.html           # Home page
├── Gemfile              # Ruby dependencies
└── _site/               # Generated site (not committed)
```

## Customization

Edit `_config.yml` to customize your blog's title, description, and other settings.