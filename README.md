# Light-Rag-For-Steve

This repository provides a dead-simple containerized stack for running LightRAG alongside Ollama. The setup builds a custom LightRAG image, uses Ollama for both chat and embedding models, and exposes both services on localhost for quick experimentation.

## Stack layout

```
lightrag-ollama-stack/
├─ docker-compose.yml
├─ .env
├─ lightrag/
│  ├─ Dockerfile
│  └─ config.ini
└─ data/
   ├─ inputs/
   └─ workspace/
```

## Usage

1. From `lightrag-ollama-stack/`, start the stack:
   ```bash
   docker compose up -d
   ```
2. Access the services:
   * Ollama API at http://localhost:11434
   * LightRAG API & Web UI at http://localhost:9621
3. Drop documents into `data/inputs/` to ingest via the API or Web UI.
4. Stop the stack when finished:
   ```bash
   docker compose down
   ```

See `docker-compose.yml` and `lightrag/config.ini` for configuration details, including model selections and runtime options.
