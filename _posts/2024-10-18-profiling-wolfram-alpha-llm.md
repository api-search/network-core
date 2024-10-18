---
layout: post
title: 'Profiling Wolfram Alpha LLM API'
image: https://kinlane-productions2.s3.amazonaws.com/apis-io/wolfram-alpha-llm-api-screenshot.png
tags:
    - LLM
    - Artificial Intelligence
    - AI
---
[I recently profiled the Wolfram Alpha LLM API](https://github.com/api-search/wolfram-alpha/blob/main/apis.yml). There are [additional APIs to be profiled](https://products.wolframalpha.com/llm-api/documentation), but I wanted to get this one in the system so we could use as part of other work.

One thing I tested with this one was the ability for ChatGPT to generate an OpenAPI if I pasted specific content from the [Wolfram Alpha LLM API page](https://products.wolframalpha.com/llm-api/documentation). It did a really good job producing the [OpenAPI](https://github.com/api-search/wolfram-alpha/blob/main/openapi.yml) in the repo and is something I will continue to use and automate around.

You can visit [the APIs.yml and OpenAPI over at the GitHub repository for Wolfram Alpha LLM API](https://github.com/api-search/wolfram-alpha/blob/main/apis.yml), and we will keep adding other APIs and common properties for Wolfram Alpha LLM API as time allows.