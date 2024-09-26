# **Tech News Generation Project**

This project aims to scrape tech news headlines from multiple websites, process the data, and fine-tune a BART (Bidirectional and Auto-Regressive Transformers) model to automatically generate full articles in French based on the scraped headlines.

## **Project Objectives**

The main goal of this project is to develop an automated system that generates full tech articles in French based on headlines scraped from various news sources. To achieve this, I utilized Natural Language Processing (NLP) techniques, including model fine-tuning with datasets constructed from real-world news articles.

## **Main Steps**

### 1. **Data Collection and Scraping**

Data was collected by scraping tech news headlines and articles from various sources using tools such as `newspaper3k`. Key steps included:
- **Scraping**: Automated collection of headlines and URLs from multiple tech news websites.
- **Content Extraction**: Using the `newspaper3k` library to extract full-text content from the URLs.
- **Data Cleaning**: Filtering and cleaning the scraped content to ensure completeness.

### 2. **Data Preprocessing**

In this phase, the headlines and articles were processed for use in model training:
- **Tokenization**: Text data was tokenized using the BART tokenizer, converting headlines and articles into tokenized input-output pairs.
- **Data Formatting**: The data was formatted into a CSV file with two main columns: `title` (headlines) and `content` (articles), and then converted into a Hugging Face dataset for training.

### 3. **Model Fine-Tuning**

A pre-trained BART model was fine-tuned on the collected tech news dataset:
- **Model**: Hugging Face's BART was fine-tuned on the dataset for sequence-to-sequence tasks (headline-to-article generation).
- **Training**: The model was trained on a dataset split into training and validation sets using Hugging Face’s Trainer API.
- **Evaluation**: After training, the model was evaluated on the validation set to measure its performance in generating coherent, relevant articles.

### 4. **Results and Conclusion**

The fine-tuned model was able to generate full-length articles in French based on the headlines. The performance improved after fine-tuning, showing coherent and grammatically correct outputs for most of the test headlines.

## **Future Improvements**

- **Increase Dataset Size**: Scrape more articles to build a larger dataset for further fine-tuning.
- **Model Optimization**: Experiment with different transformer models (e.g., T5, GPT-2) and further optimize hyperparameters.
- **Fine-Tune with Domain-Specific Data**: Incorporate more domain-specific articles from different tech sectors (e.g., AI, cybersecurity) to improve relevance.
