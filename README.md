# Text Classification Using Different Vectorization Techniques

## Project Overview

This project explores and compares different text vectorization techniques for sentiment classification using the IMDb Dataset of 50K Movie Reviews.

The main objective is to understand how different text representation techniques affect the performance of machine learning models in classifying movie reviews as positive or negative.

## Dataset

**IMDb Dataset of 50K Movie Reviews**

- Source: Kaggle
- Total reviews: 50,000
- Input feature: Movie review text
- Target variable: Sentiment (positive/negative)

Dataset link: https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

The dataset is not included in this repository. Download it from Kaggle and place `IMDB Dataset.csv` in your working directory before running the notebooks.

## Vectorization Techniques

This project implements four different text representation techniques:

### 1. Bag of Words (BoW)
Converts text into numerical vectors based on word frequencies.

### 2. N-Grams
Captures sequences of words to preserve some local context. This project experiments with bigrams.

### 3. TF-IDF (Term Frequency–Inverse Document Frequency)
Assigns importance to words based on their frequency within a document and across the document collection.

### 4. Word2Vec
Uses word embeddings to represent words as dense numerical vectors that capture semantic relationships.

## Repository Structure

```text
text-classification-vectorization-comparison/
│
├── dataset/
│   └── README.md
│
├── notebooks/
│   ├── README.md
│   ├── Text_Classification_BOW.ipynb
│   ├── Text_Classification_Bigrams.ipynb
│   ├── Text_Classification_Word2Vec.ipynb
│   └── Text_Classification_tfidf.ipynb
│
├── requirements.txt
│
└── README.md
```

## Experimental Results

The following results were obtained during the experiments:

| Vectorization | Classifier / Configuration | Score |
|---|---|---:|
| BoW | Gaussian Naive Bayes | 0.63645 |
| BoW | Random Forest | 0.83575 |
| BoW | Random Forest (max_features=3000) | 0.83976 |
| Bigrams | Random Forest (max_features=5000) | 0.84326 |
| TF-IDF | Random Forest | **0.84477** |
| Word2Vec | Classifier to be documented | 0.77166 |

*Note: The evaluation metric and Word2Vec classifier configuration will be specified in the final experimental documentation.*

## Key Observations

- Random Forest performed better than Gaussian Naive Bayes in the BoW experiments.
- Increasing the number of features improved the BoW results.
- Bigram features provided an improvement over the initial BoW experiments.
- TF-IDF achieved the highest score among the experiments conducted so far.
- Word2Vec produced a lower score than TF-IDF in the current experiment due to smaller dataset.

## Tools and Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Gensim
- Matplotlib

## How to Run

1. Clone or download this repository.
2. Download the IMDb dataset from Kaggle.
3. Open the notebooks using Google Colab or Jupyter Notebook.
4. Upload the dataset to your working environment.
5. Run the notebooks to reproduce the experiments.

## Future Improvements

- Experiment with different Word2Vec configurations.
- Explore TF-IDF-weighted Word2Vec embeddings.
- Compare additional classification algorithms.
- Evaluate models using precision, recall, F1-score and balanced accuracy.
- Perform hyperparameter tuning.

## Author

Computer Engineering Student

## Acknowledgement

Dataset provided by Kaggle and the IMDb movie review collection.
