# SmartPriceCompare

SmartPriceCompare is a responsive React and TypeScript price-comparison web application for browsing products across electronics categories and comparing prices from multiple e-commerce platforms.

> The project uses demonstration/mock product data stored in the app. It does not currently call live retailer APIs or perform real-time web scraping.

## Features

- Search products by name, brand, category, or specifications
- Filter products by category, brand, price range, rating, and offer type
- Sort products by best match, lowest/highest price, rating, or discount
- Quick category tabs for common product groups
- Compare up to four products side by side
- View platform prices and available offers
- Display mock 30-day price-history charts
- Responsive desktop and mobile layouts
- Accessible UI components built with Radix UI and shadcn/ui

## Technology Stack

- React 18
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- Radix UI
- React Router
- TanStack React Query
- Recharts
- Lucide React
- ESLint

## Project Structure

```text
smartprice-compare-main/
├── public/                 # Static public assets
├── src/
│   ├── components/         # Application and reusable UI components
│   ├── data/               # Mock product and price data
│   ├── hooks/              # Custom React hooks
│   ├── lib/                # Shared utility functions
│   ├── pages/              # Route-level pages
│   ├── types/              # TypeScript interfaces and types
│   ├── App.tsx             # Application routes and providers
│   ├── main.tsx            # React entry point
│   └── index.css           # Global styles
├── package.json            # Scripts and dependencies
├── vite.config.ts          # Vite configuration
└── tailwind.config.ts      # Tailwind configuration
```

## Getting Started

### Requirements

- Node.js 18 or newer
- npm (included with Node.js)

### Installation

```bash
npm install
```

### Run the Development Server

```bash
npm run dev
```

Open the local URL printed by Vite, usually <http://localhost:5173>.

### Create a Production Build

```bash
npm run build
```

The generated production files are written to the `dist` directory.

### Preview the Production Build

```bash
npm run preview
```

### Run Lint Checks

```bash
npm run lint
```

## Available Scripts

| Script | Description |
| --- | --- |
| `npm run dev` | Starts the Vite development server |
| `npm run build` | Builds the app for production |
| `npm run build:dev` | Builds using development mode |
| `npm run preview` | Locally previews the production build |
| `npm run lint` | Runs ESLint checks |

## Data Sources

Product records and platform prices are defined in `src/data/products.ts`. Type definitions are located in `src/types/product.ts`.

For a production deployment, replace the mock data with a trusted source, such as:

- Official retailer APIs
- Authorized affiliate feeds
- A maintained price-tracking backend

Live retailer names and URLs are links to search or product pages; the application does not verify current inventory or prices.

## Deployment

Build the project and deploy the contents of `dist` to a static hosting service such as Vercel, Netlify, GitHub Pages, or Azure Static Web Apps.

For a root deployment:

```bash
npm run build
```

Configure the host to serve `index.html` for route fallbacks if client-side routing is added beyond `/`.

## Notes

- The price-history chart uses generated mock variation data.
- Product images are loaded from remote Unsplash URLs and require internet access.
- External retailer links open retailer search or product pages.
