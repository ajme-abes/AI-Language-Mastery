# Spacy

- spacy is free and open source library for NLP

### Linguistic annotations

- They are **tags or metadata** attached to text that describe its **linguistic properties**.
- These annotations help NLP models understand grammar, syntax, semantics, and more.

### 🧬 2. Core Concepts

| Concept | Description |  |
| --- | --- | --- |
| `Doc` | Container for processed text |  |
| `Token` | Individual word or punctuation |  |
| `Span` | Slice of `Doc` (e.g., sentence or entity) |  |
| `Pipeline` | Sequence of components (e.g., tokenizer → tagger → parser → NER) |  |

### 📦 What Is a `Doc` in spaCy?

A `Doc` object is created when you pass text through a spaCy **language model** (like `en_core_web_sm`). It contains:

- The original text
- Tokenized words
- Part-of-speech tags
- Named entities
- Dependency parse
- Lemmas
- Sentence boundaries
- And more!

### Token Attribute

- .txt
- .head
- .left_edge
- .right_Edge
- .ent_type_
- .iob_
- .lemma_
- .morph
- .pos_
- .dep_
- .lang_

### 🧠 spaCy vs. NLTK: Key Differences

| Feature / Aspect | **spaCy** 🧬 | **NLTK** 📚 |
| --- | --- | --- |
| **Purpose** | Industrial-strength NLP library | Educational and research-focused |
| **Ease of Use** | Streamlined, Pythonic API | More granular, academic-style APIs |
| **Speed** | Very fast, optimized for production | Slower, not optimized for speed |
| **Pretrained Models** | Built-in models (POS, NER, etc.) | Requires external models or training |
| **NER (Named Entity Recognition)** | High-quality, pretrained NER | Basic NER, often needs customization |
| **POS Tagging** | Accurate and fast | Decent, but less robust |
| **Dependency Parsing** | Built-in and efficient | Not natively supported |
| **Text Classification** | Custom pipelines via training | Manual implementation required |
| **Tokenization** | Rule-based and language-specific | Regex-based, customizable |
| **Training Capabilities** | Supports model training (NER, etc.) | Limited training support |
| **Visualization** | `displacy` for syntax and entities | No built-in visualization tools |
| **Integration with Transformers** | Yes (`spacy-transformers`) | No direct integration |
| **Learning Curve** | Easier for developers | Better for academic exploration |
| **Use Case** | Production apps, real-time NLP | Teaching, prototyping, linguistics |

### 🧪 Summary

- **Use spaCy** if you're building real-world applications, need speed, and want pretrained models with modern NLP features.
- **Use NLTK** if you're exploring linguistic theory, building from scratch, or learning NLP fundamentals.