# Club404 Theme - Basic usage example

This is a basic example of how to use the theme.

## Prerequisites

You will need the follwoing dependencies to build the website:

 - [Go](https://go.dev/)
 - [Hugo](https://gohugo.io/)

## Local Development

You can start the website in local development like this:

```bash
# Add local go module (to track your dependencies) for hugo
[ -f go.mod ] || go mod init main

# Fetch and update hugo module dependencies
hugo mod get -u

# Start the website in development mode
hugo server
# <-- Typically hosted on: http://localhost:1313/
```

# Build the website for production

Yopu can build the website for production, by running:

```bash
# Remember to fetch dependencies
hugo mod get -u
hugo --minify
```