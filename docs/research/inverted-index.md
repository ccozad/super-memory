An inverted index is a foundational information retrieval data structure mapping content (e.g., words) to its locations within a document or dataset. It enables rapid full-text searching by creating a dictionary of terms and posting lists of document IDs where they appear, rather than scanning all documents sequentially. 

# Core Components

- **Dictionary (Vocabulary)**: A sorted list of unique terms/tokens extracted from the corpus.
- **Postings List**: A linked list or array associated with each term containing document IDs (and often term frequency or positions) where the term appears.

# Construction Process (Indexing)

- **Tokenization**: Splitting documents into individual words.
- **Preprocessing**: Lowercasing, removing punctuation, and removing stop words ("the", "is").
- **Stemming/Lemmatization**: Reducing words to their root form (e.g., "running" to "run").
- **Posting Creation**: Mapping unique terms to the document IDs, ordered by term for fast lookup.

# Key Advantages and Use Cases

- **Speed**: Provides sub-second lookup for keywords, crucial for search engines and databases.
- **Efficiency**: Efficiently handles large-scale text searching.
- **Usage**: Used in search engines (e.g., Apache Lucene/Elasticsearch), database full-text search, and RAG retrieval.

# Example

- Doc 1: "fast search"
- Doc 2: "fast data"

Inverted Index:
- fast -> [Doc 1, Doc 2]
- search -> [Doc 1]
- data -> [Doc 2]

# Optimizations

- Compression: Postings lists are often compressed to reduce storage.
- Ranking: Frequency information (TF-IDF) in postings is used to rank results.

# Resources

- https://sites.cs.ucsb.edu/~tyang_class/293s20f/slides/TopicIndexSimple.pdf
- https://course.khoury.northeastern.edu/cs6200sp15/slides/m04.s02%20-%20inverted%20indexes.pdf
