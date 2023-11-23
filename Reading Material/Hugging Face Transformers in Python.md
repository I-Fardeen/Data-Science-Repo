# Hugging Face Transformers in Python Cheat Sheet 🤗🐍

Welcome to the Hugging Face Transformers in Python cheat sheet! Hugging Face Transformers is a powerful library for natural language processing (NLP), offering a wide range of pre-trained models and tools for various NLP tasks. Explore this cheat sheet to unleash the potential of Hugging Face Transformers with essential concepts and code examples.

## Installation

Install Hugging Face Transformers using pip:

```bash
pip install transformers
```

## Importing Hugging Face Transformers

Import Hugging Face Transformers in your Python script or Jupyter notebook:

```python
from transformers import pipeline, AutoModelForSequenceClassification, AutoTokenizer
```

## Basic Concepts

### 1. Text Classification

Perform text classification with a pre-trained model:

```python
# Load pre-trained model and tokenizer
model_name = "bert-base-uncased"
model = AutoModelForSequenceClassification.from_pretrained(model_name)
tokenizer = AutoTokenizer.from_pretrained(model_name)

# Text classification pipeline
classifier = pipeline("sentiment-analysis", model=model, tokenizer=tokenizer)
result = classifier("I love using Hugging Face Transformers!")
```

### 2. Named Entity Recognition (NER)

Extract entities from text:

```python
# Named Entity Recognition pipeline
ner_pipeline = pipeline("ner", model=model, tokenizer=tokenizer)
result = ner_pipeline("Hugging Face is a fantastic library for NLP.")
```

### 3. Translation

Translate text from one language to another:

```python
# Translation pipeline
translator = pipeline("translation", model=model, tokenizer=tokenizer)
result = translator("Hello, how are you?", src="en", tgt="fr")
```

### 4. Text Summarization

Generate a summary for a given text:

```python
# Summarization pipeline
summarizer = pipeline("summarization", model=model, tokenizer=tokenizer)
result = summarizer("Hugging Face Transformers is a powerful NLP library.")
```

### 5. Text Generation

Generate text using a pre-trained language model:

```python
# Text generation pipeline
generator = pipeline("text-generation", model=model, tokenizer=tokenizer)
result = generator("Once upon a time, in a land far, far away...")
```

### 6. Question Answering

Answer questions based on a given context:

```python
# Question answering pipeline
qa_pipeline = pipeline("question-answering", model=model, tokenizer=tokenizer)
result = qa_pipeline({
    "question": "What is Hugging Face Transformers?",
    "context": "Hugging Face Transformers is a library for natural language processing."
})
```

## Advanced Usage

### 7. Fine-Tuning

Fine-tune a pre-trained model for specific tasks:

```python
# Fine-tuning example
# (Refer to Hugging Face documentation for detailed fine-tuning procedures)
```

### 8. Custom Model Loading

Load a custom pre-trained model:

```python
# Load a custom pre-trained model and tokenizer
custom_model_name = "your-custom-model-name"
custom_model = AutoModelForSequenceClassification.from_pretrained(custom_model_name)
custom_tokenizer = AutoTokenizer.from_pretrained(custom_model_name)
```

### 9. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and NLP-related content.

Explore the world of natural language processing with Hugging Face Transformers in Python! 🌐🤖💬
