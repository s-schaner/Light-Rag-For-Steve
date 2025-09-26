FROM python:3.11-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
    curl ca-certificates build-essential git \
    && rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir "lightrag-hku[api]" \
    && pip install --no-cache-dir "python-dotenv"

WORKDIR /app
RUN mkdir -p /app/data/inputs /app/data/workspace

COPY config.ini /app/config.ini

EXPOSE 9621
