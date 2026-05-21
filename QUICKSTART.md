# PulseTeam MVP — Quick Start

## What is PulseTeam?
Privacy-first remote team monitoring and wellness SaaS.

## What's included
- Interactive dashboard (frontend)
- REST API backend
- Role-based access (employee, manager, admin)
- File-based persistence
- Privacy-first design

## Run it

### Terminal 1: Start backend
```bash
node backend/src/server.js
```
You should see:
```
✓ PulseTeam backend running on http://localhost:4000
```

### Terminal 2: Open frontend
```bash
open frontend/index.html
# or
open frontend/dashboard.html
```

## How to use

1. **Role switching**: Click Employee/Manager/Admin buttons
2. **See different views** based on your role
3. **Open DevTools** to see API calls
4. **Check endpoints**: `http://localhost:4000/api/summary`

## API endpoints

- `/health` — status
- `/api/me` — current user info
- `/api/summary` — dashboard summary
- `/api/team-health` — team data (role-aware)
- `/api/teams` — teams list
- `/api/nudges` — wellness nudges
- `/api/privacy` — privacy policy
- `/api/integrations` — integration status
- `/api/export` — export all data

## Data storage
File: `data.json` (created automatically)

## Next steps
- Add real database (PostgreSQL)
- Implement full auth
- Add Slack/Google integrations
- Deploy to production

## Notes
- Backend runs on `http://localhost:4000`
- Frontend uses CORS to fetch from backend
- Role-based views work via `x-role` header
- Data persists in `data.json`
