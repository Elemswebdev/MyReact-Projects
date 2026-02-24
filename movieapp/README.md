# MovieApp

A React movie browsing application built with Vite and React Router.

This repository contains a single frontend app located in `movieapp/`.

## Project Description

MovieApp lets users:
- Browse popular movies from The Movie Database (TMDB)
- Search for movies by title
- Add and remove favorites
- Persist favorites in browser `localStorage`

The app is a client-side SPA using:
- React 19
- React Router DOM 7
- Vite (Rolldown build)
- Plain CSS modules per feature/page

## Repository Layout

- Root folder: workspace container
- App folder: `movieapp/`

## Prerequisites

- Node.js 18+ (recommended 20+)
- npm 9+

## Installation

From the repository root:

```bash
cd movieapp
npm install
```

## Run the App

```bash
npm run dev
```

Then open the local URL shown by Vite (usually `http://localhost:5173`).

## Available Scripts

Run these inside `movieapp/`:

- `npm run dev` - Start development server with HMR
- `npm run build` - Create production build
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint

## Usage Examples

### 1. Browse Popular Movies
1. Start the app with `npm run dev`.
2. Open the Home page (`/`).
3. Popular movies are fetched and displayed in a grid.

### 2. Search for a Movie
1. Type a title in the search box (for example: `Inception`).
2. Click **Search**.
3. Matching results replace the default popular list.

### 3. Manage Favorites
1. Click the heart button on any movie card to add/remove favorites.
2. Go to **Favorites** in the navbar (`/favorites`).
3. Favorites stay saved after refresh using `localStorage`.

## Project Structure

```text
movieapp/
  .gitignore
  eslint.config.js
  index.html
  package.json
  vite.config.js
  public/
    vite.svg
  src/
    App.jsx
    main.jsx
    assets/
      react.svg
    components.jsx/
      MovieCard.jsx
      NavBar.jsx
    context/
      MovieContext.jsx
    pages/
      Home.jsx
      Favorites.jsx
    services/
      api.js
    css/
      App.css
      Home.css
      Favorites.css
      MovieCard.css
      Navbar.css
      index.css
```

## Routing

- `/` -> Home page (popular/search movies)
- `/favorites` -> Favorites page

## Data Source

Movie data comes from TMDB API via `src/services/api.js`.

Current implementation uses a hardcoded API key in source. For production use, move the key to environment variables and avoid committing secrets.

## Notes

- Favorites are managed with React Context in `src/context/MovieContext.jsx`.
- No backend is required; all state is client-side.
