# Unified API Signature

If you're familiar with OpenAI's API, you'll find Rubeus's API easy to use due to its unified signature.
```bash
# OpenAI query
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data-raw '{
    "config": {
        "provider": "openai"
    },
    "params": {
        "prompt": "What are the top 10 happiest countries in the world?",
        "max_tokens": 50,
        "user": "jbu3470"
    }
}'

# Anthropic Query
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data-raw '{
    "config": {
        "provider": "anthropic"
    },
    "params": {
        "prompt": "What are the top 10 happiest countries in the world?",
        "max_tokens": 50,
        "user": "jbu3470"
    }
}'
```