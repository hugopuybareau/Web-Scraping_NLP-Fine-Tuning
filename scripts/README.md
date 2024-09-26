Tech News Article Generator
This project is a Tech News Article Generator that scrapes tech news titles from websites such as Financial Times, and automatically generates full-length articles in French using advanced NLP models like BART from Hugging Face. The goal is to automate content generation for tech news articles, making it easier to keep up with trends by generating high-quality content from minimal input.

Features
Web Scraping: Scrapes tech-related news titles from the Financial Times.
NLP-Based Generation: Uses Hugging Face's BART model to generate full articles based on scraped titles.
French Language Support: Generates the articles directly in French.
Customizable: The length of the articles and the style can be adjusted by changing the generation parameters.
How It Works
Scrape Titles: The script scrapes tech news titles from Financial Times using BeautifulSoup and requests.
Generate Articles: For each title, a prompt is passed to a BART model which generates a full-length article.
Output: The generated articles are displayed or stored for further use.
Prerequisites
Before running the project, ensure you have the following dependencies installed:

Python 3.7+
pip (Python package installer)
Hugging Face Transformers library
BeautifulSoup and requests for web scraping
