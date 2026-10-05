# Evaluation

## Current state

The repository does not contain a versioned labeled benchmark for resume-to-job recommendation quality.

Therefore the project should not claim:

- recommendation accuracy;
- precision/recall;
- ranking quality;
- employment probability;
- improvement over a baseline.

## Recommended benchmark

A defensible evaluation set should contain:

- anonymized candidate/resume profiles;
- job postings;
- human relevance labels;
- job-source metadata;
- a fixed train/evaluation split if the model is tuned;
- reproducible embedding/model version.

Useful ranking metrics:

- Recall@K;
- Precision@K;
- MRR;
- nDCG@K.

A simple baseline should be included, such as TF-IDF cosine similarity, so the Sentence-Transformer approach can be evaluated against a non-neural baseline.

## Current similarity score

Cosine similarity is used only as a ranking signal. It is not a calibrated probability or hiring likelihood.

## Trend visualization

The current trend chart is generated from random values for demonstration. It has no evaluation value and must not be used as evidence of market demand.
