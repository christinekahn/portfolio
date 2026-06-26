# christinekahn.com

Personal portfolio site for Christine Kahn — Staff Technical Program Manager. Static HTML/CSS, deployed via GitHub Pages with a custom domain.

## Structure

- `index.html` — home / hero
- `work.html` — selected work / case studies
- `about.html` — about page
- `contact.html` — contact page
- `styles.css` — shared stylesheet for all pages
- `christine-profile.jpeg` — profile photo
- `CNAME` — custom domain config for GitHub Pages (`christinekahn.com`)

## Deployment

Hosted on GitHub Pages, served from the repo root on the `main` branch.

Custom domain setup:
1. `CNAME` file at repo root contains `christinekahn.com`.
2. Repo Settings → Pages: source set to `main` / root, custom domain set to `christinekahn.com`.
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
