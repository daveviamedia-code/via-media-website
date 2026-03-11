# Via Media Website

A modern, avant-garde website built with Astro for Via Media - a digital solutions agency.

## 🚀 Features

- **Modern Stack**: Astro 5.x, Tailwind CSS, TypeScript
- **Responsive Design**: Mobile-first, works on all devices
- **Performance Optimized**: Zero JavaScript by default, lazy loading
- **SEO Ready**: Meta tags, OpenGraph, sitemap.xml, robots.txt
- **Accessibility**: WCAG compliant, semantic HTML, focus states
- **Dual Deployment**: Ready for GitHub Pages and Cloudflare Pages

## 📁 Project Structure

```
via-media-website/
├── public/
│   ├── logo.png          # Company logo
│   ├── sitemap.xml       # SEO sitemap
│   ├── robots.txt        # Search engine directives
│   └── _routes.json      # Cloudflare Pages config
├── src/
│   ├── components/
│   │   ├── Header.astro  # Navigation header
│   │   └── Footer.astro  # Site footer
│   ├── layouts/
│   │   └── Layout.astro  # Base layout with SEO
│   ├── pages/
│   │   ├── index.astro   # Home page
│   │   ├── hosting.astro # Hosting services
│   │   ├── portfolio.astro # Project portfolio
│   │   ├── support.astro # Support center
│   │   ├── contact.astro # Contact form
│   │   └── 404.astro     # Error page
│   └── styles/
│       └── global.css    # Global styles & Tailwind
├── .github/
│   └── workflows/
│       └── deploy.yml    # GitHub Actions workflow
└── astro.config.mjs      # Astro configuration
```

## 🛠️ Development

### Prerequisites

- Node.js 18+ 
- npm or pnpm

### Install Dependencies

```bash
npm install
```

### Start Development Server

```bash
npm run dev
```

The site will be available at `http://localhost:4321`

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## 🎨 Brand Colors

| Color | Hex | Usage |
|-------|-----|-------|
| Orange | `#F58634` | Primary brand, CTAs |
| Red | `#E74C3C` | Accent, gradients |
| Gray | `#4A4F5C` | Text, dark backgrounds |
| Cream | `#FEF9F5` | Page background |

## 🚀 Deployment to Cloudflare Pages

### Option 1: Git Connection (Recommended)

1. **Initialize Git repository:**
   ```bash
   cd via-media-website
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **Push to GitHub/GitLab:**
   ```bash
   git remote add origin <your-repo-url>
   git branch -M main
   git push -u origin main
   ```

3. **Connect to Cloudflare:**
   - Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/)
   - Go to **Pages > Create a project**
   - Connect your Git repository (GitHub or GitLab)
   - Configure build settings:
     - **Build command**: `npm run build`
     - **Build output directory**: `dist`
     - **Environment variables**: `NODE_VERSION=20`
   - Click **Deploy**

4. **Automatic deployments:** Every push to `main` will trigger a new deployment automatically.

### Option 2: Wrangler CLI (Direct Deploy)

```bash
# Install Wrangler
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Deploy
wrangler pages deploy dist --project-name=via-media
```

### Option 3: Manual Upload

1. Build the project: `npm run build`
2. In Cloudflare Dashboard, go to **Pages**
3. Click **Create a project > Direct Upload**
4. Upload the `dist` folder

## 📱 Pages Overview

| Page | Route | Description |
|------|-------|-------------|
| Home | `/` | Hero, services, stats, about, CTA |
| Hosting | `/hosting` | Pricing plans, features, FAQ |
| Portfolio | `/portfolio` | Project gallery with filtering |
| Support | `/support` | Knowledge base, contact options |
| Contact | `/contact` | Contact form, company info |

## ✏️ Customization

### Updating Content

All page content is in `src/pages/*.astro`. Edit the text directly in the files.

### Adding New Pages

1. Create a new `.astro` file in `src/pages/`
2. Import and use the `Layout` component
3. Add the page to the navigation in `src/components/Header.astro`

### Changing Colors

Edit `tailwind.config.mjs` to update the brand colors:

```js
colors: {
  via: {
    orange: '#F58634', // Change here
    // ...
  }
}
```

## 📄 License

Copyright © 2026 Via Media. All rights reserved.
