# Medar · مدار

**Immersive AI/AR heritage experience for Madinah's historic sites.**

Live at **[medar.website](https://medar.website)** · Contact: **fadel.a.alobaidi@gmail.com**

---

## Files

```
medar/
├── index.html               ← the entire site (HTML + CSS + JS)
├── CNAME                    ← contains: medar.website
├── README.md                ← this file
└── images/
    ├── medar-app-tour.jpg       (hero — AR Tour Guide product mockup)
    ├── medar-app-phone.jpg      (Bir Al-Fuqayr site card — phone view)
    ├── saqifah-interior.jpg     (Al-Suffah site card)
    ├── saqifah-courtyard.jpg    (gallery)
    ├── saqifah-exterior.jpg     (gallery — outdoor reconstruction)
    ├── saqifah-architecture.jpg (architecture detail block)
    ├── bir-ghars-well.jpg       (Bir Ghars site card)
    └── bir-ghars-site.jpg       (gallery — real site marker)
```

All images use relative paths (`images/...`), so the whole folder ships as-is.

## Deploy on GitHub Pages

1. Create a new public repository on GitHub (e.g. `medar` or `<user>.github.io`).
2. Push the entire `medar/` contents to the repo root: `index.html`, `CNAME`, `README.md`, and the `images/` folder.
3. Repo **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. After a minute the site will be live at `https://<user>.github.io/<repo>/`, then it switches to `https://medar.website` once DNS is set.

## Wire up medar.website

The `CNAME` file already contains `medar.website`. At your registrar:

- **Apex** (`medar.website`): four `A` records pointing to GitHub Pages IPs:
  ```
  185.199.108.153
  185.199.109.153
  185.199.110.153
  185.199.111.153
  ```
- **www subdomain** (`www.medar.website`): one `CNAME` record pointing to `<user>.github.io`.

Back in **Settings → Pages**, enter `medar.website` as the custom domain. Tick **Enforce HTTPS** once the certificate is issued (usually within an hour).

## Customization

- **Colors / theme:** CSS variables at the top of `index.html` (`:root { … }`). Edit `--gold`, `--night-1`, etc.
- **Language:** Arabic-first with EN toggle. Bilingual text uses `data-ar` / `data-en` attributes throughout — search-replace within each pair to update copy.
- **Stats:** all sourced from public reporting and linked beneath each card.
- **Images:** drop a new file into `images/` with the same filename to swap. To add, edit the relevant `<img>` reference.
- **Form:** uses a `mailto:fadel.a.alobaidi@gmail.com` fallback so it works on GitHub Pages without a backend. When you want a proper form, swap for Formspree / Web3Forms.
- **Logo:** the inline SVG in nav and footer plays on the "MedAr = Medinah AR" name. Edit the SVG paths directly to refine.

## Content principles

All historical content references the verified prophetic biography (sīrah) and is intended to be reviewed by qualified scholars before any AR scene ships to the public. The Prophet ﷺ is represented as light (not figure), in keeping with traditional Islamic visual ethics.
