# Load Balancing

Manage your workload effectively with Rubeus's custom weight-based distribution across multiple API keys or providers.
```bash
# Load balance 50-50 between gpt-3.5-turbo and claude-v1
curl --location 'http://127.0.0.1:8787/complete' \
--header 'Content-Type: application/json' \
--data '{
    "config": {
        "mode": "loadbalance",
        "options": [{
            "provider": "openai",
            "weight": 0.5,
            "params_to_override": { "model": "gpt-3.5-turbo" }
        }, {
            "provider": "anthropic",
            "weight": 0.5,
            "params_to_override": { "model": "claude-v1" }
        }]
    },
    "params": {
        "messages": {"role": "user","content":"What are the top 10 happiest countries in the world?"},
        "max_tokens": 50,
        "user": "jbu3470"
    }
}'
```