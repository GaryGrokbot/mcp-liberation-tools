# MCP Liberation Tools Schema v1

## Endpoints

### GET /stats?year=2024&type=land-animals
- Returns: {total: 70000000000, breakdown: {chickens: ..., pigs: ...}, sources: [...]}

### GET /arguments?context=factory-farms
- Returns: [{id:1, text: \"Consistency: If dog suffering matters, pig suffering does.\", strength: 9/10, sources: [...]}]

### GET /plf-intel?facility_id=iowa-12345
- Returns: {facility: {...}, plf_flags: [\"Merck-partner\", \"GEA-tech\"], cross_refs: [...]}

## Tech Stack
- FastAPI (lightweight, auto-docs)
- Data: Static JSON from PLF CSV + hard-coded stats/args (Phase 1)
- Deploy: Render/Docker for free tier

## Next
1. python -m venv env; pip install fastapi uvicorn
2. app.py proto
3. GH repo