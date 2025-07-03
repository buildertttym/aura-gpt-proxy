# AuraGPT OpenAI Proxy

A secure Node.js/Express proxy to keep your OpenAI API key safe and off your mobile app.

## Features
- Forwards requests to OpenAI's Chat Completions API
- Keeps your OpenAI API key secret (never exposed to the client)
- Easy to deploy (Vercel, Render, Railway, or your own server)

## Setup

1. **Clone or copy this folder.**
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Add your OpenAI API key:**
   - Copy `.env.example` to `.env` and fill in your real key:
     ```bash
     cp .env.example .env
     # Edit .env and set OPENAI_API_KEY=sk-...
     ```

## Local Development

```bash
npm run dev
```
- Proxy runs on http://localhost:3001/openai

## Usage (from your app)
- POST to `/openai` with the same JSON body you would send to OpenAI.
- Example endpoint: `http://localhost:3001/openai` (local) or your deployed URL.

## Deploy to Vercel
1. Push this folder to a GitHub repo (or use Vercel CLI).
2. Go to [vercel.com](https://vercel.com/) and import the repo.
3. Set the `OPENAI_API_KEY` environment variable in Vercel dashboard.
4. Deploy!

## Security
- Never commit your real `.env` file or API key to git.
- For production, consider adding rate limiting, authentication, or logging.

---
Questions? DM @yourname or open an issue. 