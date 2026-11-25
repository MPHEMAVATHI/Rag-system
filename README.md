# Lung cancer staging RAG assistant

## Run in GitHub Codespaces

1. Push this repo to GitHub, then **Code → Codespaces → Create codespace on main**.
   Dependencies install automatically (takes a few minutes).
2. Edit `.env` (created from `.env.example`) and set `GROQ_API_KEY` and `NCBI_EMAIL`.
3. Build the knowledge base (one time, needs internet):
   ```bash
   python src/fetch_pubmed.py
   python src/build_index.py
   ```
4. Start the app:
   ```bash
   streamlit run src/app.py
   ```
   Codespaces will pop up the forwarded port 8501 — open it in the browser.

Terminal demo:
```bash
python src/main.py --ct "4.5 cm spiculated mass in left lower lobe, no lymph node involvement, no distant metastasis" --cea 12.4
```

> `data/pubmed_raw.json` and `index/` are git-ignored, so they must be built in each new codespace (step 3).
