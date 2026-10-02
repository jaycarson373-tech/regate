# Aggregate / Regate

A responsive, Rinse-inspired Solana swap interface built with plain HTML, CSS, and JavaScript.

## Run locally

Open `dist/index.html` directly in a browser, or serve the site:

```sh
python3 -m http.server 8080 --bind 127.0.0.1 --directory dist
```

Then visit http://127.0.0.1:8080.

## Features

- Swap and send demo modes
- Searchable coin picker with six sample assets
- Estimated quotes with an illustrative fee
- Up to five recipient wallets and an equal output split
- Pace settings, review, and simulated completion
- Demo wallet connection
- Responsive layout, walkthrough, and FAQ

## Current status

This is an interactive frontend demo. Prices and fees are illustrative. Wallet connections are simulated. It does not sign transactions, move funds, provide privacy routing, or run a custody backend.

## Files

- `dist/index.html`: page structure and content
- `dist/style.css`: responsive styling
- `dist/app.js`: interactions and demo calculations
- `.openai/hosting.json`: static hosting configuration; no Site is registered

## Deploy

Publish the contents of `dist` using a static web host. No build step or dependencies are required. Google Fonts are loaded when available, with fallback fonts otherwise.

A manual GitHub Pages workflow is prepared in `.github/workflows/deploy.yml`. After Pages is enabled with GitHub Actions as its source, run **Actions → Deploy Aggregate → Run workflow**.

Deployment is currently blocked: GitHub rejected Pages for this private repository under the account’s current plan. Keeping the source private requires a compatible GitHub plan or another host. Making the repository public requires owner approval. The prepared workflow has not been run.

## Check JavaScript

```sh
node --check dist/app.js
```
