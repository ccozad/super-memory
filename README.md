# super-memory
A unified knowledge base service for agentic systems

# Introduction

Agentic systems need grounded context to perform business functions. `super-memory` aims to provide a turn key knowledge base management solution so teams can focus on their business logic and not the mechanics of storing and indexing data.

# Architecture

`super-memory` has a central knowledge store that you can add to and query. Different types of knowledge can be processed using plugins and processing capabilities can be extended by creating custom plugins.

Knowledge can take several forms
- Documents and files
- Media
- Communications
- Derrived facts

## Storage Backends

Content can be stored is various configurations including local storage and cloud storage options. What actually appears in storage will vary by knowledge type. In some cases the original content is stored and in other cases, especially for large content, only meta data is stored. Storage backends have options for encrypting content to protect data at rest.

## Knowledge Processors

Knowledge processors have logic to process specific types of data and make it searchable within the knowledge base.

## Query Providers

Query providers fulfill queries to identify the best matches in the knowledge base.
