# zedapex.com website

A one-page static site: plain HTML, CSS and JavaScript, with no build step and no server code.

## Files

```
index.html           the whole site (styles and scripts inside)
assets/              logo (white/black/badge), favicon, social preview image, product logos
robots.txt
```

## Edit links and contacts

Open `index.html` and find the block that starts with `const CONFIG = {` near the bottom. Change these:

- `email`: where the contact form sends messages (default hello@zedapex.com).
- `telegram`: the Telegram username, without @.
- `voosquare`: the VooSquare link.
- `products`: each product's name, one-line description, link and status (`live`, `new` or `soon`). Leave `url: ''` for a product that has no site yet.

The contact form opens the visitor's email app with the message filled in. To receive messages in a dashboard instead, point the form at a service such as Formspree or a Telegram bot. That needs a small code change in the `submit` handler.

## Put it online (about 5 minutes)

Any static host works. Pick one:

- **Cloudflare Pages:** Create project → Direct upload → drop this folder. Then add the custom domain `zedapex.com`.
- **Netlify:** drag this folder onto app.netlify.com/drop, then add the domain.
- **Railway:** New project → Deploy from GitHub (with this folder as the repo) using a static template, or serve it with any static file server.
- **Shared hosting / cPanel:** upload the folder's contents to `public_html`.

After the domain points to the host, open the site on a phone and check:
- the menu works;
- the product links open;
- the form opens an email.

## Fonts

The site loads Archivo, Hanken Grotesk and JetBrains Mono from Google Fonts. Nothing to install.
