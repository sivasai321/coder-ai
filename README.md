# coder-ai


**1. Unzip and open**
```
File → Open Folder → select the oasis-coder folder
```

**2. Open the terminal** (`Ctrl+` `` ` ``) and run:
```bash
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # Mac/Linux

pip install -r requirements.txt
```

**3. Add your API key** — open `.env` and paste your Gemini key:
```
GEMINI_API_KEY=AIza...your key here
```
Get a free key at **aistudio.google.com/app/apikey**

**4. Run it:**
```bash
python app.py
```

Then open **http://localhost:5000** in your browser.

---

**What's in the project:**

- `app.py` — Flask backend, handles the PDF upload and Gemini API call with the full medical coding system prompt
- `templates/index.html` — the UI shell
- `static/css/style.css` — all styles
- `static/js/app.js` — drag-and-drop, form submission, result rendering
- `.env` — your API key (never commit this to Git)
- `README.md` — full setup guide

The backend does all the heavy lifting — the PDF never leaves your machine except to go to Gemini's API. When you're ready for production with real patient data, the README explains the Vertex AI switch for HIPAA compliance.
