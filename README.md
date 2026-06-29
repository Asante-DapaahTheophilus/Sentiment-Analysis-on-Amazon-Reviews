# Sentiment-Analysis-on-Amazon-Reviews
I used NLP to analyze classify customers reviews into Positive, Negative or Neutral feedback on Amazon Reviews.
# Amazon Fine Food Reviews Sentiment Analysis Using NLP

## Project Overview

This project applies Natural Language Processing (NLP) techniques to analyze customer reviews from the Amazon Fine Food Reviews dataset. The objective was to classify customer opinions as **Positive**, **Neutral**, or **Negative** and uncover insights from large-scale textual data.

Using Python and NLTK, the project demonstrates the complete NLP workflow, including text preprocessing, sentiment analysis, visualization, and interpretation of customer feedback.

---

## Dataset

The dataset used in this project is the **Amazon Fine Food Reviews Dataset** from Kaggle, containing over 500,000 customer reviews of food products sold on Amazon.

### Key Features

* Review Score (1–5 stars)
* Review Summary
* Review Text
* Product Information
* User Information
* Review Timestamp

For sentiment classification:

* Scores 1–2 → Negative
* Score 3 → Neutral
* Scores 4–5 → Positive

---

## Project Objectives

* Understand customer sentiment from textual reviews.
* Clean and preprocess unstructured text data.
* Apply NLP techniques to prepare text for analysis.
* Perform sentiment classification using NLTK's VADER sentiment analyzer.
* Visualize sentiment distribution.
* Identify frequently occurring words using Word Clouds.
* Generate sentiment scores for individual reviews.

---

## Tools and Libraries

* Python
* Pandas
* NLTK
* Matplotlib
* WordCloud
* Regular Expressions (re)

---

## Project Workflow

### 1. Data Loading

The Amazon Fine Food Reviews dataset was imported into Python using Pandas.

```python
df = pd.read_csv("Reviews.csv")
```

The dataset was inspected for structure, missing values, and relevant features.

---

### 2. Data Preprocessing

Raw text data often contains punctuation, numbers, stopwords, and inconsistencies that can affect analysis.

The following preprocessing steps were applied:

#### Text Cleaning

* Converted text to lowercase
* Removed punctuation and special characters
* Removed numerical values

#### Tokenization

Each review was split into individual words (tokens).

Example:

```text
I absolutely love this product!
```

becomes

```text
['i', 'absolutely', 'love', 'this', 'product']
```

#### Stopword Removal

Common words such as:

```text
the, is, and, of, a
```

were removed because they contribute little to sentiment understanding.

#### Lemmatization

Words were reduced to their root form.

Examples:

```text
running → run
cars → car
```

This reduced vocabulary size and improved consistency.

---

### 3. Sentiment Analysis

NLTK's VADER (Valence Aware Dictionary and sEntiment Reasoner) was used to evaluate the emotional tone of each review.

For every review, VADER generated:

* Positive Score
* Negative Score
* Neutral Score
* Compound Score

The Compound Score was used to classify sentiment:

| Compound Score         | Sentiment |
| ---------------------- | --------- |
| ≥ 0.05                 | Positive  |
| ≤ -0.05                | Negative  |
| Between -0.05 and 0.05 | Neutral   |

---

### 4. Sentiment Classification

Each review was assigned a sentiment category:

```python
Positive
Negative
Neutral
```

Additional columns were created:

* Compound_Score
* Predicted_Sentiment

allowing direct comparison between review ratings and sentiment predictions.

---

### 5. Data Visualization

#### Sentiment Distribution

A bar chart was created to visualize the number of:

* Positive Reviews
* Neutral Reviews
* Negative Reviews

This provided an overview of customer satisfaction levels.

---

#### Word Cloud Analysis

Word Clouds were generated to identify the most frequently occurring words.

Visualizations included:

* Overall Word Cloud
* Positive Review Word Cloud
* Negative Review Word Cloud

These helped reveal common themes within customer feedback.

---

## Key Findings

### Customer Satisfaction

The majority of reviews were classified as positive, indicating strong customer satisfaction across many products.

### Common Positive Themes

Frequently occurring positive words included:

* great
* love
* good
* delicious
* best

### Common Negative Themes

Frequently occurring negative words included:

* bad
* disappointed
* waste
* poor
* terrible

### Sentiment Insights

VADER successfully captured emotional patterns in customer reviews and assigned sentiment labels based on review text rather than star ratings alone.

---

## Challenges Encountered

Several challenges were encountered during the project:

* Parsing errors while loading the large dataset.
* Handling missing and malformed review records.
* Cleaning noisy text data.
* Processing large volumes of reviews efficiently.
* Understanding sentiment scoring and classification thresholds.

These challenges provided valuable hands-on experience with real-world NLP workflows.

---

## Conclusion

This project demonstrates the practical application of Natural Language Processing techniques to customer review analysis.

By combining text preprocessing, sentiment classification, and visualization, meaningful insights were extracted from thousands of customer reviews. The project strengthened my understanding of NLP concepts, text analytics, sentiment analysis, and data visualization using Python.

---

## Skills Demonstrated

* Natural Language Processing (NLP)
* Text Preprocessing
* Tokenization
* Stopword Removal
* Lemmatization
* Sentiment Analysis
* Data Cleaning
* Data Visualization
* Python Programming
* Exploratory Data Analysis (EDA)

---

## Author

Developed as part of my Data Analytics and Machine Learning learning journey and internship experience, focusing on practical applications of Natural Language Processing for customer feedback analysis.
