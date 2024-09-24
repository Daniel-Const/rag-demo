# RAG Demo

Demo for RAG pattern combining search retrieval and LLM text generation.

[Code source](https://www.elastic.co/search-labs/blog/rag-with-llamaIndex-and-elasticsearch)

## Python setup 

```bash
# Setup virtual environment
> python -m venv .venv
> source .venv/bin/activate

# Install requirements
> pip install -r requirements.txt
```

## Elasticsearch

```bash
# Make sure service is running
systemctl start elasticsearch.service
```

## Ollama

[Install](https://ollama.com/)

```bash
# Make sure service is running
systemctl start ollama.service

# Download models locally
ollama run mistral
```

## Running demo

Run the indexing script to put the data into elasticsearch
```bash
python index.py
```

Run the query script to test a query on the data + generate the LLM response
```bash
python query.py
```

## Resources

- Original resource: https://www.elastic.co/search-labs/blog/rag-with-llamaIndex-and-elasticsearch
- Ollama: https://ollama.com/

## Examples in the wild

- Docker docs: https://docs.docker.com/ "Ask AI"
