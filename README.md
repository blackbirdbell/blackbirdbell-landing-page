# Blackbird Bell — landing page

The marketing site for [blackbirdbell.com](https://blackbirdbell.com): general-purpose
data & analytics consulting, and software for life and civil society.

Plain static HTML/CSS/JS — no framework, no build step. Everything served lives in
[`public/`](public/).

## Develop

Open `public/index.html` in a browser, or:

```sh
npx wrangler dev
```

## Deploy

Hosted on Cloudflare Workers (static assets). Config in [`wrangler.jsonc`](wrangler.jsonc).

```sh
npx wrangler deploy
```

### Custom domain

The `blackbirdbell.com` zone must be on the Cloudflare account (Dashboard → Add site,
then update nameservers at the registrar). After that, uncomment the `routes` block in
`wrangler.jsonc` and redeploy — Cloudflare provisions DNS and certificates automatically.
