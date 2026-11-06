# Movie Recommender

A movie recommendation system that combines multi-label genre classification with hybrid information retrieval to provide relevant movie suggestions based on natural-language queries.

## Overview

This project uses a fine-tuned DistilBERT classifier and a hybrid retrieval pipeline combining BM25 keyword search and Sentence Transformer embeddings.

Users can describe the movies they want using genres, moods, actors, directors, or release years.

## Key Features

- **Multi-label Genre Classification:** Fine-tuned DistilBERT model for predicting movie genres.
- **Hybrid Search:** Combines BM25 keyword retrieval with semantic similarity using Sentence Transformers.
- **Intent Parsing:** Extracts user preferences such as mood, actor, director, year, decade, and year range.
- **Result Re-ranking:** Improves recommendations using genre alignment, semantic relevance, cast and director matching, and ratings.
- **Interactive Interface:** Built with Gradio for natural-language movie discovery.

## Technologies

- Python
- PyTorch
- Hugging Face Transformers
- Sentence Transformers
- BM25
- NumPy & Pandas
- Scikit-learn
- Gradio
- Google Colab

## Project Workflow

1. Load preprocessed movie data.
2. Load the fine-tuned genre classification model.
3. Generate semantic representations of movie descriptions.
4. Retrieve candidate movies using hybrid search.
5. Parse user intent and re-rank the results.
6. Display recommendations through the Gradio interface.

## Model & Data

The project uses saved model and search-index artifacts stored in Google Drive.

Model training and search-index generation are optional steps and do not need to be repeated when the saved artifacts are available.

## How to Run

The notebook is designed to run in Google Colab.

1. Open the project notebook in Google Colab.
2. Mount Google Drive.
3. Make sure the required saved model, movie data, and embedding files are available in the expected project directories.
4. Install the required dependencies.
5. Run the inference and Gradio application cells.

## Interface

The application allows users to enter natural-language movie requests and receive ranked recommendations.

## Project Status

Developed as an applied machine learning and information retrieval project.# movie-recommender-
