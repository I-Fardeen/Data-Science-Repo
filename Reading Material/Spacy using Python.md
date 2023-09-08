# Spacy for NLP using Python Cheat Sheet 📝🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of Natural Language Processing (NLP) with Spacy and Python! This cheat sheet is your essential guide to harnessing the power of Spacy for NLP tasks. Be sure to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more NLP insights and updates! 🙌

🚀 **Getting Started with Spacy**:
To begin your NLP journey with Spacy, make sure you have Spacy installed on your system.

```bash
pip install spacy
```

💼 **Loading Language Models**:
Load pre-trained language models for various languages with just a few lines of code.

```python
import spacy

# Load English language model
nlp = spacy.load('en_core_web_sm')

# Process text
doc = nlp("This is a sample text for NLP analysis.")
```

📊 **Basic NLP Tasks with Spacy**:
Perform common NLP tasks easily using Spacy.

- **Tokenization**:
```python
for token in doc:
    print(token.text)
```

- **Part-of-Speech Tagging**:
```python
for token in doc:
    print(token.text, token.pos_)
```

- **Named Entity Recognition (NER)**:
```python
for ent in doc.ents:
    print(ent.text, ent.label_)
```

🔍 **Dependency Parsing**:
Analyze sentence structure and relationships between words.

```python
for token in doc:
    print(token.text, token.dep_, token.head.text)
```

🧰 **Customizing Spacy**:
Train your own NER models or customize existing models.

```python
# Train NER
from spacy.pipeline.ner import EntityRecognizer

ner = EntityRecognizer(nlp.vocab)
ner.update(train_data)
```

📄 **Text Classification**:
Perform text classification tasks using Spacy.

```python
# Example: Sentiment analysis
text = "This movie is great!"
doc = nlp(text)
sentiment_score = doc.sentiment
```

📝 **Rule-Based Matching**:
Define custom rules to extract specific information from text.

```python
from spacy.matcher import Matcher

matcher = Matcher(nlp.vocab)
pattern = [{'LOWER': 'data'}, {'IS_PUNCT': True}, {'LOWER': 'science'}]
matcher.add('DataScience', [pattern])
```

🌐 **Multilingual NLP**:
Spacy supports various languages for NLP tasks.

```python
# Load a different language model
nlp_de = spacy.load('de_core_news_sm')
```

Now, you're well-equipped to dive into the exciting world of NLP with Spacy and Python. Happy NLP-ing! 📝🐍

Made with :heart: by **Fardeen Ahmad Khan**
