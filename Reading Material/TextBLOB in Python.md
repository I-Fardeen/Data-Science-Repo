# TextBlob Cheat Sheet 📝🤖

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the TextBlob cheat sheet! TextBlob is a powerful Python library for processing textual data. It provides simple API calls for common natural language processing (NLP) tasks, making it an excellent tool for sentiment analysis, part-of-speech tagging, noun phrase extraction, and more.

## Installation

You can install TextBlob using pip:

```bash
pip install textblob
```

You'll also need to install the corpora:

```bash
python -m textblob.download_corpora
```

## Importing TextBlob

Import TextBlob and other necessary modules:

```python
from textblob import TextBlob
```

## Basic Usage

### 1. Creating a TextBlob

Create a TextBlob object from text:

```python
text = "TextBlob is a fantastic library for natural language processing."
blob = TextBlob(text)
```

### 2. Tokenization

Tokenize sentences and words:

```python
# Tokenize into sentences
sentences = blob.sentences

# Tokenize into words
words = blob.words
```

### 3. Part-of-Speech Tagging

Perform part-of-speech tagging:

```python
tags = blob.tags
```

### 4. Noun Phrase Extraction

Extract noun phrases:

```python
noun_phrases = blob.noun_phrases
```

### 5. Sentiment Analysis

Analyze sentiment (returns a polarity and subjectivity score):

```python
sentiment = blob.sentiment
```

### 6. Language Translation

Translate text to another language:

```python
translated_blob = blob.translate(to='es')  # Translate to Spanish
```

## Advanced Usage

### 7. Word Inflection and Lemmatization

Inflect and lemmatize words:

```python
word = "running"

# Inflect to past tense
inflected_word = Word(word).lemmatize("v", "prt")

# Lemmatize
lemma = Word(word).lemmatize()
```

### 8. Spelling Correction

Correct spelling mistakes:

```python
text_with_mistake = "NLP is a powrful tool for data scientits."
corrected_blob = TextBlob(text_with_mistake).correct()
```

### 9. Define Word

Get the definition of a word:

```python
definition = Word("python").definitions
```

### 10. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and NLP content.

TextBlob simplifies natural language processing in Python, making it accessible for various tasks. Explore the versatility of TextBlob for your text analysis needs! 📝🤖✨

Made with :heart: by **Fardeen Ahmad Khan**
