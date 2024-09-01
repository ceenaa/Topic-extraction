# Text Classification and Topic Extraction from COVID-19 Articles

## Overview

In response to the surge in COVID-19-related research articles, this project focuses on the classification and topic extraction of scientific papers. The goal is to assist researchers and healthcare professionals in quickly finding relevant information amidst the vast number of publications.

A dataset containing metadata from approximately 10,000 articles related to COVID-19 is utilized in this project. The dataset is provided in CSV format and includes the following fields:

- **paper_id**: A unique identifier for each article, extracted from the PDF files.
- **doi**: The Digital Object Identifier for referencing the articles.
- **abstract**: The article’s abstract (if available).
- **body_text**: The main content of the article.
- **authors**: The authors listed in a structured format.
- **title**: The title of the article.
- **journal**: The journal in which the article was published.
- **abstract_summary**: A summary of the abstract.

## Goal

This project aims to determine whether similar research articles can be identified and categorized using text classification and topic extraction methods. Additionally, it facilitates the extraction of key topics from existing research, aiding in the quick dissemination of critical knowledge among specialists.

## Dataset

The dataset includes the following key features:

- **paper_id**: Unique identifier for each article.
- **doi**: Digital Object Identifier for referencing.
- **abstract**: Summary of the article.
- **body_text**: Full content of the article.
- **authors**: List of authors.
- **title**: Title of the article.
- **journal**: Publication source.
- **abstract_summary**: Summary of the abstract.

## Methodology

The project employs text classification and topic extraction techniques to analyze and categorize the articles. These methods help identify the main topics discussed in each article and classify them accordingly.

## Methodology

The following techniques and methods were used in this project:

### 1. **Preprocessing**
   - **Tokenizing**: Splitting the text into individual words or tokens.
   - **Stemming and Lemmatization**: Reducing words to their root forms.
   - **Removing Stopwords**: Filtering out common words that do not carry significant meaning (e.g., "and", "the").
   - **Removing Punctuation**: Cleaning the text by eliminating punctuation marks.

### TF-IDF Matrix
Term Frequency-Inverse Document Frequency (TF-IDF) is a statistical measure used to evaluate the importance of words in a document relative to a collection of documents. It is composed of two main components:

1. Term Frequency (TF): Measures how often a word appears in a document. It can be either raw frequency or normalized to account for document length.
2. Inverse Document Frequency (IDF): Measures the importance of a word by considering how common or rare it is across all documents. The formula is IDF = log(N / DF), where N is the total number of documents and DF is the number of documents containing the word.
The TF-IDF matrix is a two-dimensional matrix where rows represent documents and columns represent terms. Each cell indicates the importance of a term in a document.

### 2. **Feature Extraction**
   - Transforming textual data into numerical features for analysis.

### 3. **Dimensionality Reduction**
   - **PCA (Principal Component Analysis)**: Reducing the dimensionality of the feature set while preserving as much variance as possible.

### 4. **Clustering**
   - **K-Means Clustering**: Grouping articles into clusters based on their features.
   - **Elbow Method**: Determining the optimal number of clusters.
   - **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: Identifying clusters based on density.
   - **Hierarchical Clustering**: Creating a hierarchy of clusters.

### 5. **Visualization**
   - **t-SNE (t-Distributed Stochastic Neighbor Embedding)**: Visualizing high-dimensional data in a lower-dimensional space.
   - **Topic Modeling**: Extracting the main topics from the articles using techniques like LDA (Latent Dirichlet Allocation).
   - **Visualization Techniques**: Various visualizations were employed to interpret and present the results effectively.

### Topic Modeling
Topic modeling is performed on each cluster to identify and interpret the topics within the documents:

1. Latent Dirichlet Allocation (LDA):
   * generative probabilistic model that discovers topics based on the distribution of words in documents.

2. Latent Semantic Analysis (LSA):
   * Uses singular value decomposition to identify topics by analyzing the term-document matrix.

3. Non-Negative Matrix Factorization (NMF):
   * Decomposes the matrix into two non-negative matrices, identifying topics based on the decomposition.


## Results
![image](https://github.com/user-attachments/assets/ae1595e8-1d0d-453f-8837-0fd9c38e58bd)
