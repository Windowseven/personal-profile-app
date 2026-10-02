# Personal Profile App

A personal profile application built with Express: a few plain-text routes plus a JSON API.

Built for the freeCodeCamp course *Build a Personal Profile App*
(Back-End Development and APIs certification).

## Setup

```bash
npm install
npm start
```

The server listens on port `3000` (override with `PORT`).

## Routes

| Method | Path | Response |
| --- | --- | --- |
| GET | `/` | `Welcome to Camper Bot's homepage!` |
| GET | `/hobbies` | `I cycle, go boating, and play guitar.` |
| GET | `/skills` | `JavaScript, Node.js, and Express.js!` |
| GET | `/api/profile` | JSON profile object |

```bash
curl localhost:3000/
curl localhost:3000/api/profile
```

```json
{
  "name": "Camper Bot",
  "hobbies": ["cycling", "boating", "guitar"],
  "skills": ["JavaScript", "Node.js", "Express.js"]
}
```

The profile object is defined once at the top of `index.js` and reused by the JSON route,
so the text routes and the API stay in sync.