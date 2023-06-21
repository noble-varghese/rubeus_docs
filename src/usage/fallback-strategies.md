# Fallback Strategies
In case one provider fails, Rubeus is designed to automatically switch to another, ensuring uninterrupted service.

```bash
# Fallback to anthropic, if openai fails (This API will use the default text-davinci-003 and claude-v1 models)
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data-raw '{
    "config": {
        "mode": "fallback",
        "options": [
          {"provider": "openai"}, 
          {"provider": "anthropic"}
        ]
    },
    "params": {
        "prompt": "What are the top 10 happiest countries in the world?",
        "max_tokens": 50,
        "user": "jbu3470"
    }
}'

```

<br>

```bash
# Fallback to gpt-3.5-turbo when gpt-4 fails
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data-raw '{
    "config": {
        "mode": "fallback",
        "options": [
          {"provider": "openai", "params_to_override": {"model": "gpt-4"} }, 
          {"provider": "anthropic", "params_to_override": {"model": "gpt-3.5-turbo"} }
        ]
    },
    "params": {
        "messages": {"role": "user", "content": "What are the top 10 happiest countries in the world?"},
        "max_tokens": 50,
        "user": "jbu3470"
    }
}'
```
