# Movie Recommender System

A Natural Language Processing and Information Retrieval project that helps users discover movies through natural-language queries.

The system combines multi-label genre classification, semantic search, keyword retrieval, and intent parsing to deliver relevant movie recommendations.

## 1. Project Overview

The Movie Recommender System allows users to describe the movies they want in their own words instead of relying only on traditional filters.

For example, users can search for:

- Science fiction movies released between 2010 and 2015.
- Movies starring Tom Cruise.
- Movies directed by Christopher Nolan.
- Animated movies for children.

The system processes each query, identifies relevant preferences and constraints, retrieves candidate movies, and presents ranked recommendations through an interactive web interface.

## 2. Key Features

**Multi-label Genre Classification**
- Uses a fine-tuned DistilBERT model.
- Predicts multiple movie genres from natural-language descriptions.
- Applies class-specific decision thresholds.

**Hybrid Information Retrieval**
- BM25 for keyword-based retrieval.
- Sentence Transformers for semantic similarity.
- Combines both retrieval signals to identify relevant movies.

**Natural Language Intent Parsing**
- Detects explicit genres.
- Extracts actors and directors.
- Identifies release years, decades, and year ranges.
- Supports additional query preferences such as mood.

**Movie Filtering and Ranking**
- Applies detected search constraints.
- Uses hybrid retrieval scores to rank candidate movies.
- Presents the most relevant available results.

**Interactive Web Interface**
- Built with Gradio.
- Allows users to enter natural-language queries and explore recommendations.

## 3. System Workflow

1. Receive a natural-language movie query.
2. Predict relevant genres using DistilBERT.
3. Extract search intent and constraints.
4. Retrieve candidate movies using BM25 and semantic similarity.
5. Apply relevant filters and ranking logic.
6. Display recommendations through the Gradio interface.

## 4. Machine Learning Approach

### Genre Classification

A fine-tuned DistilBERT model is used for multi-label genre prediction.

Since a movie can belong to multiple genres, the classifier predicts genre probabilities and applies individual thresholds to determine the selected labels.

### Hybrid Search

The retrieval pipeline combines two complementary methods:

- **BM25:** Identifies relevant movies through keyword matching.
- **Sentence Transformers:** Captures semantic relationships between the user's query and movie descriptions.

The combined retrieval score helps balance exact keyword relevance with contextual similarity.

## 5. Dataset

The project uses a dataset containing **4,682 movie records**.

Available information includes:

- Movie ID and title
- Overview
- Genres
- Release year
- Vote average
- Cast
- Director

The dataset is used for genre classification, information retrieval, and movie recommendation.

## 6. Technologies Used

| Category | Technologies |
|---|---|
| Programming | Python |
| Machine Learning | PyTorch, Scikit-learn |
| NLP | Hugging Face Transformers, DistilBERT |
| Semantic Search | Sentence Transformers |
| Information Retrieval | BM25 |
| Data Processing | Pandas, NumPy |
| User Interface | Gradio |
| Development Environment | Google Colab |

## 7. Notebook Structure

The notebook is organized into seven main sections:

1. Environment Setup
2. Data Loading
3. Optional Model Training
4. Optional Evaluation & Threshold Calibration
5. Optional Search Index Building
6. Inference & Recommendation
7. Gradio Web Interface

Model training and search-index generation are optional when the required saved artifacts are already available.

## 8. Running the Project

The notebook is designed to run in Google Colab.

To use the recommendation system:

1. Open `Movie_Recommender.ipynb` in Google Colab.
2. Mount Google Drive.
3. Ensure the required dataset, trained model, and search-index files are available in the expected directories.
4. Install the required Python dependencies.
5. Run the inference and recommendation sections.
6. Launch the Gradio interface.

**Important:** The notebook is hosted in this repository, while the dataset, trained model files, and search-index artifacts are stored separately in Google Drive. Their paths must be configured before running the application.

## 9. Project Scope

This project demonstrates the practical application of:

- Natural Language Processing
- Multi-label Text Classification
- Semantic Search
- Hybrid Information Retrieval
- Natural Language Intent Parsing
- Recommendation Systems
- Interactive Machine Learning Applications

---

**Project Type:** Applied Machine Learning & NLP  
**Environment:** Google Colab
