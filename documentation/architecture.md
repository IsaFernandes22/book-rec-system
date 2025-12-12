```
                   ┌─────────────────────┐
                   │    Book Dataset     │
                   │ (Title, Author,     │
                   │  Genre, Description)│
                   └─────────┬──────────┘
                             │
                             ▼
                   ┌─────────────────────┐
                   │ Data Preprocessing  │
                   │ - Clean text fields │
                   │ - Handle duplicates │
                   └─────────┬──────────┘
                             │
                             ▼
                   ┌─────────────────────┐
                   │  Embedding Layer    │
                   │ - Convert text to   │
                   │   vector embeddings │
                   │ - Using pre-trained │
                   │   language model    │
                   └─────────┬──────────┘
                             │
                             ▼
                   ┌─────────────────────┐
                   │ Similarity Engine   │
                   │ - Compute cosine   │
                   │   similarity       │
                   │ - Rank similar books│
                   └─────────┬──────────┘
                             │
                             ▼
                   ┌─────────────────────┐
                   │ Recommendation API  │
                   │ - Input: book title │
                   │ - Output: top N     │
                   │   recommended books │
                   └─────────┬──────────┘
                             │
                             ▼
                   ┌─────────────────────┐
                   │ Optional Web UI     │
                   │ - Streamlit / Flask │
                   │ - User inputs book  │
                   │   → displays top N  │
                   │   recommendations   │
                   └─────────────────────┘
```