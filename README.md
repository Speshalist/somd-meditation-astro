# Southern Maryland Meditation Community Website

Astro static site for SOMD Meditation Community. Hosted on Cloudflare Pages.

## Setup

```bash
npm install
npm run dev
```

## Project Structure

- `src/pages/` — Routes (index, agreements, events)
- `src/components/` — UI components
- `src/layouts/` — Base layout with SEO meta tags
- `src/assets/images/` — Optimized images (Astro handles WebP/AVIF)
- `public/` — Static files (favicon, etc.)

## Adding Images

1. Extract your 8 gallery photos and hero image from Wix
2. Place them in `src/assets/images/`
3. Import and use Astro's `<Image />` component:

```astro
import myImage from "../assets/images/my-image.jpg";
<Image src={myImage} alt="Descriptive text" width={800} />
```

## EmailOctopus Setup

1. In EmailOctopus, go to Forms → Embedded HTML
2. Copy the `<form>` snippet
3. Paste it into `src/components/Newsletter.astro`, replacing the placeholder form

## Deploy to Cloudflare Pages

1. Push this repo to GitHub
2. In Cloudflare Pages, create a project → Connect to Git → select this repo
3. Build settings:
   - Framework preset: Astro
   - Build command: `npm run build`
   - Build output directory: `dist`
4. Add your custom domain

## Content Updates

For now, edit the `.astro` files directly. When you're ready for non-technical editors,
we can add Decap CMS or Keystatic on top of the existing content structure.
