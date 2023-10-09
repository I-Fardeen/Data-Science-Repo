# Gensim Library in Python Cheat Sheet 📚✨

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Gensim cheat sheet! Gensim is a popular Python library for natural language processing and topic modeling. It's widely used for building topic models, document similarity analysis, and more. Whether you're a beginner or an expert in NLP, this cheat sheet will help you get started with Gensim and includes some code examples to empower your text analysis projects.

## Installation

You can install Gensim using pip:

```python
pip install gensim
```

## Code Examples

### Creating a Word2Vec Model

```python
from gensim.models import Word2Vec

# Example sentences
sentences = [
    ["machine", "learning", "is", "fun"],
    ["deep", "learning", "is", "exciting"],
    ["natural", "language", "processing", "is", "cool"]
]

# Create and train a Word2Vec model
model = Word2Vec(sentences, vector_size=100, window=5, min_count=1, sg=0)

# Find the vector representation of a word
vector = model.wv['machine']
print(vector)
```

### Creating a Doc2Vec Model

```python
from gensim.models import Doc2Vec
from gensim.models.doc2vec import TaggedDocument

# Example documents
documents = [TaggedDocument(doc, [i]) for i, doc in enumerate(sentences)]

# Create and train a Doc2Vec model
model = Doc2Vec(documents, vector_size=100, window=2, min_count=1, epochs=20)

# Infer the vector representation of a document
vector = model.infer_vector(["machine", "learning", "is", "fun"])
print(vector)
```

### Building a Topic Model with LDA

```python
from gensim import corpora
from gensim.models import LdaModel

# Example documents
documents = [
    "machine learning is fun and exciting",
    "natural language processing is cool",
    "topic modeling is interesting"
]

# Tokenize the documents
tokens = [document.split() for document in documents]

# Create a dictionary and a corpus
dictionary = corpora.Dictionary(tokens)
corpus = [dictionary.doc2bow(token) for token in tokens]

# Build an LDA model
lda_model = LdaModel(corpus, num_topics=2, id2word=dictionary, passes=10)

# Print the topics
for topic in lda_model.print_topics():
    print(topic)
```

### Similarity Queries

```python
from gensim import similarities

# Create a similarity index
index = similarities.MatrixSimilarity(lda_model[corpus])

# Query for similarity
query = "machine learning is exciting"
query_bow = dictionary.doc2bow(query.split())
sims = index[lda_model[query_bow]]

# Print document similarities
for document, similarity in enumerate(sims):
    print(f"Document {document + 1}: Similarity = {similarity:.4f}")
```

This cheat sheet provides a glimpse into Gensim's capabilities and code examples to get you started. Gensim is a powerful library for NLP and text analysis, and you can explore its detailed documentation for more advanced usage.

📖 Gensim Documentation: [Gensim Documentation](https://radimrehurek.com/gensim/)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more data science and Python-related content. Enjoy your journey into the world of natural language processing with Gensim! 📊📝📖
