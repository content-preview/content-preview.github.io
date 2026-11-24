# Global Spellbound Initiative website

The GSI website is an English-language, mobile-friendly Astro site for the initial launch phase. It introduces GSI, describes programs as planned or in development, and offers adult-facing family, volunteer, partnership, sponsorship and contact inquiries.

## Local development

Requirements: Node.js 22.12 or later and npm.

```powershell
npm ci
npm run dev
```

Open the local URL printed by Astro. Build and preview the production site with:

```powershell
npm run build
npm run preview
```

## Deploy to GitHub Pages

This repository is configured as the user site `https://content-preview.github.io`. The GitHub Actions workflow at `.github/workflows/deploy.yml` installs the Node dependencies, builds the Astro site, and deploys the `dist` output.

1. In GitHub, open the repository's **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **GitHub Actions** (not **Deploy from a branch**).
3. Push changes to the `main` branch, or run **Build and deploy Astro site** from the **Actions** tab using **Run workflow**.
4. Wait for the workflow to finish, then visit `https://content-preview.github.io`.

If GitHub Pages is left on **Deploy from a branch**, GitHub runs Jekyll on the Astro source files and reports invalid YAML front matter. Astro pages are not Jekyll files; the GitHub Actions workflow must deploy the generated `dist` directory instead.
