<div align="center">

# Netflix Clone

[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=111)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-4.6-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-3-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-State-764ABC?logo=redux&logoColor=white)](https://redux-toolkit.js.org/)

A Netflix inspired streaming UI with TMDB browsing, genre rows, detail modals, and a custom video player screen.

[Live site](https://netflix-ranjansharma.vercel.app/) | [GitHub repo](https://github.com/Konseptt/netflix-clone)

</div>

## Why I built this

I built this to practice a more complete streaming interface in TypeScript. The project has real route loaders, RTK Query data fetching, a modal provider, genre browsing, animated hover cards, and a watch page built around Video.js.

It helped me understand how many small pieces go into an interface that looks effortless.

## Preview

![Netflix clone home page](public/assets/home-page.png)

## What it includes

- Home page with hero media and genre sliders
- TMDB data fetching with Redux Toolkit Query
- Detail modal with trailer playback, metadata, and similar videos
- Genre explore page with infinite style grids
- Watch page with Video.js controls and seekbar UI
- Responsive Material UI layout
- Framer Motion transitions

## Live website flow

```mermaid
flowchart TD
  A[Visitor opens live app] --> B[Router loads main layout]
  B --> C[Home loader fetches genres]
  C --> D[Hero section requests featured media]
  D --> E[Slider rows request titles by genre]
  E --> F{Visitor action}
  F -->|Hover| G[Preview card]
  F -->|More info| H[Detail modal]
  F -->|Play| I[Watch page]
  H --> J[Similar video cards and trailer]
  I --> K[Video.js player controls]
```

## Architecture diagram

```mermaid
flowchart LR
  A[src/routes] --> B[Pages]
  B --> C[Components]
  C --> D[DetailModalProvider]
  C --> E[PortalProvider]
  B --> F[Redux store]
  F --> G[RTK Query slices]
  G --> H[TMDB API]
  C --> I[Video.js player]
```

## Tech stack

| Area | Tools |
|---|---|
| App | React, TypeScript, Vite |
| UI | Material UI, Framer Motion, React Slick |
| Data | Redux Toolkit, RTK Query, TMDB |
| Video | Video.js, videojs-youtube |
| Routing | React Router |

## Run locally

```bash
npm install
npm run dev
```

Build for production:

```bash
npm run build
```

Preview the build:

```bash
npm run preview
```

## Notes

This is a learning clone. The UI is inspired by Netflix, but the project is mainly about practicing API-driven browsing, TypeScript components, global modal state, and media playback.
