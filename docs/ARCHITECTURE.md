# Architecture

## Current pipeline

```text
PDF resume
   |
   v
PyPDF2 text extraction
   |
   v
SentenceTransformer
all-MiniLM-L6-v2
   |
   +--------------------+
   |                    |
   v                    v
Resume embedding    Remote job feed
                         |
                         v
                 Job title + description
                         |
                         v
                 Job embeddings
                         |
                         v
                 Cosine similarity
                         |
                         v
                    Ranking
                         |
                         v
                Top recommendations
```

## UI capabilities

The Streamlit application currently supports:

- resume upload;
- extracted-text inspection;
- top-five semantic recommendations;
- related jobs by category;
- country filtering;
- external application links;
- demonstration trend charts.

## Boundary

The application does not currently implement:

- continuous monitoring;
- a persistent job database;
- candidate profiles;
- resume optimization;
- application submission;
- recommendation calibration;
- production observability.

## Data integrity

The country trend visualization uses random demonstration data. It must not be interpreted as an actual market-trend dataset.
