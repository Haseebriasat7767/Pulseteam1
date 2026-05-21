# PulseTeam API Reference

## Base URL
`http://localhost:4000`

## Authentication
Header: `x-role: [employee|manager|admin]`

## Endpoints

### Health check
```
GET /health
```
Response: `{ ok: true, service: "pulseteam-backend" }`

### Current user
```
GET /api/me
Headers: x-user-id: u1, x-role: manager
```
Response: `{ id, name, role, teamId }`

### Summary
```
GET /api/summary
```
Response: `{ employees, teams, nudges, highRiskTeams, averageWellness, status }`

### Team health
```
GET /api/team-health
```
Response: `{ teams: [...], canView: true, averageWellness: 72 }`

### Teams list
```
GET /api/teams
```
Response: `{ teams: [...], canView: true }`

### Nudges
```
GET /api/nudges
POST /api/nudges
Body: { teamId, text }
```

### Privacy policy
```
GET /api/privacy
```
Response: `{ rules: [...], dataExport: "supported", dataDelete: "supported" }`

### Integrations
```
GET /api/integrations
```
Response: `{ slack: {...}, google: {...}, status: "coming-soon" }`

### Export data
```
GET /api/export
```
Response: `{ exportedAt, data, format }`

## Role-based behavior

### Employee
- Can view personal nudges
- Cannot see team data
- Can view privacy settings

### Manager
- Can view team health
- Can see all team nudges
- Can view trends

### Admin
- Can see all data
- Can manage users
- Can manage integrations

## Error handling
```json
{ "error": "not_found", "path": "/api/unknown" }
```

## Status codes
- 200: Success
- 404: Not found
- 500: Server error
