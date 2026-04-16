# PGx CDS — marketing & legal site

Static site for the **PGx Clinical Decision Support** mobile app: home page, privacy policy, and terms of use. Intended for Google Play listing URLs and general reference.

## Deploy on Vercel

1. Push this folder as its **own Git repository** (or set **Root Directory** to `pgx-cds-website` if it lives in a monorepo).
2. In Vercel: **Add New Project** → import the repo.
3. Framework preset: **Other** (no build command). Output is static files at the root.
4. Deploy.

After deploy, use these URLs in Play Console:

- Privacy policy: `https://<your-domain>/privacy`
- **Account deletion (Data safety):** `https://<your-domain>/account-deletion`
- Terms (optional link): `https://<your-domain>/terms`

## Local preview

Open `index.html` in a browser, or serve the folder with any static server so `/privacy` and `/terms` rewrites work (or open `privacy.html` and `terms.html` directly).

Example with Python:

```bash
cd pgx-cds-website
python -m http.server 8080
```

Then visit `http://localhost:8080` — clean paths `/privacy` and `/terms` need Vercel or a server that applies the same rewrites; locally you can use `http://localhost:8080/privacy.html`.

## Play Store link

The home page includes a Google Play button using package id `com.pgxcds.mobile`. Update `index.html` if the final store URL differs.
