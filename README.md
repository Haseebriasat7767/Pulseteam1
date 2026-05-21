# PulseTeam

**Privacy-first remote team monitoring and wellness SaaS.**

Help remote teams spot burnout, overload, and disengagement — without surveillance.

## Quick start
```bash
# Terminal 1
node backend/src/server.js

# Terminal 2
open frontend/dashboard.html
```

## Features
- ✓ Employee wellness dashboard
- ✓ Manager team health overview
- ✓ Admin privacy controls
- ✓ Role-based access
- ✓ Privacy-first design
- ✓ Real-time data sync

## Architecture
- **Frontend**: HTML + JavaScript
- **Backend**: Node.js HTTP server
- **Persistence**: File-based JSON
- **Auth**: Header-based roles (MVP)

## Documentation
- [QUICKSTART.md](./QUICKSTART.md) — Run in 30 seconds
- [SETUP.md](./SETUP.md) — Detailed setup
- [API.md](./API.md) — API reference
- [docs/architecture.md](./docs/architecture.md) — System design
- [docs/product.md](./docs/product.md) — Product spec
- [docs/privacy.md](./docs/privacy.md) — Privacy policy
- [BUYER_MEMO.md](./BUYER_MEMO.md) — For acquisition

## What's working
- Dashboard UI with role switching
- API endpoints (health, summary, teams, nudges, privacy, integrations)
- Data persistence
- CORS-enabled

## What's next
- Real database (PostgreSQL)
- JWT authentication
- Slack/Google integrations
- Production deployment
- Customer onboarding

## Endpoints
- `GET /health` — status
- `GET /api/summary` — dashboard data
- `GET /api/team-health` — team details
- `GET /api/nudges` — wellness reminders
- `GET /api/privacy` — privacy policy
- `GET /api/integrations` — integration status
- `POST /api/nudges` — create nudge

## For buyers
This is a working MVP with clean code, solid architecture, and a clear path to customers.

See [BUYER_MEMO.md](./BUYER_MEMO.md) for details.

## License
MIT (or specify your license)

## Contact
[your name / email]
