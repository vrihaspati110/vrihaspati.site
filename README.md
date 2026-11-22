# Vrihaspati Tiwari — Corporate & Event Video Editor Portfolio
**Domain:** [vrihaspati.site](https://vrihaspati.site)  
**Hosting & CDN:** Cloudflare Pages  
**Version Control:** GitHub ([vrihaspati110/vrihaspati.site](https://github.com/vrihaspati110/vrihaspati.site))  
**Tech Stack:** Astro, Semantic HTML5, Vanilla CSS3

---

## 🚀 Quick Start

All commands should be executed from the root of this folder:

```bash
# Install dependencies
npm install

# Start local dev server (available at http://localhost:4321)
npm run dev

# Build production static bundle to ./dist/
npm run build

# Preview production build locally
npm run preview
```

---

## 🌐 Cloudflare Deployment & Management

This project is optimized for **Cloudflare Pages** hosting with the custom domain `vrihaspati.site`.

### Option A: Automatic Git Integration (Recommended)
1. Go to your [Cloudflare Dashboard](https://dash.cloudflare.com/) > **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**.
2. Select your repository: `vrihaspati110/vrihaspati.site`.
3. Set the build settings:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
4. Click **Save and Deploy**. Cloudflare will automatically build and publish preview and production branches.
5. In **Custom Domains**, add `vrihaspati.site` to enable automatic global SSL/TLS and DNS routing.

### Option B: Direct CLI Deployment via Wrangler
You can deploy directly to Cloudflare Pages anytime with:

```bash
# Deploy dist folder to Cloudflare Pages
npx wrangler pages deploy dist --project-name=vrihaspati-site
```

---

## 📁 Project Structure

```text
├── public/                 # Static assets (favicons, profile image)
│   ├── favicon.ico
│   ├── favicon.svg
│   └── profile.jpg
├── src/
│   ├── components/         # Astro components
│   │   └── VideoEmbed.astro# Responsive 16:9 & 9:16 video card component
│   └── pages/
│       └── index.astro     # Main portfolio page with filterable showcase
├── astro.config.mjs        # Astro configuration with site URL
├── wrangler.jsonc          # Cloudflare Pages configuration
└── package.json            # Scripts & dependencies
```

---

## 🎨 Updating Portfolio Videos & Copy

To update or replace showcase projects, open `src/pages/index.astro` and locate the `<VideoEmbed />` components in `#work`. Update:
- `videoUrl`: YouTube embed URL (e.g. `https://www.youtube.com/embed/YOUR_VIDEO_ID`)
- `title`: Project title
- `category`: `conference` | `brand` | `product` | `keynote` | `social`
- `client`: Client / Agency name
- `role`: Your specific role (e.g., "Lead Editor & Multicam Conforming")
- `softwareTag`: Primary tools used (e.g., "DaVinci Resolve", "Premiere Pro")
- `logline`: Summary of project scope and editorial achievements
