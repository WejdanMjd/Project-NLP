# 🧠 NLP-Powered Review Analysis Project

This project leverages Natural Language Processing (NLP) and Transformer-based models to analyze Amazon product reviews. It covers three main tasks: sentiment classification, product category clustering, and review summarization using generative AI.

---

## 📌 1. Review Classification

### 🎯 Objective
Classify customer reviews into **positive**, **negative**, or **neutral** categories to help the company improve its products and services.

### 🛠️ Task
Develop a model that categorizes textual reviews into sentiment classes using pre-trained transformer-based models.

### ✅ Approach
- Used Transformer-based models (e.g., BERT) via Hugging Face to leverage powerful language representations.
- Focused on fine-tuning rather than training from scratch.

### 📊 Results
- **Test Accuracy**: 0.967
- **Test Precision**: 0.966
- **Test Recall**: 0.967
- **Test F1-Score**: 0.967

**Classification Report**:
          precision    recall  f1-score   support
 Negative       0.86      0.84      0.85       337
 Neutral        0.66      0.64      0.65       261
 Positive       0.99      0.99      0.99      6069


 Accuracy                           0.97      6667


---

## 📌 2. Product Category Clustering

### 🎯 Objective
Simplify the product dataset by clustering detailed product types into **4–6 broader meta-categories**.

### 🛠️ Task
Build a model that analyzes product names/descriptions and assigns them to high-level categories.

### ✅ Categories Identified
After analyzing the dataset, the following meta-categories were created:

| Meta Category                         | Number of Reviews |
|--------------------------------------|-------------------|
| Batteries & Accessories              | 12,071            |
| Tablets & E-readers                  | 6,486             |
| Fire Tablets & Kindle Devices        | 6,307             |
| Kids' Tablets & Educational Devices  | 6,084             |
| Smart Devices & Alexa                | 2,384             |

---

## 📌 3. Review Summarization Using Generative AI

### 🎯 Objective
Generate **blog-style summaries** per product category that highlight:
- Top products and their key differences
- Top complaints for each product
- Worst product and why it should be avoided

### 🛠️ Task
Develop a pipeline that automatically generates short articles from customer review data.

### ✅ Approach

#### ✅ Load Pre-trained Models
- `facebook/bart-large-cnn` for summarization
- `facebook/bart-large-mnli` for zero-shot classification

#### 🧩 Summarize Complaints
- `summarize_reviews()` condensed top negative reviews per product.

#### 🏷️ Extract Key Features
- `extract_features()` used zero-shot classification with labels like:
  - Battery
  - Performance
  - Durability
  - Price

#### 🌟 Identify Top & Worst Products
- Selected **Top 3** products based on positive reviews.
- Identified **Worst** product using negative review count.

#### 📝 Generate Articles
For each meta-category:
- Introduced top 3 products with their advantages and complaint summaries.
- Included the worst product and why it should be avoided.

### 📄 Output
The generated summaries act as **automated product recommendation articles** to help customers make informed purchasing decisions.

---

## 🚀 Tools & Libraries Used
- Python
- Hugging Face Transformers
- Scikit-learn
- Pandas / NumPy
- Jupyter Notebook
