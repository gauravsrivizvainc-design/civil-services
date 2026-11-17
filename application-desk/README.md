# Application Desk

Upload a CV and a job advert, get five application sections written from your own experience:
employment history, skills and experience, personal statement, STAR behaviour statements,
and technical and competency interview prep.

## Run it

It is one static file: `index.html`. No build step, no server code.

- Quick test: double-click `index.html`, or run `python3 -m http.server` in this folder.
- Publish: drag the folder onto Netlify Drop, or deploy it with Vercel, Cloudflare Pages
  or GitHub Pages. Any static host works.

## Use it

1. Open the page and paste your Anthropic API key (from console.anthropic.com) into the key box.
   It is kept for the browser tab only.
2. Add your CV and the advert (upload PDF, DOCX or TXT, or paste).
3. Choose Build my application.

Your CV text is remembered in that browser (localStorage) for the next advert. Use Clear to remove it.

## Important

- The key is typed in by each person and sent straight from their browser to api.anthropic.com.
  Never put your own key into the file if the page is public.
- If you want to share this with other people without them needing a key, add a small backend that
  holds the key and forwards requests, then change the fetch call in the shim near the bottom of
  `index.html`.
- PDF and DOCX reading loads pdf.js and mammoth from cdnjs, and fonts load from Google Fonts,
  so the page needs internet access.
- Model names are set in the Model dropdown and the shim. Update them if Anthropic retires one.
