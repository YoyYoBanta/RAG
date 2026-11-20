# AGENTS.md — Mutual Fund FAQ Assistant (facts-only RAG)

Start here. Read these before changing code:

1. `problemstatement.md` (also `problemstatement.txt`) — the brief: facts only, no investment advice, one source link per answer
2. `architecture.md` — pipeline design
3. `implementation-plan.md` — build phases
4. `edge-case.md` and `eval.md` — guardrails and how answers are checked
5. `task.md` — task checklist (update it as work is completed)

Pipeline: `scraper.py` → `chunker.py` → `embedder.py` → `ingest.py` (Chroma) → `retriever.py` + `guardrails.py` → `api.py` / `app.py`.
