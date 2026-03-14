Apache Lucene is a high-performance, full-featured, open-source search engine library written entirely in Java. It is not a standalone application, but rather a code library and API designed for developers to add search capabilities to applications. It is widely considered the de facto standard for search libraries, powering major search platforms like Elasticsearch, OpenSearch, and Apache Solr.

# Key Features and Capabilities

- **Inverted Index**: Lucene uses an inverted index architecture, allowing for fast, full-text searches across large volumes of data by mapping terms to the documents that contain them.
- **High Performance**: It is capable of indexing over 800GB/hour on modern hardware and has small RAM requirements.
- **Advanced Search**: Supports diverse query types including phrase, wildcard, fuzzy (edit distance), proximity, and range queries.
- **Relevance Scoring**: Lucene provides ranked results, meaning it ranks documents by relevance to the search query using models like TF-IDF or BM25.
- **Analyzers**: It tokenizes text, removes stop words, and lowercases words to create efficient indices.
- **Cross-Platform**: While written in Java, it is cross-platform, and ports exist for other languages (e.g., PyLucene for Python, Lucene.NET).

# How It Works

Lucene breaks down text into smaller, indexable units called tokens through an Analyzer class. These tokens are then indexed in an "inverted index" via an IndexWriter.

- **Documents & Fields**: Data is indexed as Documents, which are collections of Fields (e.g., title, content, date).
- **Storage**: Lucene doesn't just index text; it can store raw data, allowing it to be retrieved during search results.
- **Concurrency**: It supports concurrent updates and searches.

# Lucene vs. Search Servers (Solr/Elasticsearch)

- **Lucene** is the core library (the engine).
- **Elasticsearch/Solr** are full search servers (the car) built on top of Lucene that add capabilities like distributed searching, REST APIs, and easy scaling.
Use Lucene directly if you need an embedded, low-level search within a Java app; use Solr/Elasticsearch for large-scale, distributed web applications.

# Resources

- https://web.cs.ucla.edu/classes/winter15/cs144/projects/lucene/index.html
- https://lucene.apache.org/core/