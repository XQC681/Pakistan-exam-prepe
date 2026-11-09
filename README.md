# 📚 Imtihan Saathi – AI Exam Prep for Pakistan Matric & Inter Students

Upload a chapter from **your own textbook** and get:

- Practice questions (MCQs, short and long) made only from that chapter
- Your answers checked against the chapter text
- Feedback and explanations in **English, Urdu (اردو) or Roman Urdu**
- A score, plus the exact line from the chapter that supports each answer

Powered by Google's Gemini Flash model and built with Streamlit.

## Features

- Works for Matric (Class 9 and 10) and Intermediate (Class 11 and 12)
- Upload a **PDF**, **photos of book pages** (PNG/JPG/WEBP) or a **.txt** file, or paste text directly
- Scanned or Urdu-script books are read with AI (tick the checkbox in the app)
- MCQs are marked by the app itself, so the score does not depend on the AI's arithmetic
- Written answers are marked against the chapter: Correct, Partially correct, Incorrect or Not attempted
- Urdu text is shown right-to-left in an Urdu font

## Files

| File | Purpose |
|---|---|
| `app.py` | The whole app |
| `requirements.txt` | Python packages |
| `README.md` | This guide |

## Run on your computer

1. Install Python 3.10 or newer.
2. Get a free Gemini API key at https://aistudio.google.com/apikey
3. In a terminal, inside the project folder:

```bash
pip install -r requirements.txt
streamlit run app.py
```

4. Paste your API key in the sidebar, or create `.streamlit/secrets.toml`:

```toml
GEMINI_API_KEY = "your-key-here"
```

> ⚠️ Never upload `secrets.toml` or your key to GitHub.

Optional: set `GEMINI_MODEL` (in secrets or as an environment variable) to use a different Gemini Flash model. The default is `gemini-2.5-flash`.

## Put the code on GitHub (using the website, no Git needed)

1. Sign in at https://github.com and click **+ → New repository**.
2. Name it (e.g. `imtihan-saathi`), choose **Public**, click **Create repository**.
3. On the new repo page click **uploading an existing file**.
4. Drag in `app.py`, `requirements.txt` and `README.md` (the files themselves, not a folder).
5. Click **Commit changes**.

To update later: open a file in the repo → ✏️ edit icon → paste the new code → **Commit changes**. Streamlit redeploys automatically.

## Deploy on Streamlit Community Cloud

1. Go to https://share.streamlit.io and sign in with GitHub.
2. Click **Create app → Deploy a public app from GitHub**.
3. Pick your repository, branch `main`, and main file path `app.py`.
4. Open **Advanced settings → Secrets** and add:

```toml
GEMINI_API_KEY = "your-key-here"
```

5. Click **Deploy**. After a minute or two you get a public link to share.

**About the key:** if you add your key as a secret, everyone using your app shares your free quota. If you leave the secret out, each student pastes their own free key in the sidebar.

## Tips for best results

- Use **one chapter at a time** (the app reads up to 60,000 characters).
- Check the text box after uploading. If the extracted text looks wrong (common with Urdu PDFs), tick the AI-reading option or paste the text.
- Answers are judged against your chapter. AI can still make mistakes, so confirm important points with your textbook or teacher.

## Limits

- Free Gemini keys have rate and daily limits. If you see "usage limit reached", wait a minute and try again.
- PDFs and photos sent for AI reading must be under 18 MB each.
