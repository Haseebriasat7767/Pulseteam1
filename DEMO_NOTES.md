# PulseTeam Demo Notes

## Before the demo
- [ ] Backend running: `node backend/src/server.js`
- [ ] Frontend open: `open frontend/dashboard.html`
- [ ] API responding: curl http://localhost:4000/health
- [ ] Data loads: check Network tab in DevTools
- [ ] Internet connection (for CORS if needed)

## During the demo (5-10 minutes)

### Opening (1 min)
"This is PulseTeam. Privacy-first team wellness for remote teams."
- Point to dashboard
- Explain: helps spot burnout without surveillance

### Dashboard walkthrough (2 min)
- Show the 4 cards (wellness, teams, nudges, at risk)
- Explain data is live from API
- Show team health table

### Role switching (2 min)
1. Click "Employee"
   - "Employee sees aggregate data only"
2. Click "Manager"
   - "Manager sees team-level insights"
3. Click "Admin"
   - "Admin sees everything"
- Point out the difference in detail

### Privacy panel (1 min)
- "No message content"
- "No keystroke tracking"
- "Aggregate by team"
- "Opt-in nudges"

### Code tour (2-3 min)
- Open VSCode or terminal
- Show backend/src/server.js
- Point to API endpoints (10 lines, clear)
- Show data persistence (db.js)
- Show auth logic (auth.js)

### Closing (1 min)
"This is a solid foundation. Next owner can:
- Deploy to cloud
- Add real database
- Build integrations
- Start selling"

## Q&A talking points
- **"Why file-based DB?"** → "It's an MVP. Real owner will migrate to PostgreSQL."
- **"How do you get data?"** → "Slack/Google integrations are placeholders for now."
- **"Is this production-ready?"** → "It's MVP-ready. Production is the buyer's job."
- **"Can you sell this?"** → "Yes. It's a solid prototype."
- **"How long to launch?"** → "2-4 weeks for a buyer to go live."

## After the demo
- Ask: "Questions?"
- Share: repo access (if agreed)
- Next: "Let's discuss the handoff process"
- Close: "I think this is a great foundation for you."
