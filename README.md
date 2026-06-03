# Avengers AI — Assemble

A fan-made educational multi-agent AI command-center website. It includes a cinematic intro, browser-generated synthetic voice narration, agent selection, a mock multi-agent mission workflow, a responsive dashboard, and a FastAPI backend.

> Fan-made educational project. Not affiliated with Marvel Studios.

## Safety and copyright note

The project uses character names for a personal educational demo. It does not include Marvel logos, actor images, movie clips, movie audio, or actor voice cloning. For a commercial product, replace the names with original characters.

## Run the backend first

Open a terminal inside the `backend` folder:

```bash
cd backend
python -m venv venv
```

Windows PowerShell:

```bash
venv\Scripts\Activate.ps1
```

Windows Command Prompt:

```bash
venv\Scripts\activate
```

Install and run:

```bash
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

API health check: open `http://localhost:8000/api/health`.

## Run the frontend

Open a second terminal:

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173`.

## Features

- Cinematic boot sequence and reactor animation
- “Avengers, assemble” browser synthetic narration
- Eight agent introductions
- Skip intro and replay intro
- Voice mute/unmute preference stored in localStorage
- Responsive Avengers command-center UI
- Select one or more agents, or assemble all agents
- Working mock FastAPI mission orchestration
- Automatic offline mock fallback when backend is not running
- Copy final report button

## Change agent names, lines, and roles

Edit:

```text
frontend/src/data.ts
backend/app/main.py
```

## Connect a real AI model later

Keep API keys in `backend/.env`, never inside frontend files. Replace the mock contribution logic inside `backend/app/main.py` with server-side provider calls. Add streaming later with Server-Sent Events or WebSockets.

## Production note

Before public commercial deployment, use original superhero-style character names and original visual identity.
