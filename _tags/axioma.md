---
name: Axioma
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/axioma.png
url: https://example.com/apis/axioma.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Axioma
apis:
  - name: FactSet Axioma Equity Optimizer API
    description: >-
      The Axioma Equity API offers equity-based portfolio optimizations,
      balancing a client’s investment objectives within the confines of the
      established constraints within their investment strategy.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/axioma-equity-optimizer-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/axioma-equity-optimizer-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/axioma-equity-optimizer-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/axioma-equity-optimizer-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/axioma-equity-optimizer-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/axioma-equity-optimizer-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Axioma Equity API
            license:
              name: Apache License 2.0
              url: http://www.apache.org/licenses/LICENSE-2.0.txt
          paths:
            /analytics/lookups/v3/accounts/{path}:
              get:
                tags:
                  - Get
                  - Accounts
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                summary: Get accounts and sub-directories in a directory
                description: >-
                  This endpoint looks up all ACCT and ACTM files and
                  sub-directories in a given directory.
            /analytics/engines/axp/v3/optimizations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Axioma
                  - Optimization
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                summary: Create and Run Axioma optimization
                description: "This endpoint creates and runs Axioma optimization specified in the POST body parameters.\r\n            \r\nRemarks:\r\n            \r\n*\tAny settings in POST body will act as a one-time override over the settings saved in the strategy document."
            /analytics/engines/axp/v3/optimizations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Axioma
                  - Optimization
                  - And
                  - Run
                  - It.
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                summary: Create or Update Axioma optimization and run it.
                description: >-
                  This endpoint updates and run the Axioma optimization
                  specified in the PUT body parameters. It also allows the
                  creation of new Axioma optimization with custom id.
              get:
                tags:
                  - Get
                  - Axioma
                  - Optimization
                  - Parameters
                  - By
                  - Id
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                summary: Get Axioma optimization parameters by id
                description: >-
                  This is the endpoint that returns the optimization parameters
                  passed for a calculation.
              delete:
                tags:
                  - Cancel
                  - Axioma
                  - Optimization
                  - By
                  - Id
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                summary: Cancel Axioma optimization by id
                description: >-
                  This is the endpoint to cancel a previously submitted
                  optimization.
            /analytics/engines/axp/v3/optimizations/{id}/status:
              get:
                tags:
                  - Get
                  - Axioma
                  - Optimization
                  - Status
                  - By
                  - Id
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                  - Status
                summary: Get Axioma optimization status by id
                description: "This is the endpoint to check on the progress of a previously requested optimization.\r\nIf the optimization has finished computing, the body of the response will contain result in JSON.\r\nOtherwise, the optimization is still running and the X-FactSet-Api-PickUp-Progress header will contain a progress percentage."
            /analytics/engines/axp/v3/optimizations/{id}/result:
              get:
                tags:
                  - Get
                  - Axioma
                  - Optimization
                  - Result
                  - By
                  - Id
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                  - Status
                  - Result
                summary: Get Axioma optimization result by id
                description: >-
                  This is the endpoint to get the result of a previously
                  requested optimization.
            /analytics/lookups/v3/currencies:
              get:
                tags:
                  - Get
                  - Currencies
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                  - Status
                  - Result
                  - Currencies
                summary: Get currencies
                description: >-
                  This endpoint lists all the currencies that can be applied to
                  any calculation.
            /analytics/engines/axp/v3/strategies/{path}:
              get:
                tags:
                  - Get
                  - Axioma
                  - Equity
                  - Strategy
                  - Documents
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Path
                  - Engines
                  - Axp
                  - Optimizations
                  - Id
                  - Status
                  - Result
                  - Currencies
                  - Strategies
                summary: >-
                  Get Axioma Equity strategy documents and sub-directories in a
                  directory
                description: >-
                  This endpoint looks up all Axioma Equity strategy documents
                  and sub-directories i
    overlays:
      - type: APIs.io Search
        url: overlays/axioma-equity-optimizer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/axioma-equity-optimizer-openapi-api-evangelist-ratings.yml
    aid: factset:factset-axioma-equity-optimizer-api
  - name: FactSet Axioma Fixed Income Optimizer
    description: Fixed Income-based portfolio optimization
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/axioma-fixed-income-optimizer
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/axioma-fixed-income-optimizer#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/axioma-fixed-income-optimizer#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/axioma-fixed-income-optimizer#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/axioma-fixed-income-optimizer#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/axioma-fixed-income-optimizer#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: AFI Optimizer API
            license:
              name: Apache License 2.0
              url: http://www.apache.org/licenses/LICENSE-2.0.txt
          paths:
            /analytics/engines/afi/v3/optimizations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Optimization
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                summary: Create and Run AFI optimization
                description: "This endpoint creates and runs AFI optimization specified in the POST body parameters.\r\n            \r\nRemarks:\r\n            \r\n*\tAny settings in POST body will act as a one-time override over the settings saved in the strategy document."
            /analytics/engines/afi/v3/optimizations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Optimization
                  - And
                  - Run
                  - It.
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                  - Id
                summary: Create or Update AFI optimization and run it.
                description: >-
                  This endpoint updates and run the AFI optimization specified
                  in the PUT body parameters. It also allows the creation of new
                  AFI optimization with custom id.
              get:
                tags:
                  - Get
                  - Optimization
                  - Parameters
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                  - Id
                summary: Get AFI optimization parameters by id
                description: >-
                  This is the endpoint that returns the optimization parameters
                  passed for an optimization.
              delete:
                tags:
                  - Cancel
                  - Optimization
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                  - Id
                summary: Cancel AFI optimization by id
                description: >-
                  This is the endpoint to cancel a previously submitted
                  optimization.
            /analytics/engines/afi/v3/optimizations/{id}/status:
              get:
                tags:
                  - Get
                  - Optimization
                  - Status
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                  - Id
                  - Status
                summary: Get AFI optimization status by id
                description: "This is the endpoint to check on the progress of a previously requested optimization.\r\nIf the optimization has finished computing, the body of the response will contain result in JSON.\r\nOtherwise, the optimization is still running and the X-FactSet-Api-PickUp-Progress header will contain a progress percentage."
            /analytics/engines/afi/v3/optimizations/{id}/result:
              get:
                tags:
                  - Get
                  - Optimization
                  - Result
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                  - Id
                  - Status
                  - Result
                summary: Get AFI optimization result by id
                description: >-
                  This is the endpoint to get the result of a previously
                  requested optimization.
            /analytics/engines/afi/v3/strategies/{path}:
              get:
                tags:
                  - Get
                  - Axioma
                  - Strategy
                  - Documents
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Analytics
                  - Engines
                  - Afi
                  - V3
                  - Optimizations
                  - Id
                  - Status
                  - Result
                  - Strategies
                  - Path
                summary: >-
                  Get Axioma FI strategy documents and sub-directories in a
                  directory
                description: >-
                  This endpoint looks up all Axioma FI strategy documents and
                  sub-directories i
    overlays:
      - type: APIs.io Search
        url: overlays/axioma-fixed-income-optimizer-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/axioma-fixed-income-optimizer-openapi-api-evangelist-ratings.yml
    aid: factset:factset-axioma-fixed-income-optimizer
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---