# Project Overview

This repository contains several models for review analysis, classification, summarization, and product category clustering. The models were developed to help classify customer reviews, summarize them into recommendations, and cluster products into broader categories.

## Tasks and Models

### 1. **Summarize Reviews Using Generative AI**
**Objective**: Summarize customer reviews into articles that recommend the top products for each category.  
**Task**: Create a model that generates a short article (like a blog post) for each product category. The output should include:
- Top 3 products and key differences between them.
- Top complaints for each of those products.
- Worst product in the category and why it should be avoided.

**Model Details**:
- Used Hugging Face pipelines for summarization and zero-shot classification.
- Models used: `facebook/bart-large-cnn` for summarization and `facebook/bart-large-mnli` for zero-shot classification.
  
**🔗 [Download Summarization Model](https://drive.google.com/drive/folders/1GY1X3MlJdLwT0Z3AvYlF3qX6HQLklNIM?usp=sharing)**

---

### 2. **Review Classification**
**Objective**: Classify customer reviews into positive, negative, or neutral categories to help the company improve its products and services.  
**Task**: Create a model for classifying the textual content of reviews into these three categories.

**Model Details**:
- Pretrained transformer-based models were used to classify reviews without training from scratch.
  
**Model Performance**:
- **Test Accuracy**: 96.69%
- **Test Precision**: 96.63%
- **Test Recall**: 96.69%
- **Test F1**: 96.66%

**🔗 [Download Classification Model](https://drive.google.com/drive/folders/12wTnJYTGPD2kGWeK0HQxWJoZDrcOrvio?usp=sharing)**

---

### 3. **Product Category Clustering**
**Objective**: Simplify the dataset by clustering product categories into 4-6 meta-categories.  
**Task**: Create a model to group all reviews into broader categories like:
- Ebook readers
- Batteries
- Accessories (keyboards, laptop stands, etc.)
- Non-electronics (e.g., Nespresso pods, pet carriers)

**Model Details**:
- Clustering was done using unsupervised machine learning techniques.
  
**Clustering Output**:
- Batteries & Accessories: 12,071 reviews
- Tablets & E-readers: 6,486 reviews
- Fire Tablets & Kindle Devices: 6,307 reviews
- Kids' Tablets & Educational Devices: 6,084 reviews
- Smart Devices & Alexa: 2,384 reviews
  
**🔗 [Download Clustering Model](https://drive.google.com/drive/folders/1oq3xv1DYC_9xPRvqUDNm5CJ4jSBACGmq?usp=sharing)**

---

### Additional Files

- 📥 [Download Final Review Summarization Notebook](https://drive.google.com/file/d/1RIxg4j6q8WuXjZNHOh-s2iQC49HWOyQA/view?usp=sharing)

---

## How to Use

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/WejdanMjd/Project-NLP.git
