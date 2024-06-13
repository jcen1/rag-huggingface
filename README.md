### This is the overview of logic flow of the code

### Pre-production Steps

#### Knowledge Base Preparation:
- **Chunking**: Split large documents into smaller parts for easier handling.
- **Embedding**: Convert these chunks into numerical representations (embeddings) using an embedding model.

#### Vector Database:
- Store the embeddings in a vector database for fast retrieval.

### In-production Steps (Query Handling)

#### Retriever:
- **User Query Embedding**: When a user asks a question, the system converts (embeds) the question into a numerical format.
- **Document Retrieval**: It finds the most similar documents in the vector database by comparing the embeddings.
- **Top K Similar Documents**: Selects the top K documents that are most relevant to the query.
- **Optional Rerankings**: Selects the top K documents that are most relevant to the query.

#### Reader:
- **Context Creation**: Combines the user query with the retrieved documents to create a context.
- **LLM Prompt**: Builds a prompt using this context and the user query.
- **Answer Generation**: Uses a language model (LLM) to generate an answer based on the prompt.

Please view the entire notebook on Kaggle: https://www.kaggle.com/code/jianiancen/rag-huggingface

Utlized Kaggle GPU T4 
