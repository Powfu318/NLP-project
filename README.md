# NLP-Project: AI Industry Impact Analysis

NLP analysis of ~200K AI news articles (2022–2026) to identify which industries 
are most impacted by AI, how they are impacted, and what drives adoption success or failure.

## Overview

| Metric | Value |
|--------|-------|
| Total articles analyzed | 199,380 |
| Relevant articles (after filtering) | 129,326 (64.9%) |
| Industries tracked | 13 |
| Time scope | Jan 2022 – Feb 2026 |
| Sentiment model accuracy | 65.3% |

## Research Questions

1. Which industries are most impacted by AI?
2. How are they impacted — positively or negatively, and by what means?
3. What makes AI adoption succeed or fail?

## Pipeline (7 Notebooks)

| # | Notebook | Description |
|---|----------|-------------|
| 1 | Data Loading & Cleaning | Load parquet → clean text → remove duplicates |
| 2 | Relevance Filtering | AI keyword scoring across 4 signal types → 129K articles |
| 3 | Industry & Entity Extraction | 13-industry keyword dict + spaCy NER |
| 4 | Impact Theme Detection | 12-theme keyword dictionary → industry-theme matrix |
| 5 | Sentiment Model | 1,208 hand-labeled articles → TF-IDF + Logistic Regression |
| 6 | AI Adoption Factors | 9 success + 10 barrier categories → industry cross-tabs |
| 7 | Final Synthesis & Charts | Aggregate outputs → visualizations |

## Key Findings

- **Media & Marketing** (89K articles), **Technology** (78K), and **Finance** (58K) 
  are the most AI-covered industries
- **Regulation & Governance** is the #1 theme across all 13 industries
- **Partnerships/Ecosystem** is the #1 success factor in every single industry
- **Bias & Ethical Concerns** is the top barrier to AI adoption
- AI sentiment is trending **more positive** year-over-year (+4.3pp from 2022→2025)
- **NVIDIA** has the most positive coverage (46% positive) driven by GPU/infrastructure demand
- **Legal** sector has the most negative sentiment (30.5% negative)

## Tech Stack

- Python, Pandas, NumPy
- spaCy (NER entity extraction)
- scikit-learn (TF-IDF, Logistic Regression)
- Matplotlib / Seaborn

## Future Improvements

- Replace TF-IDF sentiment model with fine-tuned DistilBERT (target: 75-85% accuracy)
- Add interactive dashboard to make findings explorable
- Expand to non-English sources for global coverage

## Author

Shengbo Qian — University of Chicago
