# 📊 Customer Sentiment & Feedback Analyzer

### 🚀 Project Overview
This project is a Data Analytics and Natural Language Processing (NLP) solution designed to understand customer sentiment from raw product reviews. By analyzing over **20,000+ Amazon product reviews**, this tool classifies customer feedback into **Positive**, **Neutral**, and **Negative** sentiments to uncover deeper insights beyond just "Star Ratings."

The goal was to determine if star ratings always align with written text and to identify patterns in how customers express dissatisfaction vs. delight.

---

### 🔑 Key Features & Insights
* **Data Cleaning Pipeline:** Processed unstructured text data by removing noise, stop words, and standardizing formats using **Pandas**.
* **Sentiment Scoring:** Implemented **NLP techniques (TextBlob)** to calculate sentiment polarity scores (-1 to +1) for each review.
* **Behavioral Analysis:** Discovered that **negative reviews are on average 40% longer** than positive reviews, indicating customers put more effort into describing bad experiences.
* **Visualizations:** Created interactive charts using **Seaborn** and **Matplotlib** to visualize the correlation between Star Ratings and Sentiment Scores.

---

### 🛠️ Technologies Used
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **NLP Analysis:** TextBlob, NLTK
* **Visualization:** Seaborn, Matplotlib
* **Environment:** Google Colab / Jupyter Notebook

---

### 📊 Visualizations

*(Place your screenshot of the "Sentiment Score vs Star Rating" bar chart here)*

> **Insight:** As shown in the chart above, while most 5-star reviews have high positive sentiment, there is a noticeable cluster of "Positive" text even in lower-rated reviews, suggesting some users leave low stars for delivery issues despite liking the product.

---

### 💻 How to Run This Project
You can run this analysis directly in your browser without installing anything using Google Colab.

1.  **Open the Notebook:**
    Click on the `Customer_Sentiment_Analysis.ipynb` file in this repository.

2.  **Launch in Colab:**
    Click the "Open in Colab" button (if available) or download the file and upload it to [Google Colab](https://colab.research.google.com/).

3.  **Run the Cells:**
    Execute the code cells step-by-step to see the data processing and graph generation in real-time.

---

### 📝 Sample Code Snippet
Here is how the sentiment polarity is calculated:

```python
from textblob import TextBlob

def get_sentiment(text):
    # Returns a value between -1 (Negative) and 1 (Positive)
    return TextBlob(text).sentiment.polarity

df['Sentiment_Score'] = df['Review_Text'].apply(get_sentiment)
