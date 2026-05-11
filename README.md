# Movie Recommendation System

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3%2B-orange?logo=scikit-learn)](https://scikit-learn.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE)

A hybrid movie recommendation engine combining **content-based filtering**, **user-based collaborative filtering**, and a **popularity baseline** (Bayesian weighted rating). Runs entirely on a built-in 25-movie demo dataset — no external downloads required.

## Recommendation Strategies

| Strategy | Method | Best For |
|---|---|---|
| **Popularity** | Bayesian weighted rating (WR) | Cold-start / new users |
| **Content-Based** | TF-IDF on genres + plot → cosine similarity | "More like this" |
| **Collaborative** | User-item cosine similarity | Personalised picks |

## Quick Start

```bash
pip install -r requirements.txt

# Full demo (all three strategies)
python recommender.py demo

# Top 10 popular movies
python recommender.py popular --n 10

# Find movies similar to a title
python recommender.py similar "Inception" --n 5

# Personalised recommendations for a user
python recommender.py user alice --n 5
```

## Demo Output

```
📊  Top 5 Popular Movies (weighted rating):
              title            genres  vote_average  weighted_score
The Shawshank Redemption         drama           9.3            9.21
        The Dark Knight  action crime thriller   9.0            8.94
              Inception  action sci-fi thriller  8.8            8.74
           Pulp Fiction        crime drama      8.9            8.71
          Interstellar  sci-fi drama adventure   8.6            8.52
