# OPTIMAX Visual Editor V2

Editable React + Vite homepage with a free browser-based visual editor.

## Links
- Website: `https://khairiyasinpc-source.github.io/Optimax/`
- Editor after deployment: `https://khairiyasinpc-source.github.io/Optimax/?edit=1`

## V2 features
- Click-to-select text, image, or button directly in the embedded site preview.
- Layers list for every editable homepage section, with drag-to-reorder, up/down buttons, hide/show, lock/unlock, and per-section padding/background controls.
- Properties for text, typography (family, size, weight, alignment, line height, letter spacing, color).
- Images: URL, upload compressed WebP, Media Library, fit, image position, optional height.
- Buttons: text, link, width, height, radius, font size, text/background color.
- Duplicate, delete, add, or move treatment, solution and news cards (up to 12 each).
- Global theme with brand colors, page background, typography and responsive section spacing.
- Undo/Redo, import/export JSON, local draft autosave, responsive preview and preview mode.

## Publishing, no backend

1. Make edits at `?edit=1`. Local drafts are automatically stored in the same browser when storage permits.
2. Click `Export for GitHub` to download `site-content.json`.
3. Replace **`Optimax/optimax-website/public/site-content.json`** in your existing repository. Keep filename and path exact.
4. Commit changes. Wait until GitHub Actions succeeds. Refresh the normal website URL.

Editor access is **not protected**. Anyone with editor link can change only their browser-local draft. Do not put GitHub tokens, credentials, or personal patient data into this editor. Only GitHub collaborators with write access can publish.

## Updating V1 -> V2

Keep the existing root `.github/workflows/main.yml` workflow. Merge the contents of this `optimax-website/` folder into the **existing** folder in GitHub. Do not nest the directory as `optimax-website/optimax-website/`. The root workflow previously created in GitHub should run `npm install` and `npm run build -- --base=/Optimax/` with working directory `./optimax-website`, then deploy `./optimax-website/dist`.

A separate `optimax-website/.github` folder is not needed and has intentionally been excluded from this ZIP.

## Local commands

Requires Node.js LTS:

```bash
npm install
npm run dev
npm run test:logic
npm run build
```

This package passed code syntax parsing and data logic tests. **A full npm/Vite build was not verified in the authoring environment** because npm registry access returned a DNS error. Check the GitHub Actions build after upload.

## Boundaries

- This is an editor for the homepage currently implemented in the repo, not a multi-page CMS or unrestricted Figma-like positioning canvas.
- Reorder applies to homepage sections; card lists support add/duplicate/delete/reorder.
- No direct GitHub publish, authentication, or backend. Drafts are browser-local and may be lost on clearing browser data. Always export JSON as backup.
- Uploaded images are stored as WebP data URLs inside exported JSON; high image counts can exceed browser storage or make the website slow. For production, put optimized files in `public/images/` and set image URLs accordingly.
- The enquiry form uses `mailto:` without an addressed recipient; it does not accept server-side submissions.
- Existing example photos are external stock links. Partner names are placeholders. Verify all copy, links, imagery rights and medical claims before using as official public marketing.
