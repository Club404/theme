<p align="center" style="padding-top:20px">
 <img width="100px" src="static/images/logo.svg" align="center" alt="GitHub Readme Stats" />
 <h1 align="center">Club404 - Theme</h1>
 <p align="center">Built using an opinionated Hugo starter template with Tailwind CSS 3.2 and Alpine.js with light/dark modes.</p>
</p>
  <p align="center">    
    <a href="https://gohugo.io/">
      <img src="https://img.shields.io/badge/Hugo%20-0.105.0%20-gray.svg?colorA=c9177e&colorB=FF4088&style=for-the-badge"/>
    </a>
    <a href="https://tailwindcss.com/">
      <img src="https://img.shields.io/badge/TailwindCSS%20-V3-gray.svg?colorA=0284c7&colorB=38bdf8&style=for-the-badge"/>
    </a>
    <a href="https://alpinejs.dev/">
      <img src="https://img.shields.io/badge/Alpine.js%20-V3-gray.svg?colorA=68a5af&colorB=77c1d2&style=for-the-badge"/>
    </a>
  </p>

  <p align="center">
    <a href="https://club404.io">View Demo</a>
    ·
    <a href="https://github.com/Club404/website/issues">Report Bug</a>
  </p>
</p>

## Prerequisites

This theme is designed for [Hugo](https://gohugo.io/), and it is assumed you have some knowledge of how its used as a static web server.

## Getting started

By far the easiest way to get started would be to just import this theme in your hugo config as a module:

```yaml
# File: hugo.yaml

title: "My New Hugo Site"
baseURL: "http://example.org/"
languageCode: "en-us"

module:
  imports:
    - path: github.com/Club404/theme

```

Then you can start or build the website with this theme loaded:

```bash
# Run the server locally
hugo server

# Or build the static site contents
hugo --minify
# <-- Outputs: ./public/
```

## Adding your own contents

On its own, its just an empty themed website. By adding some [markdown](https://www.markdownguide.org/cheat-sheet/) files to the `content` folder, you can add some pages to your website.

Hugo uses [certain naming conventions](https://gohugo.io/content-management/organization/) to determine how sub pages are rendered. To get you started, lets create a file called: `./content/about.md`

```yaml
---
draft: false
title: About
date: 2023-06-30
description: About this theme
language: en
---

# Hello there

This is a simple placeholder where you can add your own content
```

You will notice the metadata (also called the `front matter`) that hugo uses, that is distinct and different from the page contents (markdown).

This will create a new page that you can view at: `http://localhost:1313/about/`

### Supported file structure

The following folders are supported and monitored for your site's content:
```yaml
assets/         # Custom Images, CSS and Javescript
content/        # Your actual site content (in markdown format)
  + posts/      # Blog post entries (well known page type)
layouts/        # You can customise, extend or override your HTML layout
  + partials/   # Add or extend existing partials (custom HTML)
static/         # Additional static HTTP server content (served as-is)
```

### Page Navigation

We can go one step further, and add some menu's for page navigation. Go to your `hugo.yaml` config file, to make the new `About Us` page visible on the top and bottom navigation:

```yaml
# File: hugo.yaml

title: "My New Hugo Site"
baseURL: "http://example.org/"
languageCode: "en-us"

module:
  imports:
    - path: github.com/Club404/theme

menu:
  main:    
    - identifier: about
      name: About Us
      url: /about/
      weight: 10
    - identifier: posts
      name: Blog Posts
      url: /posts/
      weight: 20
  footer:
    - identifier: about
      name: About Us
      url: /about/
      weight: 10
```




## Local Development

You can clone and run these sources on your development environment:

```bash
# Get the sources
git clone git@github.com:club404/theme my-site
cd my-site

# Install dependencies
yarn        # or: npm install
yarn start  # or: npm run start
```

## Build and publish

You can compile the website into static content, by running:

```bash
# To generate the site HTML
yarn build  # or: npm run build
# --> This will run two commands parallel:
#  <- npx tailwindcss -i ./assets/css/main.css -o ./assets/css/theme.css --watch
#  <- hugo server
```

## Image shortcodes for webp as well.

Has paginated Categories and Tags. Markdown files will automatically convert images put into `/assets` folder to .webp images.

```
{{< imgh src="img-name.jpg" alt="Place alt text here." >}}
```

## Credits

**NUSSER STUDIOS** - Original Theme
https://github.com/nusserstudios/tailbliss

