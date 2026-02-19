# Full Stack Todo Application


## What it does
- Create, edit, delete todos with title, description, due date.
- Create and delete categories; todos are grouped by category with counts.
- Mark todos complete/incomplete; filter by all/active/completed.
- Sort todos by created date or due date; pagination built in.
- Past-due dates are blocked; server validation returns clear errors.
- Light/dark toggle, error Snackbar, inline field validation.
- Light/dark toggle, error Snackbar, inline field validation.

## Tech Stack
- Backend: Node.js, Express, TypeScript (in-memory store).
- Frontend: React + Vite + TypeScript + MUI, Redux Toolkit.

## Local setup
1) Backend
   ```bash
   cd backend
   npm ci
   npm run dev        # runs on http://localhost:4000
   ```
2) Frontend
   ```bash
   cd frontend
   npm ci
   npm run dev        # opens http://localhost:5173/
   ```
   - API base defaults to `http://localhost:4000/api`. To override, set `VITE_API_BASE_URL` (include `/api`).
3) Build checks
   ```bash
   cd backend && npm run build
   cd ../frontend && npm run build
   ```

## Deploy
- Backend (Render/Railway): root `backend/`, build `npm ci && npm run build`, start `npm run start`, env `PORT=4000`. Copy the public URL, e.g. `https://your-api.onrender.com/api`.
- Frontend (GitHub Pages):
  - Set repo secret `VITE_API_BASE_URL` to the backend URL (with `/api`).
  - Workflow `frontend/.github/workflows/deploy-frontend.yml` builds and publishes `frontend/dist` on push to `master`.
  - Pages URL: `https://<username>.github.io/<repo>/todo-fullstack/` (base is set in `vite.config.ts`).

## Notes
- Data persists across refreshes while the backend process is running (in-memory). 

## To Use the hosted application:
- Open https://tejadesu0909.github.io/todo-fullstack/ (use a hard refresh if you previously opened an older build).

