# Sentiment Analysis of Yelp Reviews

This project demonstrates how to perform sentiment analysis on Yelp reviews using a pre-trained BERT model.

## Setup and Installation

Ensure you have Python installed. Install the necessary packages using pip:

```bash
pip install torch torchvision torchaudio transformers requests beautifulsoup4 pandas numpy
```

## Model Overview

We utilize the nlptown/bert-base-multilingual-uncased-sentiment model from Hugging Face, which can classify text into 5 sentiment categories.

Running the Script
1.	Instantiate the Model: Load the pre-trained BERT model and tokenizer.
2.	Collect Yelp Reviews: Scrape reviews from Yelp using requests and BeautifulSoup.
3.	Sentiment Analysis: Analyze the sentiment of the collected reviews and store the results in a DataFrame.

## Example
```
tokens = tokenizer.encode('This was a decent place to eat', return_tensors='pt')
result = model(tokens)
print(int(torch.argmax(result.logits)) + 1)  # Outputs the sentiment score
```

## Output

The script scrapes Yelp reviews, analyzes sentiment, and outputs a DataFrame with review texts and their respective sentiment scores.