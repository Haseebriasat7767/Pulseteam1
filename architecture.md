# PulseTeam Architecture

## Overview
- Frontend: Static HTML + JavaScript
- Backend: Node.js HTTP server
- Persistence: File-based JSON (`data.json`)
- Auth: Header-based role assignment (MVP)

## Frontend
- `frontend/index.html` — basic dashboard
- `frontend/dashboard.html` — full dashboard
- Fetches from backend via REST API
- Role switching via buttons

## Backend
- `backend/src/server.js` — main server
- `backend/src/db.js` — file persistence
- `backend/src/auth.js` — role checks
- `backend/src/routes.js` — business logic
- Listens on `http://localhost:4000`

## Data model

### Users
```js
{ id, name, role, teamId }
```

### Teams
```js
{ id, name, riskScore, notes }
```

### Nudges
```js
{ id, teamId, text, sent }
```

## Auth model
Role-based (employee, manager, admin):
- Employee: sees own wellness data only
- Manager: sees team data
- Admin: sees all data

## Future improvements
1. Real database (PostgreSQL)
2. JWT auth
3. Integration services
4. Real analytics engine
5. Deployment to cloud
