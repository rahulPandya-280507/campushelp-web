# CampusHelp Web — Academic Demo

A React + Vite single-page web app based on the CampusHelp C++ mini-project presentation.

## Features
- Student overview dashboard and demo complaint metrics
- Issue submission with categories and priority assignment
- Generated complaint IDs and tracking progress
- Admin panel to update report status
- Fictional Greenfield University campus map
- Dijkstra shortest-path routing over a weighted campus graph
- Browser Geolocation API permission flow for live GPS coordinates
- Simulated campus location so the map can be demonstrated without GPS
- Responsive layout for desktop and mobile
- Browser-local persistence with `localStorage`

## Requirements
- Node.js 20+ recommended
- npm

## Run locally
```bash
npm install
npm run dev
```
Open the local URL Vite prints (usually http://localhost:5173).

## Production build
```bash
npm run build
npm run preview
```

## Tech stack
- **React**: builds the interface from reusable components and manages UI state.
- **Vite**: development server and production bundler.
- **JavaScript**: application logic, complaint handling, priority rules, and Dijkstra's algorithm.
- **CSS**: responsive layout and visual design.
- **SVG**: the fictional campus map, drawn locally without a paid map service.
- **Browser Geolocation API**: asks the user for permission to read latitude/longitude.
- **localStorage**: stores demo reports in the current browser. This is not a production database.

## Important demo boundaries
- The campus and its map coordinates are invented for the academic demo.
- Real GPS coordinates cannot be truthfully plotted onto the invented campus map. The app displays GPS coordinates and separately provides a simulated campus position for route demonstrations.
- Reports are stored only in the current browser. There is no backend, real admin authentication, multi-user sync, push notification, or actual emergency dispatch.
- Browser geolocation generally requires HTTPS or localhost and the user's permission.
- The displayed route distance uses fictional map units, not metres.

## Architecture in one line
React UI → application state and business rules → Dijkstra / priority logic → localStorage persistence.

## Main code
- `src/main.jsx`: data, UI, Dijkstra, geolocation, report creation/tracking/admin updates.
- `src/styles.css`: responsive interface styling.
- `index.html`: app entry point and metadata.
