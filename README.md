# data_capstone

Generate HTML/CSS from a screenshot or a text prompt, then optionally deploy the result to Vercel.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Copy the example env file and fill in your keys (optional):

```bash
cp .env_example .env
```

## Run

```bash
python app.py
```

Open: http://localhost:3000

## Usage

- Screenshot to HTML: upload a PNG/JPG/WEBP on the home page.
- Prompt to HTML: click “Generate UI HTML from prompt”.
- Edit and refine: use the prompt update on the results page.

## Vercel Deploy Options

### 1) Download zip (no token required)
- Click “Deploy to Vercel”.
- Unzip the bundle.
- Run:

```bash
npx vercel
# or
npx vercel --prod
```

### 2) Deploy via API (optional token flow)
- Paste a Vercel personal access token in the Deploy panel **or** set `VERCEL_TOKEN`.
- Optionally set a project name.
- Click “Deploy via API”.
- The app will return a deployment URL.

### API token creation

Create a personal access token in Vercel:
https://vercel.com/account/tokens

## Notes

- Tokens are used once per deploy and are not stored.
- Generated HTML is self-contained (no external assets).
- Max prompt length: 800 characters. Max image size: 10 MB.
