# The Shelf — affiliate shop template

A no-backend affiliate storefront. Visitors browse product cards; clicking one
sends them straight to your affiliate link in a new tab.

## Files

- `index.html` — the public shop page
- `admin.html` — where you add/edit/delete products and export the data
- `products.js` — the product data (name, description, image, link) that both pages read
- `style.css` — shared styling

## How to use it

1. Open `admin.html` in your browser (works locally, no server needed).
2. Add products: name, description, an image (paste a URL or upload a file), and your affiliate link.
3. Click **Download products.js**.
4. Replace the `products.js` file in this folder with the downloaded one.
5. Upload the whole folder to your host (see below). That's your live site.

Products you add in `admin.html` save to that browser as a draft so you don't lose work,
but the **public site only updates once you download and replace `products.js`** — there's
no live database, since that would need paid backend hosting.

## Deploying it for free

Any static host works. Easiest options:

- **Netlify / Vercel**: drag the whole folder onto their dashboard, done.
- **GitHub Pages**: push the folder to a GitHub repo, enable Pages in repo settings.
- **Cloudflare Pages**: similar drag-and-drop deploy flow.

## Notes

- Each product card is a full link with `rel="noopener sponsored"`, which is the
  recommended markup for affiliate/paid links (helps with both security and SEO).
- The footer includes a basic affiliate disclosure — check what disclosure your specific
  programs (Amazon Associates, etc.) legally require and adjust the wording if needed.
- To change the site name/tagline, edit the text near the top of `index.html`.
- To restyle it (colors, fonts), edit the `:root` variables at the top of `style.css`.
