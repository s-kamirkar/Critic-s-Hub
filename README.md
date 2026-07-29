# 🎬 Critic's Hub — Movie Discovery Web App

A responsive movie discovery web application that fetches and displays real-time data from [The Movie Database (TMDB)](https://www.themoviedb.org/) API. Built with vanilla JavaScript — no frameworks, no build tools.

**Live Demo:** [critic-s-hub.vercel.app](https://critic-s-hub.vercel.app/)

---

## Features

- **Real-time search** across TMDB's catalog of 500,000+ movie titles
- **Color-coded rating system** — instantly see how a movie is rated:
  - 🟢 Green: rating ≥ 8
  - 🟠 Orange: rating ≥ 5
  - 🔴 Red: rating < 5
- **Hover-to-reveal overview** — hover over any movie card to see its synopsis
- **Fully responsive grid layout** — adapts across 5 breakpoints, from a 5-column desktop grid down to a single-column mobile view
- **Popularity-sorted homepage** — displays trending/popular movies by default on load

---

## Tech Stack

- **HTML5** — semantic page structure
- **CSS3** — custom properties (CSS variables), CSS Grid, media queries, transitions
- **Vanilla JavaScript (ES6+)** — `async`/`await`, Fetch API, DOM manipulation
- **TMDB API** — movie data source

No frontend framework (React, Vue, etc.) was used — all rendering is done via direct DOM manipulation.

---

## How It Works

1. On page load, the app calls the TMDB `discover/movie` endpoint (sorted by popularity) and renders the results as a grid of movie cards.
2. Each card shows the poster, title, and a color-coded rating badge based on `vote_average`.
3. Hovering over a card reveals the movie's overview/synopsis in an animated overlay.
4. Typing a query into the search bar and submitting the form calls TMDB's `search/movie` endpoint instead, replacing the grid with matching results.

---

## Project Structure

```
├── index.html      # Page markup: header/search form + main content container
├── style.css       # Styling, responsive grid, hover animations
├── script.js       # Fetch logic, rendering, search handling
```

---



## Possible Future Improvements

- Move the TMDB API key server-side via a serverless function (e.g., Vercel/Netlify function) to eliminate the exposed-key issue
- Add `try/catch` error handling with a user-facing error message
- Add a loading indicator during fetch calls
- Replace hover-triggered overview with a tap/click-triggered modal for touch device support
- Add pagination or infinite scroll for search results

---

## Author

**Sana Kamirkar**
[GitHub](https://github.com/s-kamirkar) · [LinkedIn](https://www.linkedin.com/in/sanakamirkar/)
