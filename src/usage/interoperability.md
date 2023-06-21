# Interoperability
Rubeus allows you to switch between different language learning models from various providers, making it a highly flexible tool. The following example shows a request to `openai`, but you could change the provider name to `cohere`, `anthropic` or others and Rubeus will automatically handle everything else.

```bash
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data-raw '{
    "config": {
        "provider": "openai"
    },
    "params": {
        "prompt": "What are the top 10 happiest countries in the world?",
        "max_tokens": 50,
        "model": "text-davinci-003",
        "user": "jbu3470"
    }
}'
```