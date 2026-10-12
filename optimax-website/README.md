# OPTIMAX Website
Responsive React + Vite homepage based on the provided visual reference.

## Run locally
1. Install Node.js 20.19+ or 22.12+.
2. In this folder, run `npm install` then `npm run dev`.
3. Open the local address shown by Vite.

## Deploy to GitHub Pages (free)
1. Create a **public** GitHub repository called `optimax-website`.
2. Upload **all project files and folders**, including `.github/workflows/deploy.yml`, to the repository root (not the ZIP itself).
3. Commit to the `main` branch.
4. In GitHub, open **Settings → Pages → Build and deployment → Source**, select **GitHub Actions**.
5. In **Actions**, wait for the **Deploy to GitHub Pages** workflow to finish.
6. Open `https://YOUR-USERNAME.github.io/optimax-website/`.

For easiest upload, unzip on your computer, then use GitHub Desktop to commit the complete project folder. GitHub browser uploader may not preserve hidden `.github` files easily, so confirm the workflow file is committed.

## Important before publishing
- Image URLs currently load remote editorial stock photography (Unsplash) and are not official OPTIMAX assets. Replace with licensed, approved corporate photos in `public/images`, then update paths in `src/main.jsx`.
- Logos in the partner row are text placeholders and must be replaced with approved partner logos.
- Appointment and other navigation links currently lead to relevant sections of this single-page demo. Wire to approved routes or booking system when available.
- Enquiry form uses `mailto:` and is **not a submission backend**. Configure Formspree, your API, or another approved service after confirming your intended destination and privacy requirements.
- The checkbox is a **demo**, not reCAPTCHA security.
- Social links point to generic platform homepages, not official OPTIMAX profiles.
- Content was transcribed from the supplied screenshot. Verify approved claims and text before launch.

## Build
`npm run build` creates the `dist` folder.
