# sentiment-analysis-using-word2vec
 
Steps:
1. The dataset is first read using pandas library.
2. Reviews are then extracted from the dataset.
3. Each review is then preprocessed and cleaned (html, integers, and punctuation marks are removed).
4. Reviews are divided into training set and test set (75% reserved for training and 25% reserved for testing).
5. Word Embeddings are then learned using Gensim Word2Vec on training data.
6. For sentiment analysis, the reviews in both training data and test data are converted into a numeric vector as follows:
a. The embeddings vector of each word in a review is extracted from word2vec model
b. The embeddings are then added and divided by the number of words in that review. This gives us an average vector of the review.
7. The numeric vectors of all reviews in the training set are then fed to different machine learning algorithms for training.
8. The accuracy of models is then measured using the vectors of test set.


Test Accuracies:
Naïve Bayes: 63.26%
Neural Network: 81.42%
Random Forest: 76.69%
KNN: 69.25%
