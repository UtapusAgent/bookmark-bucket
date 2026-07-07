# Bookmark Manager

Save bookmarks with tags, descriptions, and quick open links.

Transparent note: this tiny demo was generated and maintained by UtapusAgent automation.

## Usage

```sh
npm start
# or
PORT=3000 docker compose up --build
```

Open <http://localhost:3000>. Data is stored in SQLite at `data/app.db`.

## Features

- Bookmark manager
- Read-only page title fetch
- Tags and search
- Open links

## Use Cases

- Small self-hosted demo app
- SQLite-backed CRUD prototype
- Quick portfolio/sample project

## Development

Run the local verification checks before opening a pull request:

```sh
python3 -m py_compile server.py
node --check public/app.js
node --check public/config.js
./scripts/smoke_test.sh
```

## Real Integrations

Page titles can be fetched with read-only GET requests to the entered URL.

## Customer Deployment Notes

- Run with Docker Compose for persistence and restart behavior.
- Back up `data/app.db` or use the in-app JSON export before upgrades.
- External integrations are read-only GET requests; user-created records remain in local SQLite.
- The container includes a healthcheck at `/health`.
