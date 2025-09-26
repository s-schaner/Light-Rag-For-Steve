FROM python:3.11-slim

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

RUN apt-get update && apt-get install -y --no-install-recommends \
    curl ca-certificates build-essential git && \
    rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir "lightrag-hku[api]" "python-dotenv"

WORKDIR /app

COPY config.ini /app/config.ini

EXPOSE 9621
