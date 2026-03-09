# Elastic Embedding POC

A simple two-page Flask website with a persistent left-side navigation sidebar.

## Pages

- **Home** (`/`) — contains a link to the TNF page.
- **TNF** (`/tnf`) — embeds the TNF ElasticSuite staging site in a full-page iframe.

## Prerequisites

- Python 3.x installed and available on your PATH.

## Setup & Running

1. **Clone / navigate to the project folder:**
   ```
   cd c:\repos\elastic_embeding_poc
   ```

2. **Create and activate a virtual environment** (first time only):
   ```
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```
   pip install flask pyopenssl
   ```

4. **Start the development server:**
   ```
   python app.py
   ```

5. **Open your browser** and go to:
   ```
   http://127.0.0.1:5000
   ```

## Subsequent Runs

After the first setup, just activate the venv and run the app:

```
cd c:\repos\elastic_embeding_poc
.venv\Scripts\activate
python app.py
```

## Notes

- The app runs in Flask's debug mode by default — it will auto-reload when you save changes to Python files.
- Whether the TNF iframe loads depends on the `X-Frame-Options` / `Content-Security-Policy` headers set by `tnf.staging.elasticsuite.com`. If the site blocks embedding, the iframe will appear blank.
