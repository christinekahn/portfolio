# dreamsanddelivery.com

Personal site for Christine Kahn — Staff Technical Program Manager, and host of the Dreams and
Delivery podcast. Static HTML/CSS, deployed via GitHub Pages with a custom domain.

## Structure

- `index.html` — Career: hero, bio/timeline/certifications, full case studies
- `dreams-and-delivery.html` — podcast episodes, listen/follow links, music
- `contact.html` — contact page
- `about.html`, `work.html` — redirect stubs to `index.html#career` / `index.html#work` (kept so old links don't 404)
- `styles.css` — shared stylesheet for all pages
- `christine-profile.jpeg` — profile photo
- `CNAME` — custom domain config for GitHub Pages (`dreamsanddelivery.com`)

## Deployment

Hosted on GitHub Pages, served from the repo root on the `main` branch.

Custom domain setup:
1. `CNAME` file at repo root contains `dreamsanddelivery.com`.
2. Repo Settings → Pages: source set to `main` / root, custom domain set to `dreamsanddelivery.com`.
3. DNS at the registrar (Squarespace): four `A` records on host `@` pointing to GitHub Pages IPs (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`), plus a `CNAME` record on host `www` pointing to `christinekahn.github.io`.
4. "Enforce HTTPS" enabled in Pages settings once the domain verifies.

## Local preview

No build step — open `index.html` directly in a browser, or serve the folder locally:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Notes

- No email address or contact form value is published anywhere on the site by design.
