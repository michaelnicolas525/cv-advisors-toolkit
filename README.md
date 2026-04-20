# CV Advisors — Client Analysis Toolkit

AI-powered wealth management intake tool. Enter client data, get a full analysis in under 60 seconds.

---

## Setup in Cursor

### 1. Install dependencies
Open the terminal in Cursor and run:
```
npm install
```

### 2. Add your API key
Duplicate `.env.example` and rename it `.env`:
```
cp .env.example .env
```
Open `.env` and replace `your_api_key_here` with your Anthropic API key.
Get one at: https://console.anthropic.com/

### 3. Run the app
```
npm start
```
Then open http://localhost:3000 in your browser.

### 4. For live reload during development
```
npm run dev
```

---

## Deploy to Vercel (share with others)

1. Push to GitHub
2. Go to vercel.com → Import your repo
3. Add `ANTHROPIC_API_KEY` as an environment variable
4. Deploy — you get a live URL instantly

---

## Project Structure

```
cv-advisors-toolkit/
├── server.js          # Express server + Anthropic API proxy
├── public/
│   └── index.html     # Full frontend (intake form + analysis output)
├── package.json
├── .env               # Your API key (never commit this)
└── .env.example       # Template for the .env file
```

---

## What It Does

**Tab 1 — Client Intake**
Enter client name, age, risk profile, income targets, all three advisor relationships, and real estate assets.

**Tab 2 — Analysis Output**
Automatically generates:
- Net worth summary with stat cards
- ETF-by-ETF portfolio analysis with KEEP / REMOVE / REVIEW flags
- Income plan with full yield math
- Custodian comparison table
- Draft slide content ready to copy into PowerPoint