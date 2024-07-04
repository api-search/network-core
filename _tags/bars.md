---
name: Bars
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bars.png
url: https://example.com/apis/bars.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bars
apis:
  - name: FactSet Tick History API
    description: >-
      Tick History provides dynamic access to historical tick data for a
      specific security for specific dates or date range.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-tick-history-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-tick-history-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Tick History
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/factset-tick-history-api
          paths:
            /level1/coverage:
              get:
                tags:
                  - Returns
                  - The
                  - Coverage
                  - For
                  - Requested
                  - Ticker/isin
                  - Along
                  - With
                  - Other
                  - Response
                  - Fields
                  - Level1
                  - Data.
                  - Level1
                  - Coverage
                summary: >-
                  Returns the coverage for the requested ticker/isin along with
                  other response fields for Level1 data.
                description: Returns coverage for specified tickers for Level1 Data
            /level1/files/create:
              post:
                tags:
                  - Requests
                  - The
                  - Creation
                  - Of
                  - Tick-by-tick
                  - File
                  - Level1
                  - Coverage
                  - Files
                  - Create
                summary: Requests the creation of tick-by-tick file
                description: Data available from 20120101 to previous day.
            /level1/files/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - Of
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                summary: Returns the status of the ID
                description: >-
                  Need to plug-in the id get from /create endpoint into /status
                  endpoint
            /level1/files/get:
              get:
                tags:
                  - Returns
                  - The
                  - Tick-by-tick
                  - Data
                  - In
                  - Files
                  - Requested
                  - /create
                  - Endpoint
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                summary: >-
                  Returns the tick-by-tick data in files requested in the
                  /create endpoint
                description: Returns the files from tickhistory endpoint
            /level1/files/minute-bars/create:
              post:
                tags:
                  - Requests
                  - The
                  - Creation
                  - Of
                  - Minute
                  - Bars
                  - File
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                summary: Requests the creation of Minute bars file
                description: >-
                  1-minute bars available from 20120101 to previous day. Per
                  request able to fetch upto 6 months of data.
            /level1/files/minute-bars/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - Of
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                summary: Returns the status of the ID
                description: >-
                  Need to plug-in the id get from /create endpoint into /status
                  endpoint
            /level1/files/minute-bars/get:
              get:
                tags:
                  - Returns
                  - The
                  - Minute
                  - Bars
                  - Data
                  - In
                  - Files
                  - Requested
                  - /create
                  - Endpoint
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                summary: >-
                  Returns the Minute bars data in files requested in the /create
                  endpoint
                description: Returns the files from tickhistory endpoint
            /level2/files/create:
              post:
                tags:
                  - Returns
                  - The
                  - For
                  - Requested
                  - Data.
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                  - Level2
                summary: Returns the ID for the requested data.
                description: Data available from past 6 years to previous day.
            /level2/files/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - Of
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                  - Level2
                summary: Returns the status of the ID
                description: >-
                  Need to plug-in the id get from /create endpoint into /status
                  endpoint
            /level2/files/get:
              get:
                tags:
                  - Returns
                  - The
                  - Tick
                  - History
                  - Files
                  - Requested
                  - In
                  - /create
                  - Endpoint
                  - Level1
                  - Coverage
                  - Files
                  - Create
                  - Status
                  - Get
                  - Minute
                  - Bars
                  - Level2
                summary: >-
                  Returns the tick history files requested in the /create
                  endpoint
                description: Returns the files from tickhistory endpoint
          tags:
            - name: Level 1
              description: >-
                API provides access to check coverage and retrieve Level 1
                historical tick data
            - name: Level 2
              description: API provides access to the  historical tick data up
    overlays:
      - type: APIs.io Search
        url: overlays/tick-history-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/tick-history-openapi-api-evangelist-ratings.yml
    aid: factset:factset-tick-history-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---