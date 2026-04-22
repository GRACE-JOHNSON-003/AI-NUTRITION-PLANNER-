
## AI Nutrition Planner (Hackathon Prototype)

AI-powered Nutrition Planner that:
- Calculates **BMI**
- Estimates **daily calories** (BMR + activity + goal)
- Uses an LLM to generate a **personalized meal plan**
- Extracts **macros** (protein/carbs/fats)
- Shows **practical health tips**

### Tech
- **Frontend**: React + Vite + TypeScript
- **Backend**: Node.js + Express + TypeScript
- **Validation**: Zod
- **LLM**: OpenAI-compatible Chat Completions (works with OpenAI and many gateways)

### Monorepo layout
- `backend/`: Clean-ish architecture (domain/use-cases/adapters/infrastructure)
- `frontend/`: Minimal, responsive UI

### Setup

#### 1) Backend
```bash
cd backend
cp .env.example .env
npm install
npm run dev
```

#### 2) Frontend
```bash
cd frontend
npm install
npm run dev
```

Then open the frontend URL and submit the form.

### Environment variables (backend)
Create `backend/.env`:
- `PORT=8080`
- `LLM_PROVIDER=openai` (default)
- `OPENAI_API_KEY=...`
- `OPENAI_BASE_URL=https://api.openai.com/v1` (optional)
- `OPENAI_MODEL=gpt-4o-mini` (optional)

If no API key is set, the backend returns a **safe mocked plan** so the UI still works for demos.

### Notes
- No medical advice is given; output is realistic and non-extreme.
- This is a prototype optimized for hackathons; you can extend storage/auth later.

