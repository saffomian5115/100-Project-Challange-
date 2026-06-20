# AutoElite Motors — Car E-commerce Showcase

A single-page React car dealership showcase built with **Vite + React + React-Bootstrap**. Browse a catalog of premium cars, search by name/brand, and filter by fuel type — all powered by static, in-memory data (no backend required).

## Features

- 🚗 **Car Catalog** — Grid of cars rendered via a reusable `CarCard` component
- 🔍 **Live Search** — Search bar in the header filters cars by name, brand, or description
- ⛽ **Fuel Type Filter** — Quick filter buttons (All / Petrol / Electric / Hybrid, etc.)
- ❤️ **Favorites (demo)** — "Save This Car" button with a like animation (local UI state only)
- 📊 **Stats Footer** — Total cars, starting price, brand count, and latest model year
- 📱 **Responsive UI** — Built with React-Bootstrap grid and components

## Tech Stack

- **React 19** + **Vite 7**
- **react-bootstrap** + **bootstrap 5**
- ESLint (flat config) for linting

## Project Structure

```
021-Cars-Ecommerce/
├─ index.html
├─ package.json
├─ vite.config.js
├─ eslint.config.js
├─ public/
│  └─ vite.svg
└─ src/
   ├─ main.jsx
   ├─ App.jsx
   ├─ App.css
   ├─ index.css
   ├─ assets/
   │  └─ react.svg
   ├─ components/
   │  ├─ Header.jsx       # Logo, search bar, contact info
   │  ├─ CarCard.jsx       # Individual car listing card
   │  └─ Footer.jsx        # Contact & business hours
   └─ constants/
      └─ cars.js           # Static car catalog data
```

## Prerequisites

- **Node.js** v18+

## Setup & Run

```bash
cd 021-Cars-Ecommerce
npm install
npm run dev
```

The app will be available at **http://localhost:5173**.

### Other Scripts

```bash
npm run build     # Production build (outputs to dist/)
npm run preview   # Preview the production build locally
npm run lint      # Run ESLint
```

## Data

All car listings live in `src/constants/cars.js` as a static array — there is no database or API call. To add/edit cars, update that file directly (each entry includes `name`, `brand`, `price`, `year`, `mileage`, `fuelType`, `transmission`, `description`, and `image`).

## Notes

This is a front-end-only demo/portfolio project intended to showcase UI/UX patterns (search, filtering, card layouts) rather than a production e-commerce system — there's no checkout, persistence, or backend.
