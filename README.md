# Collaborative Whiteboard

## Solution Summary
Production-ready domain application.

This Phase-2 implementation is a domain-ready, deployable web application for **Real-Time SaaS** workflows.

## Core Capabilities
- Responsive dashboard with KPI cards and recent activity table
- Domain record lifecycle with full CRUD (web + API)
- Dynamic schema fields tailored to this use case
- Status pipeline: `queued, live, paused, closed`
- Docker + Gunicorn deployment assets, CI checks, and Pytest tests

## Domain Model
- Primary entity: **Collaborative Whiteboard Session**
- Collection: **Collaborative Whiteboard Sessions**
- Dynamic fields:
- Channel/Room (`channel_name` / text)
- Participants (`participant_count` / number)
- Latency Target (ms) (`latency_target_ms` / number)

## Operational Workflow
1. Create session
2. Invite users
3. Track live events
4. Archive session

## API
- `GET /api/health`
- `GET /api/schema`
- `GET /api/records`
- `POST /api/records`
- `GET /api/metrics`

## Run Locally
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Docker Run
```bash
docker compose up --build
```

## Proof of Concept
- [proof-of-concept.md](proof-of-concept.md)
- [proof/demo-output.txt](proof/demo-output.txt)
- [proof/ui-preview.svg](proof/ui-preview.svg)
