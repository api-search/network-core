---
name: All Estimates
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/all-estimates.png
url: https://example.com/apis/all-estimates.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - All Estimates
apis:
  - name: FactSet Estimates Report Builder API
    description: >-
      The FactSet Estimates Report Builder APIs return consensus estimate data
      with fiscal periods and line items structured in a presentation-ready
      format.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/factset-estimates-report-builder-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: FactSet Estimates Report Builder
            description: ''
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: Read more about STACH 2.0's row organized schema
            url: https://factset.github.io/stachschema/#/v2/RowOrganized
          tags:
            - name: All Estimates
            - name: Estimate Tables
          paths:
            /income-statement:
              get:
                tags:
                  - Income
                  - Statement
                  - Income
                  - Statement
                summary: Income Statement
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Income Statement line items.
            /balance-sheet:
              get:
                tags:
                  - Balance
                  - Sheet
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                summary: Balance Sheet
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Balance Sheet line items.
            /cash-flow:
              get:
                tags:
                  - Cash
                  - Flow
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                summary: Cash Flow
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Cash Flow line items.
            /per-share:
              get:
                tags:
                  - Per
                  - Share
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                summary: Per Share
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Per Share line items.
            /industry-metrics:
              get:
                tags:
                  - Industry
                  - Metrics
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                summary: Industry Metrics
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for industry-specific metrics.
            /product-segments:
              get:
                tags:
                  - Product
                  - Segments
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                summary: Product Segments
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for line items broken down by product
                  and business.
            /geographic-segments:
              get:
                tags:
                  - Geographic
                  - Segments
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                  - Geographic
                summary: Geographic Segments
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for line items broken down
                  geographically.
            /valuation:
              get:
                tags:
                  - Valuation
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                  - Geographic
                  - Valuation
                summary: Valuation
                description: >-
                  Returns valuation ratios in a statement format calculated from
                  historical and future period broker estimate consensus.
            /table:
              get:
                tags:
                  - Interim/
                  - Annual
                  - Estimate
                  - Table
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                  - Geographic
                  - Valuation
                  - Table
                summary: Interim/Annual Estimate Table
                description: Returns a timeseries grid of Interim and Annual data
    overlays:
      - type: APIs.io Search
        url: overlays/estimates-report-builder-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/estimates-report-builder-openapi-api-evangelist-ratings.yml
    aid: factset:factset-estimates-report-builder-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---