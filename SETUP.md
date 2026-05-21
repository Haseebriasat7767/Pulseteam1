# PulseTeam Setup Guide

## Prerequisites
- Node.js 16+ (you have it)
- Terminal access
- Browser (any modern one)

## Setup steps

### 1. Navigate to project
```bash
cd /data/.openclaw/workspace/pulseteam
```

### 2. Start backend
```bash
node backend/src/server.js
```
Watch for:
```
✓ PulseTeam backend running on http://localhost:4000
```

### 3. Open frontend
In a new terminal or directly:
```bash
# macOS
open frontend/dashboard.html

# Linux
xdg-open frontend/dashboard.html

# Windows
start frontend/dashboard.html
```

### 4. Test the app
- Click role buttons to switch views
- Check that data loads
- Open DevTools (F12) to see API calls

### 5. Verify API
```bash
curl http://localhost:4000/health
# Should return: {"ok":true,"service":"pulseteam-backend",...}
```

## What works
- ✓ Dashboard UI
- ✓ Role-based views
- ✓ API endpoints
- ✓ Data persistence
- ✓ Real-time updates

## What's not in MVP
- ✗ Database (uses file-based)
- ✗ Real auth (header-based)
- ✗ Integrations (stubs only)
- ✗ Production deployment
- ✗ Error handling

## Troubleshooting

### Backend won't start
```bash
# Check if port 4000 is in use
lsof -i :4000
# Kill it if needed
kill -9 <PID>
```

### Frontend doesn't load data
- Check backend is running on http://localhost:4000
- Open DevTools (F12) and check Network tab
- Look for CORS errors

### Port already in use
Edit `backend/src/server.js` and change port

## Next steps
- Deploy to Heroku/Railway/Vercel
- Add PostgreSQL
- Implement real auth
- Add Slack integrations

## Support
Check the docs folder for architecture, selling guide, and product spec.
