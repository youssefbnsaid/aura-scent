# AURA SCENT

> A considered fragrance house for discovering signature scents.

AURA SCENT is a premium fragrance storefront designed around exploration, intuition, and personal expression. Browse curated compositions, filter by scent family, save favorites, add products to a cart, and use the fragrance finder to discover a considered recommendation.

## Highlights

- Editorial luxury storefront with responsive desktop and mobile layouts
- Fragrance catalog with search, sorting, scent-family filters, and audience filters
- Product quick view and dedicated product detail pages
- Wishlist, cart drawer, cart page, and checkout flow
- Fragrance finder quiz with personalized recommendations
- Product reviews persisted locally in the browser
- Light and dark themes with local preference persistence
- Smooth page and product interactions powered by Framer Motion

## Technology

- React 19 and TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Lucide React
- Wouter
- pnpm workspaces

## Local development

Requirements:

- Node.js 20.19+ or Node.js 22+
- pnpm 10+

Install dependencies from the repository root:

```bash
pnpm install
```

Start the storefront:

```bash
PORT=5173 BASE_PATH=/ pnpm --filter @workspace/aura-scent run dev
```

Open `http://localhost:5173`.

On Windows PowerShell:

```powershell
$env:PORT="5173"
$env:BASE_PATH="/"
pnpm --filter @workspace/aura-scent run dev
```

## Production build

```bash
PORT=4173 BASE_PATH=/ pnpm --filter @workspace/aura-scent run build
PORT=4173 BASE_PATH=/ pnpm --filter @workspace/aura-scent run serve
```

The production files are generated in `artifacts/aura-scent/dist/public`.

## Project structure

```text
artifacts/aura-scent/
├── public/          # Favicon and public metadata
├── src/App.tsx      # Storefront routes, data, and interactions
├── src/index.css    # Theme tokens and global styles
└── vite.config.ts   # Vite and production build configuration
```

Product imagery is sourced from public Unsplash URLs. An internet connection is required for remote imagery to render.

## Deployment

The project includes Vercel configuration for the static production build:

```bash
vercel deploy --prod
```

The deployed storefront is available at [aura-scent-site.vercel.app](https://aura-scent-site.vercel.app).

## License

This project is released under the MIT License.