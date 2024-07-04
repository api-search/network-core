---
name: Ad
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/ad.png
url: https://example.com/apis/ad.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Ad
apis:
  - name: FactSet Digital Cards
    description: >-
      The FactSet Digital Cards API provides quick access to key company
      information and market data in an easily consumable and sharable format.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-digital-cards
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-digital-cards#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-digital-cards#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-digital-cards#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-digital-cards#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-digital-cards#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: FactSet Digital Cards API
            description: ''
          paths:
            /v1/company/{component}/adaptive-card:
              parameters:
                - null
                - null
                - null
                - null
              get:
                tags:
                  - Retrieve
                  - Multiple
                  - Digital
                  - Cards
                  - In
                  - Microsoft
                  - Adaptive
                  - Card
                  - Format.
                  - V1
                  - Company
                  - Component
                  - Adaptive
                  - Card
                summary: >-
                  Retrieve Multiple Digital Cards in Microsoft Adaptive Card
                  Format.
            /v1/company/{component}/adaptive-card/{id}:
              parameters:
                - null
                - null
              get:
                tags:
                  - Retrieve
                  - One
                  - Digital
                  - Card
                  - In
                  - Microsoft
                  - Ad
                  - V1
                  - Company
                  - Component
                  - Adaptive
                  - Card
                  - Id
                summary: Retrieve One Digital Card in Microsoft
    overlays:
      - type: APIs.io Search
        url: overlays/digital-cards-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/digital-cards-openapi-api-evangelist-ratings.yml
    aid: factset:factset-digital-cards
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---