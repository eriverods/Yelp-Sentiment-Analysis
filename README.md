# Exploratory Data Analysis and Advanced Analysis of Yelp Reviews for Asian Restaurants in the United States

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset Overview](#dataset-overview)
3. [Prerequisites](#prerequisites)
4. [File Descriptions](#file-descriptions)
   - [Exploratory Data Analysis Notebook](#exploratory-data-analysis-notebook)
   - [Advanced Analysis Notebook](#advanced-analysis-notebook)
5. [How to Run the Notebooks](#how-to-run-the-notebooks)
6. [Summary of Findings](#summary-of-findings)
   - [Exploratory Data Analysis](#exploratory-data-analysis)
   - [Advanced Analysis](#advanced-analysis)
7. [Next Steps](#next-steps)
8. [Acknowledgments](#acknowledgments)

## 1. Introduction
This project aims to understand customer perceptions of Asian restaurants in the United States by analyzing Yelp reviews. The analysis is divided into two main parts:

- **Exploratory Data Analysis (EDA)**: Provides an initial examination of the data to discover patterns, spot anomalies, test hypotheses, and check assumptions.
- **Advanced Analysis**: Builds upon the EDA to perform deeper analyses, including topic modeling and aspect-based sentiment analysis, to uncover hidden themes and sentiments within the reviews.

## 2. Dataset Overview
The analysis utilizes data from the Yelp Open Dataset, specifically focusing on:

- **Business Data**: Information about businesses, including their attributes, categories, and review counts.
- **Review Data**: Customer reviews, including the review text, star ratings, and timestamps.

### Filtering Criteria
- **Location**: United States only.
- **Business Status**: Only open businesses are included.
- **Review Count**: Businesses with at least 5 reviews to ensure sufficient data for analysis.
- **Cuisine Type**: Focused on Asian restaurants, identified by specific keywords in the categories.

**Data Privacy Note**: All data used in this analysis is anonymized and complies with Yelp's data usage policies.

## 3. Prerequisites
To run the notebooks, ensure you have the following installed:

- **Python 3.6 or higher**
- **Jupyter Notebook or JupyterLab**
- **Libraries**:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - nltk
  - gensim
  - pyLDAvis
  - wordcloud
  - scikit-learn (optional)

**Note**: Some NLTK resources need to be downloaded within the notebook (e.g., stopwords, punkt, vader_lexicon).

## 4. File Descriptions

### 4.1 Exploratory Data Analysis Notebook
- **Filename**: `01_EDA_Yelp_Asian_Restaurants.ipynb`
- **Purpose**:
  - Perform initial data exploration to understand the dataset.
  - Analyze customer ratings, review lengths, and sentiments.
  - Identify common words and themes in the reviews.
  - Examine geographical patterns in customer perceptions.

**Key Steps**:
1. **Data Loading and Preprocessing**
   - Load business and review datasets.
   - Filter for open Asian restaurants in the US with at least 5 reviews.
   - Merge business and review data.
2. **Descriptive Statistics**
   - Calculate the number of reviews and unique restaurants.
   - Compute average ratings and review lengths.
3. **Ratings Distribution**
   - Visualize the distribution of star ratings.
   - Analyze rating statistics.
4. **Review Length Analysis**
   - Compute review lengths.
   - Visualize the distribution using histograms and box plots.
   - Analyze review lengths by star rating.
5. **Text Preprocessing**
   - Tokenize review texts.
   - Remove stopwords and restaurant-specific common words.
6. **Common Words and Bigrams**
   - Identify the most frequent words and bigrams in the reviews.
7. **Sentiment Analysis**
   - Use VADER sentiment analyzer to compute sentiment scores.
   - Analyze the relationship between sentiment scores and star ratings.
8. **Geographical Analysis**
   - Examine average ratings and sentiment scores by state.
   - Visualize data using bar plots.
9. **Correlation Analysis**
   - Investigate the correlation between review length and star rating.
10. **Word Clouds**
    - Generate word clouds for all reviews, as well as positive and negative reviews separately.
11. **Data Saving**
    - Save the preprocessed data for further analysis.

**Usage**: Run each cell sequentially. Ensure that the Yelp dataset files are accessible in the specified paths. Adjust file paths if necessary.

### 4.2 Advanced Analysis Notebook
- **Filename**: `02_Advanced_Analysis_Yelp_Asian_Restaurants.ipynb`
- **Purpose**:
  - Perform in-depth analysis using topic modeling and aspect-based sentiment analysis.
  - Uncover hidden themes and sentiments in the reviews.
  - Provide actionable insights based on the advanced analysis.

**Key Steps**:
1. **Data Loading**
   - Load the preprocessed data saved from the EDA notebook.
2. **Topic Modeling with LDA**
   - Prepare data by creating a dictionary and corpus for LDA.
   - Determine the optimal number of topics using coherence scores.
   - Build the final LDA model.
   - Interpret the topics based on the top keywords.
   - Visualize topics using pyLDAvis.
   - Assign dominant topics to reviews.
3. **Aspect-Based Sentiment Analysis**
   - Merge dominant topics with the original data.
   - Calculate average sentiment scores per topic.
   - Visualize sentiments associated with each aspect (topic).
4. **Visualization and Interpretation**
   - Create bar plots to display average sentiment scores by topic.
   - Interpret the results to identify positive and negative aspects.
5. **Conclusion and Next Steps**
   - Summarize key findings from the advanced analysis.
   - Suggest potential next steps for further exploration.

**Usage**: Ensure the preprocessed data file (`asian_restaurants_reviews_us_preprocessed.csv`) is available. Run each cell sequentially. Install any missing libraries as needed.

## 5. How to Run the Notebooks

### Clone or Download the Repository
Place all the necessary data files and notebooks in the same directory.

### Install Required Libraries
Use `pip` or `conda` to install any missing libraries. Example:

```sh
pip install pandas numpy matplotlib seaborn nltk gensim pyLDAvis wordcloud
```

### Download NLTK Resources
Some NLTK resources are downloaded within the notebooks. Ensure an internet connection is available when running those cells.

### Run the Notebooks
- Open the notebooks using Jupyter Notebook or JupyterLab.
- Execute the cells in order.
- Adjust file paths if your data files are in different locations.

## 6. Summary of Findings

### 6.1 Exploratory Data Analysis

**Key Observations**:
- **Data Size**:
  - Total Reviews Analyzed: 591,773
  - Total Open Asian Restaurants with ≥5 Reviews: 4,914
- **Ratings Distribution**:
  - The majority of reviews are positive, with a higher number of 4 and 5-star ratings.
  - Average Star Rating: 3.90
- **Review Length**:
  - Average Review Length: 95.65 words
  - Review lengths vary slightly across star ratings, with no strong correlation.
- **Common Words and Bigrams**:
  - Frequent positive descriptors: "good," "great," "delicious," "fresh."
  - Common dishes mentioned: "sushi," "noodles," "rice," "dumplings."
- **Sentiment Analysis**:
  - Sentiment scores correlate well with star ratings.
  - Positive reviews have higher sentiment scores, as expected.
- **Geographical Insights**:
  - Average ratings and sentiment scores vary across states.
  - States like Indiana, Florida, and Louisiana have higher average ratings for Asian restaurants.
- **Correlation Analysis**:
  - Weak negative correlation between review length and star rating (-0.17).
- **Word Clouds**:
  - Positive reviews emphasize taste and quality.
  - Negative reviews highlight issues like service, price, or specific complaints.

### 6.2 Advanced Analysis

**Topic Modeling Findings**:
- **Identified Topics**:
  - **Topic 1**: Service Experience (e.g., "service," "staff," "friendly")
  - **Topic 2**: Food Taste and Quality (e.g., "delicious," "flavor," "taste")
  - **Topic 3**: Specific Cuisines (e.g., "sushi," "ramen," "spicy")
  - **Topic 4**: Ambiance and Atmosphere (e.g., "place," "atmosphere," "decor")
  - **Topic 5**: Negative Experiences (e.g., "bad," "worst," "never")
- **Topic Distribution**:
  - Topics related to food quality and service are the most prevalent.

**Aspect-Based Sentiment Analysis Findings**:
- **Sentiments per Topic**:
  - **Positive Sentiments**:
    - Topics on food taste and ambiance have higher average sentiment scores.
  - **Negative Sentiments**:
    - Topics highlighting negative experiences have lower sentiment scores.
- **Insights**:
  - Customers generally have positive sentiments towards food quality and restaurant ambiance.
  - Negative sentiments are primarily associated with poor service or bad experiences.

## 7. Next Steps

- **Temporal Analysis**: Examine how customer sentiments and topic prevalence change over time.
- **Cuisine-Specific Analysis**: Compare different Asian cuisines (e.g., Chinese, Japanese, Indian) to identify unique patterns.
- **Regional Analysis**: Investigate regional differences in customer perceptions.
- **Machine Learning Models**: Build predictive models to classify reviews or predict ratings based on text.
- **Business Recommendations**: Use insights to provide actionable recommendations for restaurant owners to improve customer satisfaction.

## 8. Acknowledgments

- **Yelp Open Dataset**: We thank Yelp for providing the open dataset used in this analysis. https://www.yelp.com/dataset
- **Libraries and Tools**: Appreciation for the developers of pandas, numpy, matplotlib, seaborn, nltk, gensim, pyLDAvis, and other tools that made this analysis possible.

**Note**: This project complies with Yelp's data usage policies. All data used is anonymized, and no personally identifiable information (PII) is disclosed.

