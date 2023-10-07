# NLTK Library in Python Cheat Sheet 📚🐍

Welcome to the NLTK (Natural Language Toolkit) cheat sheet! NLTK is a powerful Python library for working with human language data. It provides easy-to-use interfaces to over 50 corpora and lexical resources. This cheat sheet will help you get started with NLTK and show you some code examples.

## Installation

You can install NLTK using pip:

```python
pip install nltk
```

## Code Examples

### Tokenization

```python
import nltk
from nltk.tokenize import word_tokenize

nltk.download('punkt')
text = "NLTK is a leading platform for building Python programs to work with human language data."
tokens = word_tokenize(text)
print(tokens)
```

### Stopwords Removal

```python
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize

nltk.download('stopwords')
nltk.download('punkt')

text = "NLTK is a powerful library for natural language processing in Python."
words = word_tokenize(text)
filtered_words = [word for word in words if word.lower() not in stopwords.words('english')]
print(filtered_words)
```

### Stemming

```python
from nltk.stem import PorterStemmer

stemmer = PorterStemmer()
word = "jumping"
stemmed_word = stemmer.stem(word)
print(stemmed_word)
```

### Lemmatization

```python
from nltk.stem import WordNetLemmatizer

nltk.download('wordnet')

lemmatizer = WordNetLemmatizer()
word = "running"
lemmatized_word = lemmatizer.lemmatize(word, pos='v')
print(lemmatized_word)
```

### Part-of-Speech Tagging

```python
from nltk import pos_tag
from nltk.tokenize import word_tokenize

nltk.download('averaged_perceptron_tagger')

text = "NLTK is great for natural language processing."
words = word_tokenize(text)
tags = pos_tag(words)
print(tags)
```

### Named Entity Recognition

```python
from nltk import ne_chunk
from nltk.tokenize import word_tokenize

nltk.download('maxent_ne_chunker')
nltk.download('words')

text = "Barack Obama was the 44th President of the United States."
words = word_tokenize(text)
entities = ne_chunk(pos_tag(words))
print(entities)
```

### Concordance

```python
from nltk.book import text1

text1.concordance("monstrous")
```

### Frequency Distribution

```python
from nltk import FreqDist
from nltk.book import text1

fdist = FreqDist(text1)
print(fdist.most_common(10))
```

This cheat sheet provides an overview of NLTK's core features and code examples to get you started. Explore the NLTK documentation for more details and capabilities.

📖 NLTK Documentation: [NLTK Documentation](https://www.nltk.org/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more data science and Python-related content. Enjoy your NLP journey with NLTK! 🐍📊📝
