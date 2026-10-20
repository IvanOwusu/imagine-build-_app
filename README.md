# Imagine Build

AI-assisted architectural concept exploration. Generated designs, floor plans and cost estimates are preliminary and must be reviewed by qualified professionals before construction.

## Requirements
- Node.js 20+
- A Gemini API key from Google AI Studio
- Vercel CLI for local API testing (npx vercel dev)

## Setup
1. Install dependencies: npm install
2. Configure GEMINI_API_KEY as a server-side environment variable in Vercel. Never place it in Vite define, a VITE_* variable, or browser code.
3. Run locally with npx vercel dev so /api/gemini runs with the frontend. Plain npm run dev only starts Vite and will not serve the API function.
4. Deploy to Vercel and set GEMINI_API_KEY in Project Settings → Environment Variables.

## Security and limitations
- Rotate any API key that was previously committed or exposed.
- .env* files are ignored; do not commit actual secrets.
- The API validates image uploads and applies a basic in-memory rate limit. Add durable rate limiting and authentication/abuse controls before public production launch.
- AI-generated images, plans and cost figures are concepts, not construction-ready documentation or professional estimates.
