## Goal
Implement Graph Transformer-style logic from scratch using the NetworkX library.

## Why Not Use LangChain Graph Transformers Directly?
LangChain Graph Transformers are useful for fast prototyping, but they automatically infer entities, relationships, and graph structure from text. This is convenient, but it can reduce control over how features are defined and represented.

## Why NetworkX?
With NetworkX, we can explicitly define:
- Node types and attributes
- Edge types and relationship labels
- Business-specific rules for order, payment, and status workflows

This approach makes the graph design transparent, customizable, and easier to adapt to domain-specific requirements.