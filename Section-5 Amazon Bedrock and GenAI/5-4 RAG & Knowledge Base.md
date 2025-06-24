### Amazon Bedrock - RAG & Knowledge Base
- RAG = Retrival-Augmented Generation
- Allows a foundation model to reference a data source outside of it's training data


#### How it works
- User sends a prompt to a Foundation Model
- Foundation Model will search relevant information in its Knowledge Base
- Knowledge Base can be embedded by the data from S3
- Knowledge Base is backed by vector database

### AWS RAG Vector Databases
- OpenSearch (Default Database) - search & analytics database real time similarity queries, store millions of vector embeddings, scalable index management, and far nearest neighbor (KNN) search capability
- Amazon Aurora - relational DB, proprietary to AWS
- Amazon RDS PostgreSQL - relational DB, open-source
- Amazon DocumentDB (with MongoDB compability) - NoSQL. High Performant, real time similarity queries
- Amazon Neptune - graph database

Others
    - MongoDB
    - Redis
    - Pinecone

### Amazon Bedrock - RAG Data Sources
- S3
- Confluence
- MS Sharepoint
- Salesforce
- Web Pages (your website, social media feed, etc...)
- More added overtime...


### How Embedding Works
- Sample source can be S3, Confluence etc...
- S3 objects will be converted to document chunks and it will be fed to embedding model
    - Embedding Models: Amazon Titan, or Cohere
- Embedding models will generate vectors and it will be saved to vector databases
- RAG will look from Vector Databses


### Use Cases for KB
- Customer Service Chatbot
    - Knowledge Base - e.g. FAQ
    - RAG Application - chatbot that can answer customer queries
- Legal Research and Analysis
- Healcare Question-Answering