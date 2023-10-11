# ChromaDB Connector

Chroma is the open-source embedding database. Chroma makes it easy to build LLM apps by making knowledge, facts, and skills pluggable for LLMs.


Chroma gives you the tools to:

store embeddings and their metadata
embed documents and queries
search embeddings


## Authentication

ChromaDB Connector supports the following authentications:
1. API Key
2. Basic Auth

For this connector, we are defaulting to API Key authentication.

In order to set the API Key, you can set the following environment variable:

```bash
export CHROMA_SERVER_AUTH_CREDENTIALS="test-token"
export CHROMA_SERVER_AUTH_CREDENTIALS_PROVIDER="chromadb.auth.token.TokenConfigServerAuthCredentialsProvider"
export CHROMA_SERVER_AUTH_PROVIDER="chromadb.auth.token.TokenAuthServerProvider"
```

And then install and start the server,
    
    ```bash
    pip install chromadb
    chroma run --path /db_path 
    ```

This will start the chroma db in server mode and will be accessible at `http://localhost:8000`.
