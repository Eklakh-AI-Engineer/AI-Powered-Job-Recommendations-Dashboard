# AI-Powered Job Recommendations Dashboard

> **A Streamlit prototype that ranks remote job listings against uploaded resume text using sentence embeddings.**

This project demonstrates a lightweight recommendation workflow:

```text
Resume PDF
   ↓
Text extraction
   ↓
Resume embedding
   ↓
Remote job feed
   ↓
Job-description embeddings
   ↓
Cosine similarity
   ↓
Top recommendations
   ↓
Country filtering + visualization
```

It is a **prototype recommendation dashboard**, not a production job-search platform or autonomous application agent.

## Current implementation

| Capability | Status |
|---|---|
| Streamlit dashboard | Implemented |
| PDF resume extraction | Implemented |
| Sentence-Transformer semantic matching | Implemented |
| Remote job feed integration | Implemented |
| Top-5 ranking | Implemented |
| Country filtering | Implemented |
| Related-job display | Implemented |
| Apply links | Implemented |
| Trend visualization | Demo-only; generated synthetic/random values |
| Continuous job monitoring | Not implemented |
| User accounts / persistence | Not implemented |
| Resume tailoring | Not implemented |
| Autonomous applications | Not implemented |
| Production evaluation benchmark | Not documented |

## Technology

- Python
- Streamlit
- Sentence Transformers
- all-MiniLM-L6-v2
- PyPDF2
- pandas
- scikit-learn
- Plotly
- Remotive remote-jobs API

## Quick start

```bash
git clone https://github.com/Eklakh-AI-Engineer/AI-Powered-Job-Recommendations-Dashboard.git
cd AI-Powered-Job-Recommendations-Dashboard

python -m venv venv
# Windows
venv\\Scripts\\activate
# Linux/macOS
source venv/bin/activate

pip install -r requirements.txt
streamlit run app.py
```

The application opens as a Streamlit web interface.

## Recommendation method

The current implementation:

1. extracts text from an uploaded PDF;
2. creates a resume embedding with Sentence Transformers;
3. fetches jobs from the configured remote-job feed;
4. embeds each job title + description;
5. calculates cosine similarity;
6. sorts jobs by similarity;
7. displays the top five recommendations.

The similarity score is a semantic ranking signal. It is **not** a probability of employment, eligibility score, or calibrated recommendation metric.

## Visualization limitation

The current country-specific trend chart uses generated values for demonstration. Those values are **not historical labor-market data** and must not be presented as real job-market trends.

## Repository structure

```text
AI-Powered-Job-Recommendations-Dashboard/
├── app.py
├── requirements.txt
├── frontend prototype assets / configuration
├── docs/
│   ├── README.md
│   ├── ARCHITECTURE.md
│   ├── DEVELOPMENT.md
│   ├── EVALUATION.md
│   └── history/
├── .gitignore
└── LICENSE
```

## Engineering notes

- Job-feed availability depends on the external API.
- Resume PDFs with image-only/scanned content may not yield extractable text.
- Semantic similarity should be evaluated on a labeled job/resume benchmark before making quantitative recommendation claims.
- API errors are surfaced in the Streamlit UI.
- No candidate data should be persisted without an explicit privacy design.

## Project status

This repository is best presented as a **supporting AI/ML project demonstrating semantic retrieval/ranking**, not as the autonomous job agent in the broader portfolio.

## License

MIT. See [LICENSE](LICENSE).
