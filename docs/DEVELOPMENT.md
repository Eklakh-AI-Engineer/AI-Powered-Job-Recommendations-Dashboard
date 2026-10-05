# Development

## Environment

Use Python 3.8+ as documented by the original project, with the pinned requirements in requirements.txt.

```bash
python -m venv venv
# Windows
venv\\Scripts\\activate
# Linux/macOS
source venv/bin/activate

pip install -r requirements.txt
```

## Run

```bash
streamlit run app.py
```

## Dependencies

The prototype uses:

- Streamlit;
- pandas;
- requests;
- PyPDF2;
- sentence-transformers;
- scikit-learn;
- Plotly.

## Development rules

1. Keep external job-source behavior explicit.
2. Do not hard-code API credentials.
3. Do not represent similarity scores as calibrated probabilities.
4. Do not present synthetic trend data as real market data.
5. Add a labeled evaluation set before reporting recommendation quality.
6. Preserve candidate privacy when handling uploaded resumes.
