<p align="center" style="padding-top:20px">
 <img width="100px" src="static/images/logo.svg" align="center" alt="GitHub Readme Stats" />
 <h1 align="center">Club404 - Theme</h1>
 <p align="center">Built using an opinionated Hugo Starter with Tailwind CSS 3.2 and Alpine.js with light/dark modes.</p>
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

## Getting started

By far the easiest way to get started would be to just import this theme in your hugo config as a module:

```yaml title="hugo.config"
title: "My New Hugo Site"
baseURL: "http://example.org/"
languageCode: "en-us"

module:
  imports:
    - path: github.com/Club404/theme

```

Then you can initialise start the website with the theme loaded:

```bash
yarn
hugo mod get -u
hugo server -s .
```

## Local Development

You can clone and run these sources on your development environment:

```bash
# Get the sources
git clone git@github.com:club404/website
cd website

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
#  <- npx tailwindcss -i ./assets/css/main.css -o ./assets/css/style.css --watch
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

