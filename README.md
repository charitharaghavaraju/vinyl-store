# Spiral Sounds 🎵

An online store for classic vinyl records, built with Express and SQLite. Browse the catalog by genre or search, create an account, and manage a shopping cart — all backed by a session-based auth system.

## Features

- **Product catalog** — browse all records, filter by genre, or search by title/artist/genre
- **Authentication** — register and log in with hashed passwords (bcrypt), session-based auth via cookies
- **Cart** — add items, view cart contents and running count, remove individual items or clear the cart (protected routes, per-user)
- **Static frontend** — plain HTML/CSS/JS served from `public/`

## Tech Stack

- [Express](https://expressjs.com/) — server and routing
- [SQLite](https://www.sqlite.org/) via `sqlite` / `sqlite3` — data storage
- [express-session](https://github.com/expressjs/session) — session management
- [bcryptjs](https://github.com/dcodeIO/bcrypt.js) — password hashing
- [validator](https://github.com/validatorjs/validator.js) — input validation

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18+ recommended)

### Installation

```bash
git clone <your-repo-url>
cd vinyl-store
npm install
```

### Running the app

```bash
npm start
```

The server runs at [http://localhost:8000](http://localhost:8000).

### Environment variables

| Variable                 | Description                          | Default                    |
|---------------------------|--------------------------------------|-----------------------------|
| `SPIRAL_SESSION_SECRET`  | Secret used to sign session cookies  | `jellyfish-baskingshark`   |

Set a strong, unique `SPIRAL_SESSION_SECRET` in production.

## Project Structure

```
├── controllers/     # Route handler logic (auth, cart, products, me)
├── db/              # SQLite connection helper
├── middleware/       # requireAuth session guard
├── public/           # Static frontend (HTML, CSS, JS, images)
├── routes/            # Express routers
├── database.db       # SQLite database file
└── server.js          # App entry point
```


