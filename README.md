# Topic Modelling of IMDb Movie Reviews

## Motivation

This project was part of the NUS module "IT1244 Artificial Intelligence: Technology and Impact" where I worked in a team of 5 to conduct sentiment analysis on a provided dataset of 50,000 IMDb movie reviews. My role in the research was to conduct topic modelling on the dataset to determine what factors contributed most to the review sentiment.

## Methodology

Topic Modelling was conducted on the reviews to determine the dominant topics. The reviews were first run through a Question-Answering model based on MiniLM, asking the question “What was the best aspect of this movie?” and “What was the worst aspect of this movie?”, respectively. The Top2Vec library (Angelov, 2020) was used to model the topics: The extracted answers were then embedded using the Doc2Vec model, reduced in dimensionality using Uniform Manifold Approximation and Projection (UMAP), and finally clustered using Hierarchical Density-Based Spatial Clustering of Applications with Noise (HDBSCAN). Taking the centroids of the clusters and identifying the vectors nearest to each centroid, we arrive at a set of words that are representative of each cluster, shown below.
