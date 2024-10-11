# Sentiment Analysis of IMDB Movie Reviews dataset
This project aims to perform sentiment analysis on movie reviews using the [IMDb dataset of movie reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/). The dataset includes 50,000 reviews, each labeled as either positive or negative. The primary objective is to build models capable of accurately classifying the sentiment expressed in these reviews.

## Dataset
The dataset has the following counts
| Label | Number of Samples|
| :-----: | :---: | 
| Negative | 25000| 
| Positive | 25000| 

## Requirements
The project requires Python 3.x and several libraries. To install the required packages, follow these steps:
1. Ensure you have Python 3.x installed on your system.
2. Download or clone this repository to your local machine.
3. Open a terminal or command prompt and navigate to the project directory.
4. Run the following command to install the required packages:
   
``` 
pip install -r requirements.txt
```
This will install all the necessary libraries listed in the requirements.txt file.

Note: Some libraries like nltk might require additional downloads. After installation, you may need to run the following in a Python environment:
```python
import nltk
nltk.download('stopwords')
```

## Data Preprocessing

Before training the models, the dataset undergoes preprocessing steps to prepare it for analysis. The following preprocessing steps are performed:

1. Removal of HTML tags, special characters and brackets
2. Removal of stop words: Commonly occurring stop words that do not contribute much to sentiment analysis are removed from the reviews.
3. Stemming : to reduce words to root form
4. Reducing all words to lowercase

## Tokenization
To prepare the textual data for model training, the sentences are tokenized using a tokenizer. Tokenization involves splitting the text into individual words or tokens. This step helps in creating input sequences for the models.

## Models Used
Two different models are developed for sentiment analysis of IMDB movie reviews:

**1. Logistic Regression:**
  - Applied to both Bag of Words (BoW) and TF-IDF features
  - Used with L2 regularization and a maximum of 500 iterations

**2. Multinomial Naive Bayes:**
  - Applied to both Bag of Words (BoW) and TF-IDF features
  - Used with default parameters

## Model Training and Evaluation
- The dataset was split into 40,000 training samples and 10,000 test samples
- Models were trained on the preprocessed and vectorized movie review data
- Performance was evaluated using accuracy scores and classification reports

## Results
Based on the experimental results:

**1. Logistic Regression:**
BoW features: 75.12% accuracy
TF-IDF features: 75.00% accuracy

**2. Multinomial Naive Bayes:**
BoW features: 75.10% accuracy
TF-IDF features: 75.09% accuracy

## Visualization
Word clouds were generated to visualize frequently occurring words in positive and negative reviews.


Feel free to explore this project's code and experiment with different preprocessing techniques or model parameters to potentially enhance sentiment analysis performance on the IMDB movie review dataset.
