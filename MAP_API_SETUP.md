# Map API setup

This project uses **Leaflet + React-Leaflet** and supports a real **Mapbox Dark map API**.

## 1. Create a Mapbox access token
Create an account at Mapbox and create a public access token from your account dashboard.

## 2. Add the token
Create a file named `.env.local` in this folder:

```env
VITE_MAPBOX_TOKEN=YOUR_MAPBOX_PUBLIC_TOKEN
VITE_API_BASE_URL=http://localhost:8000/api
VITE_USE_MOCK=true
```

Do not commit a secret/private token. A browser map token is public by design, so restrict it to your domains in Mapbox when you deploy.

## 3. Install and run

```bash
npm install
npm run dev
```

Open the Vite URL shown in the terminal (normally http://localhost:5173).

## 4. If you don't add a Mapbox token
The project automatically uses a free CARTO dark basemap, so the map still works.

## What is already connected
- Mapbox Dark v11 raster tiles when `VITE_MAPBOX_TOKEN` is present.
- CARTO fallback when the token is missing or Mapbox tiles fail.
- Leaflet zoom controls.
- Spill polygon and origin.
- Backtrack and forecast paths.
- Satellite footprint.
- AIS vessel markers and tracks.
- Clicking a vessel centers the map.
- Layer on/off controls.

The map location is initially centered on the demo Arabian Sea scenario at approximately 20.41° N, 65.82° E.
