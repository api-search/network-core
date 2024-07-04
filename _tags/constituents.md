---
name: Constituents
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/constituents.png
url: https://example.com/apis/constituents.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Constituents
apis:
  - name: FactSet Real-Time News API
    description: >-
      Retrieve news by category, identifier, and keyword, for a specific date or
      range of dates. Endpoints can be subscribed for streamed updates.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-news-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/real-time-news-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-news-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/real-time-news-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-news-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/real-time-news-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: News API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /news/article/get:
              get:
                tags:
                  - Details
                  - For
                  - News
                  - Article.
                  - News
                  - Article
                  - Get
                summary: Details for a news article.
                description: Details for a news article.
            /news/article/list:
              post:
                tags:
                  - List
                  - Of
                  - News
                  - Articles.
                  - News
                  - Article
                  - Get
                  - List
                summary: List of news articles.
                description: List of news articles.
            /news/article/listByChain:
              post:
                tags:
                  - List
                  - News
                  - Articles
                  - Of
                  - An
                  - Article
                  - Chain.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                summary: List news articles of an article chain.
                description: List news articles of an article chain.
            /news/article/listByIndex:
              post:
                tags:
                  - News
                  - Articles
                  - For
                  - Instruments
                  - That
                  - Are
                  - Constituents
                  - Of
                  - The
                  - Given
                  - Indices.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                summary: >-
                  News articles for instruments that are constituents of the
                  given indices.
                description: >-
                  News articles for instruments that are constituents of the
                  given indices.
            /news/article/listByInstrument:
              post:
                tags:
                  - News
                  - Articles
                  - For
                  - Instruments.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                summary: News articles for instruments.
                description: News articles for instruments.
            /news/article/listByMediaKind:
              post:
                tags:
                  - List
                  - News
                  - Articles
                  - Which
                  - Contain
                  - Media
                  - Of
                  - Specific
                  - Kinds.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                summary: >-
                  List news articles which contain media of specific media
                  kinds.
                description: >-
                  List news articles which contain media of specific media
                  kinds.
            /news/article/searchByText:
              post:
                tags:
                  - Search
                  - For
                  - News
                  - Articles
                  - Using
                  - Fulltext
                  - Search.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                summary: Search for news articles using a fulltext search.
                description: >-
                  Search for news articles using a fulltext search. All
                  specified criteria need to be fulfilled for an article to
                  match. Each criterion is handled according to its
                  selectionType; "include" requires the criterion to evaluate to
                  true, "exclude" requires the criterion to evaluate to false. A
                  criterion is fulfilled when at least one of its values is
                  found.
            /news/article/type/get:
              get:
                tags:
                  - Details
                  - For
                  - News
                  - Article
                  - Type.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                summary: Details for a news article type.
                description: Details for a news article type.
            /news/article/type/list:
              get:
                tags:
                  - List
                  - Of
                  - News
                  - Article
                  - Types.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                summary: List of news article types.
                description: List of news article types.
            /news/distributor/get:
              get:
                tags:
                  - Details
                  - Of
                  - Distributor.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                  - Distributor
                summary: Details of a distributor.
                description: Details of a distributor.
            /news/distributor/list:
              get:
                tags:
                  - List
                  - Of
                  - Distributors.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                  - Distributor
                summary: List of distributors.
                description: List of distributors.
            /news/publisher/get:
              get:
                tags:
                  - Details
                  - Of
                  - Publisher.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                  - Distributor
                  - Publisher
                summary: Details of a publisher.
                description: Details of a publisher.
            /news/publisher/list:
              get:
                tags:
                  - List
                  - Of
                  - Publishers.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                  - Distributor
                  - Publisher
                summary: List of publishers.
                description: List of publishers.
            /news/publisher/listByDistributor:
              get:
                tags:
                  - List
                  - Of
                  - Publishers
                  - Provided
                  - By
                  - The
                  - Given
                  - Distributor.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                  - Distributor
                  - Publisher
                summary: List of publishers provided by the given distributor.
                description: List of publishers provided by the given distributor.
            /news/publisher/searchByName:
              post:
                tags:
                  - Search
                  - For
                  - Publishers.
                  - News
                  - Article
                  - Get
                  - List
                  - By
                  - Chain
                  - Index
                  - Instrument
                  - Media
                  - Kind
                  - Text
                  - Type
                  - Distributor
                  - Publisher
                  - Name
                summary: Search for publishers.
                description: Search for publishers by the name of the publisher.
          tags:
            - name: news
              description: news endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-news-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-news-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-news-api
  - name: FactSet Benchmarks API
    description: >-
      Returns Benchmark Constituent data including weights, price, and market
      value for a specified date.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-benchmarks-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-benchmarks-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Benchmarks API
          paths:
            /factset-benchmarks/v1/constituents:
              get:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value. You must be authorized for
                  the `ids` requested. Use the helper endpoint **/id-list** for
                  valid identifiers.  
              post:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value. You must be authorized for
                  the `ids` requested. Use the helper endpoint **/id-list** for
                  valid identifiers.
            /factset-benchmarks/v1/fixed-income-constituents:
              get:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Fixed
                  - Income
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                summary: >-
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value.
                description: >
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value. You must be
                  authorized for the `ids` requested.
              post:
                tags:
                  - Returns
                  - The
                  - Requested
                  - Benchmark
                  - Constituents
                  - And
                  - Respective
                  - Weights,
                  - Price
                  - Market
                  - Value.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                summary: >-
                  Returns the requested Benchmark Constituents and respective
                  Weights, Price and Market Value.
                description: >
                  Returns the requested Fixed Income Benchmark Constituents and
                  respective Weights, Price and Market Value. You must be
                  authorized for the `ids` requested.
            /factset-benchmarks/v1/index-snapshot:
              get:
                summary: >-
                  Index Level Prices, Returns, and related information as of a
                  single date.
                tags:
                  - Index
                  - Level
                  - Prices,
                  - Returns,
                  - And
                  - Related
                  - Information
                  - As
                  - Of
                  - Single
                  - Date.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                description: >
                  Retrieves Index Level Prices and Returns information as of a
                  specific date. Simply submit a valid Benchmark ID (you can use
                  the /id-list endpoint for a sample list of ids), and date and
                  retrieve Index Level Prices, Returns, and related information.
              post:
                summary: >-
                  Retrieves the Index Level Snapshot of Prices and Returns
                  information for a given identifier and single date.
                tags:
                  - Retrieves
                  - The
                  - Index
                  - Level
                  - Snapshot
                  - Of
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - Given
                  - Identifier
                  - Single
                  - Date.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                description: >
                  Retrieves Index Level Prices and Returns information as
                  aligned with FactSet's Benchmark Data Feed solution. Simply
                  submit a valid Benchmark ID (you can use the /id-list endpoint
                  for a sample list of ids), and date and retrieve Index Level
                  Prices, Returns, and related information.
            /factset-benchmarks/v1/index-history:
              get:
                summary: >-
                  Retrieves Index Level Prices and Returns information for a
                  list of identifiers and historical date range.
                tags:
                  - Retrieves
                  - Index
                  - Level
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Historical
                  - Date
                  - Range.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                description: >
                  Retrieves Index Level Prices and Returns information as of a
                  date range requested. Simply submit a valid Benchmark ID (you
                  can use the /id-list endpoint for a sample list of ids), and
                  date range to retrieve Index Level Prices, Returns, and
                  related information.
              post:
                summary: >-
                  Retrieves Index Level Prices and Returns information for a
                  list of identifiers and historical date range.
                tags:
                  - Retrieves
                  - Index
                  - Level
                  - Prices
                  - And
                  - Returns
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Historical
                  - Date
                  - Range.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                description: >
                  Retrieves Index Level Prices and Returns information as
                  aligned with FactSet's Benchmark Data Feed solution. Simply
                  submit a valid Benchmark ID (you can use the /id-list endpoint
                  for a sample list of ids), and date and retrieve Index Level
                  Prices, Returns, and related information.
            /factset-benchmarks/v1/ratios:
              get:
                tags:
                  - Returns
                  - The
                  - Aggregated
                  - Ratios
                  - Of
                  - Requested
                  - Benchmark
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                summary: Returns the aggregated ratios of a requested benchmark
                description: >
                  Retrieves the index level ratios for a requested benchmark.
                  Ratios supported are expressed through metrics parameter, and
                  include Categories of Profitability, Valuation, Coverage, and
                  Leverage. <p> Using FactSet Market Aggregates, the service
                  combines fundamental, estimates, and pricing content to derive
                  ratios and per share values for global equity market indexes
                  and commercial benchmark vendors. The constituents of the
                  index are fetched on rolling basis over time period requested,
                  and then the metric requested is aggregated up to the index
                  level. To learn more about FMA, visit [OA
                  15778](https://my.apps.factset.com/oa/pages/15778).</p>
              post:
                tags:
                  - Returns
                  - The
                  - Aggregated
                  - Ratios
                  - Of
                  - Requested
                  - Benchmark
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                summary: Returns the aggregated ratios of a requested benchmark
                description: >
                  Retrieves the index level ratios for a requested benchmark.
                  Ratios supported are expressed through metrics parameter, and
                  include Categories of Profitability, Valuation, Coverage, and
                  Leverage. <p> Using FactSet Market Aggregates, the service
                  combines FactSet Fundamental, FactSet Estimates, and FactSet
                  Pricing content to derive ratios and per share values for
                  global equity market indexes and commercial benchmark vendors.
                  The constituents of the index are fetched on rolling basis
                  over time period requested, and then the metric requested is
                  aggregated up to the index level. To learn more about FMA,
                  visit [OA
                  15778](https://my.apps.factset.com/oa/pages/15778).</p>
            /factset-benchmarks/v1/id-list:
              get:
                summary: >-
                  Returns a sample list of Benchmark Identifiers and the
                  benchmark categorization to use in other Benchmark API
                  endpoints.
                tags:
                  - Returns
                  - Sample
                  - List
                  - Of
                  - Benchmark
                  - Identifiers
                  - And
                  - The
                  - Categorization
                  - To
                  - Use
                  - In
                  - Other
                  - Endpoints.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                  - Id
                  - List
                description: >-
                  Returns a **sample** list of Benchmark Identifiers to use in
                  other Benchmark API endpoints. This is a supporting API to be
                  use alongside the other Benchmark API endpoints. For example,
                  use the fsymID value returned in this response as the input to
                  your `ids` parameter in the /constituents endpoint to return
                  constituents for that id.<p> *This is not the full list of
                  benchmark ids allowed in this service, but rather a
                  representation of the most commonly requested. For complete
                  assistance with ID lookup or concordance services, please
                  reach out to FactSet Support. *</p>
              post:
                summary: >-
                  Returns a sample list of Benchmark Identifiers and the
                  benchmark categorization to use in other Benchmark API
                  endpoints.
                tags:
                  - Returns
                  - Sample
                  - List
                  - Of
                  - Benchmark
                  - Identifiers
                  - And
                  - The
                  - Categorization
                  - To
                  - Use
                  - In
                  - Other
                  - Endpoints.
                  - Factset
                  - Benchmarks
                  - V1
                  - Constituents
                  - Fixed
                  - Income
                  - Index
                  - Snapshot
                  - History
                  - Ratios
                  - Id
                  - List
                description: >-
                  Returns a **sample** list of Benchmark Identifiers to use in
                  other Benchmark API endpoints. This is a supporting API to be
                  use alongside the other Benchmark API endpoints. For example,
                  use the fsymID value returned in this response as the input to
                  your `ids` parameter in the /constituents endpoint to return
                  constituents for that id.<p> *This is not the full list of
                  benchmark ids allowed in this service, but rather a
                  representation of the most commonly requested. For complete
                  assistance with ID lookup or concordance services, please
                  reach out to F
    overlays:
      - type: APIs.io Search
        url: overlays/benchmarks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/benchmarks-openapi-api-evangelist-ratings.yml
    aid: factset:factset-benchmarks-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---