---
name: Adaptive
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/adaptive.png
url: https://example.com/apis/adaptive.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Adaptive
apis:
  - name: FactSet Signals API
    description: >-
      Leverage Signals to identify material events for a company. Signals are
      derived from FactSet's core data,  cognitive computing technology, and our
      3rd party partners. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/signals-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/signals-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/signals-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/signals-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/signals-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/signals-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.2
          info:
            title: Signals API
          tags:
            - name: Events
              description: >-
                Fetch signal events. Please note that FactSet Cognitive signals
                and signals contributed by third parties are excluded from the
                response for limited API access.
            - name: Metadata
              description: Fetch signal metadata
          paths:
            /events/headlines:
              get:
                tags:
                  - Events
                  - Headlines
                description: >-
                  Fetch Signals event headlines based on at least one of the
                  following filtering parameters: `ids`, `portfolios`
              post:
                tags:
                  - Events
                  - Headlines
                description: >-
                  Fetch Signals event headlines based on the filtering criteria
                  for up to 1000 identifiers and at least one of the following
                  filtering parameters: `ids`, `portfolios`
            /events/details:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                description: >-
                  Fetch Signals event headlines plus all additional event
                  details based on at least one of the following filtering
                  parameters: `ids`, `portfolios`
              post:
                tags:
                  - Events
                  - Headlines
                  - Details
                description: >-
                  Fetch Signals event headlines plus all additional event
                  details for up to 1000 identifiers and at least one of the
                  following filtering parameters: `ids`, `portfolios`
            /events/details/{eventId}:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                description: >-
                  Fetch Signals event headlines plus all additional event
                  details for a single requested Signal event
            /events/adaptive-cards:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                description: >-
                  Fetch Microsoft's Adaptive Cards, which includes headlines and
                  event details data plus hyperlinks to FactSet reports, based
                  on at least one of the following filtering parameters: `ids`,
                  `portfolios`
              post:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                description: >-
                  Fetch Microsoft's Adaptive Cards, which includes headlines and
                  event details data plus hyperlinks to FactSet reports, based
                  on at least one of the following filtering parameters: `ids`,
                  `portfolios`
            /events/adaptive-cards/{eventId}:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                description: >-
                  Fetch Microsoft's Adaptive Cards, which includes headlines and
                  event details data plus hyperlinks to FactSet reports, for a
                  single requested Signal event
            /events/entities:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                  - Entities
                description: >-
                  Fetch FactSet entity IDs for events that match the filtering
                  criteria
              post:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                  - Entities
                description: >-
                  Fetch FactSet entity IDs for events that match the filtering
                  criteria
            /data-dictionary:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                  - Entities
                  - Data
                  - Dictionary
                description: Fetch a list of all active signals
            /data-dictionary/{signalId}:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                  - Entities
                  - Data
                  - Dictionary
                description: Fetch the metadata and contract for the requested signal
            /themes:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                  - Entities
                  - Data
                  - Dictionary
                  - Themes
                description: Fetch a list of available signal themes
            /categories:
              get:
                tags:
                  - Events
                  - Headlines
                  - Details
                  - Id
                  - Adaptive
                  - Cards
                  - Entities
                  - Data
                  - Dictionary
                  - Themes
                  - Categories
                description: Fetch a list of availab
    overlays:
      - type: APIs.io Search
        url: overlays/signals-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/signals-openapi-api-evangelist-ratings.yml
    aid: factset:factset-signals-api
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
  - name: FactSet Search Answers
    description: >-
      The FactSet Search Answers API provides answers to search queries,
      reflecting the data shown within FactSet Search Answers.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-search-answers
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-search-answers#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-search-answers#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-search-answers#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-search-answers#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-search-answers#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.2
          info:
            title: FactSet Search Answers API
          paths:
            /search/answers/v1/data:
              get:
                summary: Fetch FactSet answer in data format
                tags:
                  - Fetch
                  - Fact
                  - Set
                  - Answer
                  - In
                  - Data
                  - Format
                  - Search
                  - Answers
                  - V1
                  - Data
                description: >-
                  Returns an answer to the specified query (if a valid answer
                  exists). Returns the answer data only (as JSON), without any
                  markup information.
            /search/answers/v1/adaptive-card:
              get:
                summary: Fetch FactSet answer in Adaptive Card format
                tags:
                  - Fetch
                  - Fact
                  - Set
                  - Answer
                  - In
                  - Adaptive
                  - Card
                  - Format
                  - Search
                  - Answers
                  - V1
                  - Data
                  - Adaptive
                  - Card
                description: >-
                  Returns an answer to the specified query (if valid answer
                  exists) in the Adaptive Card format (https://a
    overlays:
      - type: APIs.io Search
        url: overlays/search-answers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/search-answers-openapi-api-evangelist-ratings.yml
    aid: factset:factset-search-answers
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---