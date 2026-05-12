# Bird Biology Sound Quiz

A simple web quiz for learning to identify 20 North American birds by their calls. Bird order is randomized each visit.

## Deploy to Vercel

This is a fully static site — no build step required.

### Option 1: One-click (recommended)
1. Push this repo to GitHub.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Leave all settings at default and click **Deploy**.

### Option 2: Vercel CLI
```bash
npm i -g vercel
vercel        # preview deploy
vercel --prod # production
```

## Run locally
Any static file server works:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
or
```bash
npx serve .
```

## Project structure
```
.
├── index.html      # The quiz
├── audio/          # 20 bird-call MP3s
├── vercel.json     # Long-cache headers for audio
└── README.md
```

## Adding a bird
1. Drop the MP3 into `audio/`.
2. Add an entry to the `BIRDS` array in `index.html`. The optional `aliases` field accepts alternate spellings.
