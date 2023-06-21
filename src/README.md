# Introduction

<img src="/images/header.png" width=2000>

<div align="center">
  
<!--[![npm version](https://badge.fury.io/js/rubeus.svg)](https://badge.fury.io/js/rubeus)
[![Build Status](https://travis-ci.com/yourusername/rubeus.svg?branch=master)](https://travis-ci.com/yourusername/rubeus)
[![Coverage Status](https://coveralls.io/repos/github/yourusername/rubeus/badge.svg?branch=master)](https://coveralls.io/github/yourusername/rubeus?branch=master)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) -->

</div>

**Rubeus** is an unopionionated edge worker for buliding with Large Language Models (LLMs). Catering to a range of LLM providers, Rubeus extends beyond a unified API, becoming a powerful ally that expertly handles retries, fallbacks, and load distribution. The essence of Rubeus isn't merely about initiating requests—it's about ensuring these requests are handled intelligently and efficiently. With Rubeus, you're harnessing the power of language models, Axios-style! 💼🚀 

## Key Features

* [🌐 **Interoperability:**](/usage/interoperability.md) Write once, run with any provider. Switch between __ models from __ providers seamlessly.
* [🔀 **Fallback Strategies:**](/usage/fallback-strategies.md) Don't let failures stop you. If one provider fails, Rubeus can automatically switch to another.
* [🔄 **Retry Strategies:**](/usage/retry-strategies.md) Temporary issues shouldn't mean manual re-runs. Rubeus can automatically retry failed requests.
* [⚖️ **Load Balancing:**](/usage/load-balancing.md) Distribute load effectively across multiple API keys or providers based on custom weights.
* [📝 **Unified API Signature:**](/usage/unified-api-signature.md) If you've used OpenAI, you already know how to use Rubeus with any other provider.
<br>

### Supported Providers

| Provider  | Support Status  | Supported Endpoints |
|---|---|---|
| <img src="/images/openai.png" width=18> OpenAI | <img src="/images/heavy_check_sign.png" width=25 align=center> Supported  | `/completion`, `/embed` |
| <img src="/images/anthropic.png" width=18> Anthropic  | <img src="/images/heavy_check_sign.png" width=25 align=center> Supported  | `/complete` |
| <img src="/images/cohere.png" width=18> Cohere  | <img src="/images/heavy_check_sign.png" width=25 align=center> Supported  | `generate`, `embed` |
| <img src="/images/bard.png" width=18> Google Bard  | <img src="/images/coming_soon.png" width=30 align=center> Coming Soon  |  |
| <img src="/images/localai.png" width=18> LocalAI  | <img src="/images/coming_soon.png" width=30 align=center> Coming Soon  |  |







