# Understanding and Detecting Malicious Prompts

## Project Overview
This repository contains the project "Understanding and Detecting Malicious Prompts Using Embeddings, Clustering, and Classification", developed for the Fundamentals of Data Science course. The main goal of this project is to analyze, cluster, and classify malicious prompts directed at Large Language Models (LLMs). It also explores how adversarial attacks impact the effectiveness of detection mechanisms.

## Author
Alicja Borek

## Dataset
The project utilizes a dataset of Polish language prompts containing various categories of intents, including:
* Safe
* Sexual Content
* Non-Violent Crimes
* Intellectual Property
* Specialized Advice

The data is divided into original queries and adversarial prompts, which are intentionally modified to bypass security filters.

## Methodology
The analytical pipeline consists of several key stages:
* **Text Representation:** Extracting embeddings using BERT (`paraphrase-multilingual-MiniLM-L12-v2`) and SpaCy (`pl_core_news_lg`).
* **Dimensionality Reduction:** Projecting high-dimensional embeddings into 2D space using PCA, t-SNE, and UMAP for visualization.
* **Clustering:** Grouping prompts using the K-Means algorithm and evaluating the results with the Silhouette Score.
* **Anomaly Detection:** Applying the Isolation Forest algorithm to identify outliers and hidden adversarial attacks.
* **Classification:** Training machine learning models (Logistic Regression, SVM, Random Forest) to detect malicious intents and evaluating their performance drop on adversarial data.

## Technologies & Libraries
The following tools and libraries were used in this project:
* Python
* pandas, numpy
* scikit-learn
* sentence-transformers
* spacy
* umap-learn
* plotly
