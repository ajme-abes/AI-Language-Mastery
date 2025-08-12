# NLP

- NLP is a field that focuses on making natural  human language usable by computer programs

# NLTK

- is a python package that we use for NLP

### Tokenizing

- **the process of breaking down a larger piece of data, like a sentence or a text file, into smaller units called tokens**

### stop word Filtering

- **Stop words** are words that you want to ignore, so you filter them out of your text when you’re processing it
- commonly used word in language , such as  preposition, article  and conjunction , that are filtered out during text processing task like NLP and search engine algorithms

Purpose:

- to improve efficiency and accuracy of text analysis
- Common examples of stop words include:
    - **Articles:** the, a, an
    - **Prepositions:** in, on, at, with, to
    - **Conjunctions:** and, but, or
    - **Pronouns:** he, she, it, they
    - **Auxiliary verbs:** is, am, are, was, were
    
    Here’s how to import the relevant parts of NLTK in order to filter out stop words:
    
    ```python
    nltk.download("stopwords")
    from nltk.corpus import stopwords
    from nltk.tokenize import word_tokenize
    ```
    

## Stemming

- is a text processing task which  we  reduce words to their root,  which its a core part of the words . For example, the words “helping” and “helper” share the root “help.”

Here’s how to import the relevant parts of NLTK in order to start stemming:

```python
from nltk.stem import PorterStemmer
from nltk.tokenize import word_tokenize
```

Understemming and overstemming are two ways stemming can go wrong:

- **Understemming** happens when two related words should be reduced to the same stem but aren’t. This is a [false negative](https://en.wikipedia.org/wiki/False_positives_and_false_negatives#False_negative_error).
- **Overstemming** happens when two unrelated words are reduced to the same stem even though they shouldn’t be. This is a [false positive](https://en.wikipedia.org/wiki/False_positives_and_false_negatives#False_negative_error).

### **Tagging Parts of Speech**

- POS tagging is the process of assigning a **grammatical category** (part of speech) to each word in a sentence
- **POS tagging**, is the task of labeling the words in your text according to their part of speech.

for importing POS tagging 

```python
from nltk.tokenize import word_tokenize
#Now call nltk.pos_tag() on your new list of words:
nltk.pos_tag()
```

Here’s how to get a list of tags and their meanings:

1. download tagsets and tagsets_json
2. meaning

```python
import nltk
nltk.download('tagsets')
nltk.download('tagsets_json')
#getting meaning
nltk.help.upenn_tagset()
```

### Lemmatization

- **Lemmatization** reduces a word to its **dictionary base form** (called the *lemma*), considering the word’s **part of speech and grammar**
- Notes: A **lemma** is a word that represents a whole group of words, and that group of words is called a **lexeme**.

### Chunking

- While tokenizing allows you to identify words and sentences, **chunking** allows you to identify **phrases**.
- Chunking makes use of POS tags to group words and apply chunk tags to those groups.
- Chunks don’t overlap, so one instance of a word can be in only one chunk at a time.

**Purpose:**

- Chunking aims to add more structure to a sentence by identifying and grouping related words, allowing for better understanding and extraction of information. It's a stepping stone towards full parsing but offers a less computationally intensive approach for tasks like named entity recognition, information extraction, and text summarization.

**Process:**

- Tokenize
- Pos tag
- chunking

```python
    import nltk

    sentence = "The quick brown fox jumps over the lazy dog."
    tokens = nltk.word_tokenize(sentence)
    tagged = nltk.pos_tag(tokens)

    # Define a grammar for noun phrases (NP)
    grammar = r"""
      NP: {<DT>?<JJ>*<NN.*>+}  # Chunk a determiner, zero or more adjectives, and one or more nouns
    """
    cp = nltk.RegexpParser(grammar)
    result = cp.parse(tagged)

    print(result)
```