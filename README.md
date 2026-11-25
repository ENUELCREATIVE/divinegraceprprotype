# Divine Grace Schools: Website

Static website (no build step): Home, About, Academics, Admissions, Gallery, News, Contact and the Portal Login page.
The school portals and dashboards (Students, Teachers, ICT, Principal, Super Admin) are not included.

## Deploy on Vercel
1. Push this folder to a GitHub repository (the folder contents at the repo root).
2. In Vercel choose **Add New > Project**, import the repository.
3. Framework Preset: **Other**. Build Command: leave empty. Output Directory: leave empty (the project root).
4. Deploy. `vercel.json` is already set up.

Or with the CLI: `npx vercel` inside this folder.

## Run locally
Open `index.html`, or run `npx serve .` / `python3 -m http.server 8000`.

## Structure
- `index.html, about.html, academics.html, admissions.html, gallery.html, news.html, news-article.html, contact.html, login.html`: desktop pages
- `mobile/`: the same pages in the phone layout. Phones (640px wide or less) are sent there automatically by `assets/js/device-route.js`
- `assets/images/`, `assets/fonts/` (Manrope, Space Grotesk, bundled), `assets/js/`
- `vercel.json`, `package.json`, `.gitignore`

## Settings: `assets/js/site-config.js`
- `loginUrl`: where "Login to Portal" buttons go (`login.html`, the Portal Login page).
- `portalUrl`: where the Portal Login page sends users after signing in. Empty for now: Login only checks that both fields are filled. Set it to the portal address once the portals are finalised.

## Data
Contact messages and admission applications are saved in the visitor's browser (localStorage) only. There is no server or database yet.
