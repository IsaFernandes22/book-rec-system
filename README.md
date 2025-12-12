# AI Book Recommendation System

## Project Overview
The **AI Book Recommendation System** is a Python-based application that recommends books to users based on a given book they like or their reading preferences. The system leverages **AI embeddings** to understand book descriptions and compute similarity between books, enabling personalized recommendations even for books with few ratings.  

This project is designed to demonstrate practical AI integration, including text embeddings, similarity computation, and simple recommendation logic.

---

## Features
- **Content-based recommendations**: Suggest books similar to a given book using description, author, and genre.
- **AI-powered embeddings**: Convert book descriptions into vector representations using a pre-trained language model.
- **Similarity scoring**: Recommend books based on cosine similarity between embeddings.
- **Optional hybrid approach**: Can integrate collaborative filtering if user rating data is available.
- **Easy to use**: Input a book title to get a ranked list of recommended books.
- **Extendable**: Can later be turned into a web app (Streamlit/Flask) or include more AI features.

---

## How It Works
1. **Data Collection**  
   - Dataset of books with metadata: title, author, genre, description, ratings (optional).  
   - Source: Goodreads dataset by Soumik.

2. **Data Preprocessing**  
   - Clean text fields (description, author, genre).  
   - Remove duplicates or incomplete entries.  

3. **Embedding Generation**  
   - Use a pre-trained language model (e.g., `sentence-transformers` or OpenAI embeddings) to convert book descriptions into numerical vectors.  
   - These vectors capture semantic meaning of the text.

4. **Similarity Computation**  
   - Compute pairwise similarity between book embeddings using **cosine similarity**.  
   - Higher similarity → more relevant recommendation.

5. **Recommendation Algorithm**  
   - For a given book input, find top N most similar books based on embedding similarity.  
   - Filter by genre, author, or other metadata.

6. **Output**  
   - Return a ranked list of recommended books with title, author, and brief description.

---

## Tech Stack
- **Python 3.10+**
- Libraries:
  - `pandas`, `numpy` – data handling
  - `scikit-learn` – similarity computation
  - `sentence-transformers` – embeddings
  - `surprise` – collaborative filtering
  - `Streamlit` or `Flask` – web interface

## Dataset

- Dataset was downloaded from the (Kaggle Goodreads-books dataset by Soumik)[https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks?resource=download].
- It has the following columns:
    - title: The name under which the book was published.
    - authors: Names of the authors of the book. Multiple authors are delimited with -.
    - average_rating: The average rating of the book received in total.
    - isbn: Another unique number to identify the book, the International Standard Book Number.
    - isbn13: A 13-digit ISBN to identify the book, instead of the standard 11-digit ISBN.
    - language_code: Helps understand what is the primary language of the book. For instance, eng is standard for English.
    - num_pages: Number of pages the book contains.
    - ratings_count: Total number of ratings the book received.
    - text_reviews_count: Total number of written text reviews the book received.
