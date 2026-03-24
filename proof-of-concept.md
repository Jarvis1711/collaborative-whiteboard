# Proof of Concept - Collaborative Whiteboard

## Scope
- App category: Real-Time SaaS
- Entity model: Collaborative Whiteboard Session
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Channel/Room: `channel_name` (text)
- Participants: `participant_count` (number)
- Latency Target (ms): `latency_target_ms` (number)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"live","payload":{"channel_name":"Demo value","participant_count":12,"latency_target_ms":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 18
- Generated UTC: 2026-03-24T15:52:21.858474+00:00
- Status: Phase-2 complete
