# adidrawsart — Portfolio Website

A single-file, custom-built portfolio site you fully own. No platform fees, no monthly subscription, no vendor lock-in.

**Brand identity**: `adidrawsart` everywhere visible. Full legal name is kept private — never used in public artifacts. See DEPLOY_GUIDE.md for the full privacy model.

## What's here

- `index.html` — The complete website. All HTML, CSS, and JavaScript in one file.
- `images/` — Drop artwork photos here (create the folder when ready).

## How to preview it

**On Windows:** Double-click `index.html`. It opens in your browser. That's it.

**For a better dev experience:** Open the folder in any code editor (VS Code is free) and use the "Live Server" extension for auto-reload on save.

## How to add a new piece

1. Photograph or scan the artwork. Save as JPG or PNG.
2. Recommended size: 1200–2000px on the long side. Lighter = faster site.
3. Save the file to `website/images/` with a clear name, like `2026-05-watercolor-koi.jpg`.
4. Open `index.html` in a text editor.
5. Find the `const pieces = [` block near the bottom.
6. Copy one of the placeholder objects and fill in the real values:

```javascript
{
  title: "Koi in Motion",
  medium: "Watercolor on cold-press paper",
  date: "May 2026",
  category: "traditional",   // traditional, digital, sketches, or 3d
  description: "First attempt at painting movement underwater. Built up the water in layers, kept the koi loose.",
  imgSrc: "images/2026-05-watercolor-koi.jpg",
},
```

7. Save. Refresh the browser.

## How to publish it (free)

Three good options, all free:

### Option A: GitHub Pages (recommended for long-term ownership)
1. Create a free GitHub account.
2. Create a new repo named `adipracs.github.io` (or use a Pages-enabled repo).
3. Upload the contents of this `website/` folder.
4. Live at `https://adipracs.github.io`.
5. Add a custom domain later (`adidrawsart.com` ~$10/yr or `adidrawsart.art` ~$13/yr).

### Option B: Netlify Drop
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the `website/` folder into the browser.
3. Live in 30 seconds at a random `*.netlify.app` URL.
4. Add a custom domain later from the dashboard.

### Option C: Cloudflare Pages
1. Connect a GitHub repo (same as Option A) or upload directly.
2. Free tier is generous.

## Custom domain

Going with **adidrawsart** as the unified brand. Check availability at Cloudflare Registrar, Namecheap, or Porkbun in this order:
- `adidrawsart.com`
- `adidrawsart.art`
- `adidrawsart.studio`

See `DEPLOY_GUIDE.md` for the full registration + DNS setup walkthrough.

## What to update before going live

In `index.html`, search for and replace these placeholders:

- `hello@example.com` — Real contact email (e.g., `hello@adidrawsart.com` — set up free forwarding via Cloudflare Email Routing)
- `https://www.instagram.com/` — Real `@adidrawsart` Instagram URL once created
- `https://www.behance.net/` — Real `@adidrawsart` Behance URL once created
- `https://www.artstation.com/` — Real `@adidrawsart` ArtStation URL once created (or remove the link)
- The about-section paragraphs — Rewrite in the artist's voice if desired

**Identity rule**: Use `adidrawsart` everywhere. No personal names, no last names, no full legal names anywhere on the public site or in any public artifact.

## Design choices (why it looks this way)

- **Serif headlines, sans body.** Classic art-portfolio feel. Iowan Old Style with Apple/Times fallbacks.
- **Off-white background `#fafaf7`.** Easier on the eyes than pure white; common in gallery sites.
- **Single accent color (deep blue `#1f4e79`).** Consistent with the strategic plan doc. Easy to change in the `:root` CSS variables.
- **Card-based gallery with modal preview.** Standard pattern. Filters let you switch between mediums.
- **Mobile-first responsive.** Works fine on phones, tablets, and desktops.
- **No external dependencies.** No Google Fonts, no jQuery, no analytics. Loads fast, works offline.

## Roadmap for future improvements

- Add a "Process" section with timelapse videos
- Add a "Sketchbook" archive section for raw working pages
- Add a simple blog/journal page for write-ups
- Add an RSS feed or email signup once there's an audience
- Add OpenGraph image so links share nicely on social
- Add an "Awards & Press" section once those start landing
