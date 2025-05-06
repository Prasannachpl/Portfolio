# Movie Recommendation Systems

This project implements and evaluates two different approaches for building movie recommendation systems using machine learning techniques.

## Project Overview

Recommendation systems are crucial components of modern digital platforms that help users discover content tailored to their preferences. This project explores both traditional collaborative filtering techniques and advanced deep learning approaches to build effective movie recommendation systems.

## Approaches

### 1. Deep Neural Networks for YouTube-Inspired Recommendations

The first approach, documented in Movie_recommendation.ipynb, implements:

- *Collaborative Filtering*: A matrix factorization technique that leverages user-item interactions
- *Deep Learning Model*: A neural network architecture inspired by "Deep Neural Networks for YouTube Recommendations" paper
- Both models are trained and evaluated on the MovieLens 100k dataset

Key results:
- Collaborative Filtering RMSE: 0.986
- Deep Learning Model RMSE: 0.935

Features:
- User and item embedding layers
- Customized recommendation generation
- Comparison of different architectures

### 2. Content-Based and Collaborative Filtering for Netflix

The second approach, outlined in Movie_recommendation_netflix_markdown.ipynb, explores:

- *Content-Based Filtering*: Using TF-IDF and cosine similarity on movie metadata
- *KNN with Means*: A collaborative filtering approach using k-nearest neighbors
- *SVD Implementation*: Matrix decomposition to identify latent factors

This approach was designed for the Netflix Movies dataset but faced computational limitations that are addressed in the future work section.

## Datasets

- *MovieLens 100k*: Contains 100,000 ratings from 943 users on 1,682 movies
- *Netflix Movies Dataset*: A larger dataset (implementation limited by computational resources)

## Methodologies

The project implements:
- Data preprocessing and normalization
- Embedding techniques for users and items
- Neural network architectures with dropout, batch normalization, and ReLU activations
- Evaluation using Root Mean Square Error (RMSE)
- Early stopping and learning rate scheduling

## Results

- The deep learning approach demonstrated superior performance compared to traditional collaborative filtering
- Performance metrics show the ability to make accurate rating predictions
- The models can generate personalized movie recommendations for specific users

## Future Work

- Implementation of the models on larger datasets like the Netflix Movies dataset
- Leveraging more powerful GPU resources for improved computational capabilities
- Exploring hybrid recommendation approaches that combine multiple techniques

## References

- [Deep Neural Networks for YouTube Recommendations](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45530.pdf)
- [MovieLens 100k Dataset](https://grouplens.org/datasets/movielens/100k/)
- [LibRec Benchmarks](https://www.librec.net/release/v1.3/example.html)

## Requirements

- Python 3.x
- PyTorch
- pandas
- numpy
- matplotlib
- tqdm
