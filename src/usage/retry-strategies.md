# Retry Strategies

Rubeus has a built-in mechanism to retry failed requests, eliminating the need for manual re-runs.
```bash
# Add the retry configuration to enable exponential back-off retries
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data-raw '{
    "config": {
        "mode": "single",
        "options": [{
            "provider": "openai",
            "retry": {
                "attempts": 3,
                "onStatusCodes": [429,500,504,524]
            }
        }]
    },
    "params": {
        "prompt": "What are the top 10 happiest countries in the world?",
        "max_tokens": 50,
        "model": "text-davinci-003",
        "user": "jbu3470"
    }
}'
```
