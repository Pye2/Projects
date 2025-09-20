# Text Analysis Using Naive Bayes Models

This project aims to classify customer reviews as either positive or negative using natural 
language processing (NLP) techniques, I employed Naive Bayes models to analyze textual 
reviews from dataset of user feedback, covering all stages from data cleaning and 
exploration to model building and performance evaluation. 
# Dataset Used 
The dataset comprises customer reviews with ratings from 1 to 5, To simplify the analysis, 
I transformed the ratings into binary classifications: ratings of 4 and 5 were considered 
positive, and ratings of 1 and 2 were considered negative, Neutral ratings (3) were 
excluded. 
# Data Exploration 
I conducted an initial exploration of the data to understand the distribution of ratings and 
the nature of the reviews, It was observed that ratings with a score of 5 were the most 
frequent, indicating general positive bias in the dataset, This distribution was illustrated 
using bar chart, which highlighted that most customers expressed high satisfaction with 
their experiences by assigning the highest possible rating. 
# Analytical Steps 
## 1. Text Data Cleaning: - Standardizing Text: All text was converted to lowercase to ensure uniformity. - Removing Unnecessary Elements: Special characters, links, and numbers were removed 
using regular expressions. - Stopword Removal and Lemmatization: The spacy library was utilized to perform 
lemmatization and remove stopwords, simplifying the text to its essential terms. 
## 2. Data Analysis: - Review Length Analysis: new column representing the length of each review was 
added, and the distribution of review lengths was analyzed to understand the variation in 
text length. - Rating Distribution: A bar chart illustrated the distribution of reviews across rating 
categories, allowing us to visualize the overall sentiment in the dataset. - Word Cloud Analysis: Frequent words for each rating category were visualized, helping 
us understand the common terms associated with positive and negative sentiments. 
## 3. Transforming Text into Numeric Features: - I applied TfidfVectorizer to transform text into numerical features based on the 
frequency and importance of words, which enhances the model's ability to distinguish 
between positive and negative reviews. 
## 4. Model Building and Evaluation: - Data Splitting: I used train_test_split to split the data into 80% training and 20% 
testing sets. - Training Models: Two models were trained: Multinomial Naive Bayes and Bernoulli 
Naive Bayes. - Evaluating Model Performance Using Confusion Matrix and ROC Curve: The confusion 
matrix and ROC curve were used to evaluate each models accuracy and to calculate the 
Area Under the Curve (AUC) for further insight into model performance.
