---
name: Benchmark
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/benchmark.png
url: https://example.com/apis/benchmark.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Benchmark
apis:
  - name: FactSet SPAR Engine API
    description: >-
      Through the SPAR API (Style, Performance, and Risk) monitor your
      portfolios’ returns against equity and fixed income benchmarks, and peer
      universes, with MPT risk statistics such as beta, standard deviation,
      r-squared, alpha, and tracking error…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/spar-engine-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/spar-engine-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/spar-engine-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/spar-engine-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/spar-engine-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/spar-engine-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: SPAR Engine API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /analytics/engines/spar/v3/accounts/{accountPath}/returns-type:
              get:
                tags:
                  - Get
                  - Account
                  - Returns
                  - Type
                  - Details
                  - Path
                  - Returns
                  - Type
                summary: Get SPAR account returns type details
                description: >-
                  This endpoint returns the returns type of account associated
                  with SPAR
            /analytics/lookups/v3/accounts/{path}:
              get:
                tags:
                  - Get
                  - Accounts
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                summary: Get accounts and sub-directories in a directory
                description: >-
                  This endpoint looks up all ACCT and ACTM files and
                  sub-directories in a given directory.
            /analytics/engines/spar/v3/benchmarks:
              get:
                tags:
                  - Get
                  - Benchmark
                  - Details
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                summary: Get SPAR benchmark details
                description: >-
                  This endpoint returns the details of a given SPAR benchmark
                  identifier.
            /analytics/engines/spar/v3/components:
              get:
                tags:
                  - Get
                  - Components
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                summary: Get SPAR components
                description: >-
                  This endpoint returns the list of SPAR components in a given
                  SPAR document.
            /analytics/engines/spar/v3/components/{id}:
              get:
                tags:
                  - Get
                  - Component
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                summary: Get SPAR component by id
                description: >-
                  This endpoint returns the default settings of a SPAR
                  component.
            /analytics/lookups/v3/currencies:
              get:
                tags:
                  - Get
                  - Currencies
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                summary: Get currencies
                description: >-
                  This endpoint lists all the currencies that can be applied to
                  any calculation.
            /analytics/engines/spar/v3/documents/{path}:
              get:
                tags:
                  - Gets
                  - R3
                  - Documents
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                summary: Gets SPAR3 documents and sub-directories in a directory
                description: >-
                  This endpoint looks up all SPAR3 documents and sub-directories
                  in a given directory.
            /analytics/engines/spar/v3/frequencies:
              get:
                tags:
                  - Get
                  - Frequencies
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                summary: Get SPAR frequencies
                description: >-
                  This endpoint lists all the frequencies that can be applied to
                  a SPAR calculation.
            /analytics/engines/spar/v3/calculations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Calculation
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Create and Run SPAR calculation
                description: "This endpoint runs the SPAR calculation specified in the POST body parameters.\r\nIt can take one or more units as input.\r\n\r\nRemarks:\r\n\r\n*\tAny settings in POST body will act as a one-time override over the settings saved in the SPAR template."
              get:
                tags:
                  - Get
                  - All
                  - Calculations
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Get all calculations
                description: This endpoints returns all calculation requests.
            /analytics/engines/spar/v3/calculations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Calculation
                  - And
                  - Run
                  - It.
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Create or Update SPAR calculation and run it.
                description: "This endpoint updates and run the SPAR calculation specified in the PUT body parameters. This also allows creating new SPAR calculations with custom ids.\r\nIt can take one or more units as input.\r\n\r\nRemarks:\r\n\r\n*\tAny settings in PUT body will act as a one-time override over the settings saved in the SPAR template."
              get:
                tags:
                  - Get
                  - Calculation
                  - Parameters
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Get SPAR calculation parameters by id
                description: >-
                  This is the endpoint that returns the calculation parameters
                  passed for a calculation.
              delete:
                tags:
                  - Cancel
                  - Calculation
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Cancel SPAR calculation
                description: >-
                  This is the endpoint to cancel a previously submitted
                  calculation.
            /analytics/engines/spar/v3/calculations/{id}/status:
              get:
                tags:
                  - Get
                  - Calculation
                  - Status
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                  - Status
                summary: Get SPAR calculation status by id
                description: "This is the endpoint to check on the progress of a previously requested calculation.\r\nIf the calculation has finished computing, the location header will point to the result url."
            /analytics/engines/spar/v3/calculations/{id}/units/{unitId}/result:
              get:
                tags:
                  - Get
                  - Calculation
                  - Result
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                  - Status
                  - Result
                summary: Get SPAR calculation result by id
                description: "This is the endpoint to get the result of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON."
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catal
    overlays:
      - type: APIs.io Search
        url: overlays/spar-engine-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/spar-engine-openapi-api-evangelist-ratings.yml
    aid: factset:factset-spar-engine-api
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
  - name: FactSet Funds API
    description: Reference and Time Series Mutual Fund Data
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-funds-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-funds-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/factset-funds-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-funds-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-funds-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-funds-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Funds API
          tags:
            - name: Reference
              description: >-
                Basic reference data for funds, including summary, status,
                benchmark details, classifications, and more.
            - name: Prices & Returns
              description: Fetch Fund Price (NAV) and Returns over a requested time-series.
            - name: Fund Flows & AUM
              description: Fetch Fund AUM and Fund Flows over a requested time-series.
            - name: Helper
              description: Check the Fund's current status and database availability
          paths:
            /factset-funds/v1/summary:
              get:
                tags:
                  - Get
                  - Basic
                  - Reference
                  - Summary
                  - Data
                  - For
                  - Fund.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                summary: Get basic reference summary data for a Fund.
                description: >
                  Fetch basic reference data for the requested fund(s),
                  including countryDomicile, shrClass, shrClassInceptDate, etc. 
              post:
                tags:
                  - Get
                  - Basic
                  - Reference
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fund
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                summary: Get basic reference data for a large list of Fund ids.
                description: >
                  Fetch basic reference data for the requested fund(s),
                  including countryDomicile, shrClass, shrClassInceptDate, etc. 
            /factset-funds/v1/classifications:
              get:
                tags:
                  - Get
                  - Basic
                  - Fund
                  - Classifications
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                summary: Get basic Fund Classifications
                description: >
                  Fetch basic fund classification data, such as Asset Class,
                  Category, Focus, Niche, Region, and more.<p> FactSet Mutual
                  Funds Reference uses FactSet's proprietary Fund Classification
                  System, which categorizes funds using a rules-based system
                  that is derived from seven core classifications. This system
                  evaluates the asset class, economic development level, and
                  geographical region as described in each fund's prospectus and
                  marketing materials. Fund exposure details are presented on
                  successively granular levels- category, then focus, and then
                  niche. Moreover, FactSet Fund Reference captures over 40
                  unique data points for U.S. mutual funds. All data items are
                  grouped in one of two levels, either as a Fund or as a Share
                  Class.</p><p>For more details regarding FactSet's Fund
                  Classification, visit Online Assistant
                  [21436](https://my.apps.factset.com/oa/pages/21436) or
                  download - [FactSet Fund Classification System Rules &
                  Methodology](https://my.apps.factset.com/oa/cms/oaAttachment/4547a2f4-5df5-4ec9-a0d3-7d51610dd637/26837)</p><p>

                  |Classification Type|Description|

                  |||

                  |Asset Class|The asset class of the fund (e.g. Equity, Fixed
                  Income, Currency, Commodities, Asset Allocation, or
                  Alternatives) based on the fund's mandate.|

                  |Category|The 1st of 3 asset-class-specific, hierarchical
                  exposure tiers; the broadest category the fund falls under
                  within its asset class (e.g., Size & Style, Sector, Precious
                  Metals, Absolute Returns); based on the fund's mandate.|

                  |Focus|The 2nd of 3 asset-class-specific, hierarchical
                  exposure tiers; the fund's classification within its category
                  (e.g. Small Cap, Energy, Palladium, Long/Short); based on the
                  fund's mandate.|

                  |Niche|The 3rd of 3 asset-class-specific, hierarchical
                  exposure tiers; The fund's classification within its Focus.
                  Most granular tier of exposure sort (e.g., Growth, Coal,
                  Physically held, Merger Arbitrage); based on the fund's
                  mandate.|

                  |Economic Development Level|The country development level of
                  the fund (Developed, Emerging, Frontier, or Blended) based on
                  the fund's mandate.|

                  |Region|The broad regional exposure of the fund (e.g., Latin
                  America, Asia-Pacific, Global) based on the fund's mandate.|

                  |Specific Geography|The specific geographic exposure of the
                  fund (e.g., Developed Europe, Chile, Asia-Pacific Ex-Japan)
                  based on the fund's mandate.|

                  </p>
              post:
                tags:
                  - Get
                  - Basic
                  - Fund
                  - Classifications
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                summary: Get basic Fund Classifications for a large list of ids.
                description: >
                  Fetch basic fund classification data, such as Asset Class,
                  Category, Focus, Niche, Region, and more.<p> FactSet Mutual
                  Funds Reference uses FactSet's proprietary Fund Classification
                  System, which categorizes funds using a rules-based system
                  that is derived from seven core classifications. This system
                  evaluates the asset class, economic development level, and
                  geographical region as described in each fund's prospectus and
                  marketing materials. Fund exposure details are presented on
                  successively granular levels- category, then focus, and then
                  niche. Moreover, FactSet Fund Reference captures over 40
                  unique data points for U.S. mutual funds. All data items are
                  grouped in one of two levels, either as a Fund or as a Share
                  Class.</p><p>For more details regarding FactSet's Fund
                  Classification, visit Online Assistant
                  [21436](https://my.apps.factset.com/oa/pages/21436) or
                  download - [FactSet Fund Classification System Rules &
                  Methodology](https://my.apps.factset.com/oa/cms/oaAttachment/4547a2f4-5df5-4ec9-a0d3-7d51610dd637/26837)</p><p>

                  |Classification Type|Description|

                  |||

                  |Asset Class|The asset class of the fund (e.g. Equity, Fixed
                  Income, Currency, Commodities, Asset Allocation, or
                  Alternatives) based on the fund's mandate.|

                  |Category|The 1st of 3 asset-class-specific, hierarchical
                  exposure tiers; the broadest category the fund falls under
                  within its asset class (e.g., Size & Style, Sector, Precious
                  Metals, Absolute Returns); based on the fund's mandate.|

                  |Focus|The 2nd of 3 asset-class-specific, hierarchical
                  exposure tiers; the fund's classification within its category
                  (e.g. Small Cap, Energy, Palladium, Long/Short); based on the
                  fund's mandate.|

                  |Niche|The 3rd of 3 asset-class-specific, hierarchical
                  exposure tiers; The fund's classification within its Focus.
                  Most granular tier of exposure sort (e.g., Growth, Coal,
                  Physically held, Merger Arbitrage); based on the fund's
                  mandate.|

                  |Economic Development Level|The country development level of
                  the fund (Developed, Emerging, Frontier, or Blended) based on
                  the fund's mandate.|

                  |Region|The broad regional exposure of the fund (e.g., Latin
                  America, Asia-Pacific, Global) based on the fund's mandate.|

                  |Specific Geography|The specific geographic exposure of the
                  fund (e.g., Developed Europe, Chile, Asia-Pacific Ex-Japan)
                  based on the fund's mandate.|

                  </p>
            /factset-funds/v1/benchmark-details:
              get:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Primary
                  - And
                  - Segment
                  - Benchmark
                  - Details
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                summary: Get the Fund's Primary and Segment Benchmark Details
                description: >
                  Fetch the Fund's Benchmark and Segment Benchmark ids. These
                  ids can be then used in the [Benchmarks
                  API](https://developer.factset.com/api-catalog/factset-benchmarks-api)
                  to fetch index-level prices, returns, constituents data.
              post:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Primary
                  - And
                  - Segment
                  - Benchmark
                  - Details
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                summary: >-
                  Get the Fund's Primary and Segment Benchmark details for large
                  list of ids.
                description: >
                  Fetch the Fund's Benchmark and Segement Benchmark ids. These
                  ids can be then used in the [Benchmarks
                  API](https://developer.factset.com/api-catalog/factset-benchmarks-api)
                  to fetch index-level prices, returns, constituents data.
            /factset-funds/v1/costs-fees:
              get:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Costs,
                  - Investment
                  - Minimums
                  - And
                  - Risk,
                  - Fees.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                summary: Get the Fund's Costs, Investment minimums and Risk, and Fees.
                description: >
                  Fetch the Fund's Costs, Investment minimums and Risk, and
                  Fees. This subcategory includes management fees, 12b-1 fees,
                  expense ratios, and several other data items. The value for
                  each specified share class is expressed as a percentage of the
                  AUM.
              post:
                tags:
                  - Get
                  - The
                  - Fund's
                  - Costs,
                  - Investment
                  - Minimums
                  - And
                  - Risk,
                  - Fees
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                summary: >-
                  Get the Fund's Costs, Investment minimums and Risk, and Fees
                  for large list of ids.
                description: >
                  Fetch the Fund's Costs, Investment minimums and Risk, and
                  Fees. Data Items include Expense Ratios, investment minimums
                  and maximums, swing prices, entry and exit expenses, and more.
            /factset-funds/v1/managers:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Fund
                  - Managers
                  - And
                  - Related
                  - Details
                  - For
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                summary: >-
                  Get a list of Fund Managers and related details for a list of
                  ids.
                description: >
                  Fetch basic Fund manager details, such as Title, Phone, Job Id
                  and Name. NOTE - A subscription to FactSet's Ownership product
                  is required to access formulas in this Asset Managers
                  subcategory.
              post:
                tags:
                  - Get
                  - List
                  - Of
                  - Fund
                  - Managers
                  - And
                  - Related
                  - Details
                  - For
                  - Large
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                summary: >-
                  Get a list of Fund Managers and related details for a large
                  list of ids.
                description: >
                  Fetch basic Fund manager details, such as Title, Phone, Job Id
                  and Name. 
            /factset-funds/v1/related-funds:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Related
                  - Funds
                  - For
                  - Fund
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                summary: Get a list of Related Funds for a list of Fund ids.
                description: >
                  Fetch the five related fund share classes. Fund share classes
                  can be related if they belong to the same Fund Classification
                  segment, have the same share class type, have the same legal
                  structure, and have the same country of primary exchange.
                  Beyond the baseline criteria, the five most relevant funds are
                  determined based on whether they follow the same benchmark,
                  have the same maturity, and have the same selection strategy
                  as the specified share class.
              post:
                tags:
                  - Get
                  - List
                  - Of
                  - Related
                  - Funds
                  - For
                  - Large
                  - Fund
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                summary: Get a list of Related Funds for a large list of Fund ids.
                description: >
                  Fetch the five related fund share classes. Fund share classes
                  can be related if they belong to the same Fund Classification
                  segment, have the same share class type, have the same legal
                  structure, and have the same country of primary exchange.
                  Beyond the baseline criteria, the five most relevant funds are
                  determined based on whether they follow the same benchmark,
                  have the same maturity, and have the same selection strategy
                  as the specified share class.
            /factset-funds/v1/prices:
              get:
                tags:
                  - Get
                  - Fund
                  - Prices
                  - V)
                  - For
                  - Requested
                  - Time-series
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                summary: Get Fund Prices (NAV) for a requested time-series
                description: >
                  Get Fund Prices (NAV) for a requested date range and list of
                  ids.
              post:
                tags:
                  - Get
                  - Fund
                  - Prices
                  - V)
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                summary: >-
                  Get Fund Prices (NAV) for a requested date range and large
                  list of ids.
                description: >
                  Fetch fund prices (NAV) as of a requested date range and a
                  large list of ids. 
            /factset-funds/v1/returns:
              get:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - For
                  - Requested
                  - Time-series
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                summary: Get Fund Returns for a requested time-series
                description: >
                  Get Fund NAV Returns over a time-series for the requested date
                  range and frequency. <p>The simple Total Return NAV shows the
                  fund's total return level by reinvesting distributions so that
                  ex-date NAVs are increased by the distribution amount and
                  compounded thereafter. Total return NAV compounds daily and is
                  calculated from the first available NAV date of each fund. The
                  total return NAV series reflects the value that an investor
                  would own if it had purchased one share at the inception date
                  and reinvested all dividends on a Gross basis.</p><p> Control
                  the dividends to include or exclude using the dividendAdjust
                  parameter. The first available NAV date of each fund can be
                  found in the /summary endpoint as `priceFristDate`. Visit [OA
                  #21437](https://my.apps.factset.com/oa/pages/21437) for more
                  details.</p>
              post:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - For
                  - Requested
                  - Time-series
                  - And
                  - Large
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                summary: >-
                  Get Fund Returns for a requested time-series and large list of
                  ids
                description: >
                  Get Fund NAV Returns over a time-series for the requested date
                  range and frequency. <p>The simple Total Return NAV shows the
                  fund's total return level by reinvesting distributions so that
                  ex-date NAVs are increased by the distribution amount and
                  compounded thereafter. Total return NAV compounds daily and is
                  calculated from the first available NAV date of each fund. The
                  total return NAV series reflects the value that an investor
                  would own if it had purchased one share at the inception date
                  and reinvested all dividends on a Gross basis.</p><p> Control
                  the dividends to include or exclude using the dividendAdjust
                  parameter. The first available NAV date of each fund can be
                  found in the /summary endpoint as `priceFristDate`. Visit [OA
                  #21437](https://my.apps.factset.com/oa/pages/21437) for more
                  details.</p>
            /factset-funds/v1/returns-snapshot:
              get:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - Over
                  - Pre-defined
                  - Time
                  - Horizons
                  - As
                  - Of
                  - Specific
                  - Date.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                summary: >-
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date.
                description: >
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date. Use the date parameter to set the perspective
                  date, and adjust the return type to include or exclude
                  dividends using the dividendAdjust parameter. Returns Ranges
                  include - 

                  * oneWeek

                  * oneMonth

                  * threeMonth

                  * yearToDate

                  * oneYear

                  * threeYear

                  * threeYearAnnualized

                  * fiveYear

                  * fiveYearAnnualized
              post:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - Over
                  - Pre-defined
                  - Time
                  - Horizons
                  - As
                  - Of
                  - Specific
                  - Date.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                summary: >-
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date.
                description: >
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date. Use the date parameter to set the perspective
                  date, and adjust the return type to include or exclude
                  dividends using the dividendAdjust parameter. Returns Ranges
                  include - 

                  * oneWeek

                  * oneMonth

                  * threeMonth

                  * yearToDate

                  * oneYear

                  * threeYear

                  * threeYearAnnualized

                  * fiveYear

                  * fiveYearAnnualized 
            /factset-funds/v1/returns-range:
              get:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - For
                  - User-defined
                  - Date
                  - Range
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                summary: Get Fund Returns for a user-defined date range
                description: >
                  Get Fund Returns between a specified startDate and endDate.
                  The service will compute the return between those two periods
                  to retrieve the single value and does not create a
                  time-series. Control the return type to include or exclude
                  dividends by using the dividendAdjust parameter.
              post:
                tags:
                  - Get
                  - Fund
                  - Returns
                  - Over
                  - Pre-defined
                  - Time
                  - Horizons
                  - As
                  - Of
                  - Specific
                  - Date
                  - For
                  - Large
                  - List
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                summary: >-
                  Get Fund Returns over pre-defined time horizons as of a
                  specific date for large list of ids.
                description: >
                  Get Fund Returns between a specified startDate and endDate.
                  The service will compute the return between those two periods
                  to retrieve the single value and does not create a
                  time-series. Control the return type to include or exclude
                  dividends by using the dividendAdjust parameter.
            /factset-funds/v1/aum:
              get:
                tags:
                  - Get
                  - Fund
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                summary: Get Fund AUM for a requested date range and list of ids
                description: >
                  Get the Fund Level or Share Class Level Assets Under
                  Management (AUM). <p>NOTE - AUM can be accessed on a five-day
                  calendar. If a vendor does not provide NAV and shares
                  outstanding on a market holiday, the previous trading day
                  value is used. If a vendor does provide data on a market
                  holiday, that value will be presented, and then fund flows and
                  AUM will be calculated. When you are manually calculating
                  actual AUM on a market holiday or a rolled date, it will
                  differ from the value shown in the FactSet workstation. This
                  is due to the previous day's NAV being used in the manual AUM
                  calculation.</p>
              post:
                tags:
                  - Get
                  - Fund
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - Large
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                summary: Get Fund AUM for a requested date range and large list of ids
                description: >
                  Get the Fund Level or Share Class Level Assets Under
                  Management (AUM). <p>NOTE - AUM can be accessed on a five-day
                  calendar. If a vendor does not provide NAV and shares
                  outstanding on a market holiday, the previous trading day
                  value is used. If a vendor does provide data on a market
                  holiday, that value will be presented, and then fund flows and
                  AUM will be calculated. When you are manually calculating
                  actual AUM on a market holiday or a rolled date, it will
                  differ from the value shown in the FactSet workstation. This
                  is due to the previous day's NAV being used in the manual AUM
                  calculation.</p>
            /factset-funds/v1/flows:
              get:
                tags:
                  - Get
                  - Fund
                  - Flows
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                summary: Get Fund Flows for a requested date range and list of ids
                description: >
                  Get the Fund Flows. One-day fund flows are calculated by
                  subtracting the shares outstanding at previous close from the
                  shares outstanding one day prior to close, and then
                  multiplying the result by the net asset value (NAV) of one day
                  prior to close.


                  The fund flows calculation breaks down as follows - 

                  (Shares Outstanding T0 - Shares Outstanding T-1) * NAV T-1

                  While NAVs are routinely reported on a trade-day (T0) basis,
                  industry-wide shares outstanding are a mixture of trade-day
                  and next-day values. Trade-day values are not verified, as the
                  actual creation/redemption activity takes place late in the
                  evening, after NAVs and shares outstanding values have been
                  published. The result is that multiple industry flows are
                  calculated using unverified T0 values.

                  FactSet has standardized all shares outstanding reporting on a
                  next-day basis. To ensure that assets under management (AUM)
                  and fund flows are synchronized, FactSet synchronizes shares
                  outstanding values and changes with NAVs reported on the
                  previous day, as the creations and redemptions used the
                  previous day's reported NAVs as a transaction price. <p>For
                  more information on Fund Flows Methodology, Time Windows,
                  Makret Holidays, and Missing Values, visit - [OA
                  #17863](https://my.apps.factset.com/oa/pages/17863#Flows_Calculation)</p>
              post:
                tags:
                  - Get
                  - Fund
                  - Flows
                  - For
                  - Requested
                  - Date
                  - Range
                  - And
                  - Large
                  - List
                  - Of
                  - Ids
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                summary: >-
                  Get Fund Flows for a requested date range and large list of
                  ids
                description: >
                  Get the Fund Flows. One-day fund flows are calculated by
                  subtracting the shares outstanding at previous close from the
                  shares outstanding one day prior to close, and then
                  multiplying the result by the net asset value (NAV) of one day
                  prior to close.


                  The fund flows calculation breaks down as follows - 

                  (Shares Outstanding T0 - Shares Outstanding T-1) * NAV T-1

                  While NAVs are routinely reported on a trade-day (T0) basis,
                  industry-wide shares outstanding are a mixture of trade-day
                  and next-day values. Trade-day values are not verified, as the
                  actual creation/redemption activity takes place late in the
                  evening, after NAVs and shares outstanding values have been
                  published. The result is that multiple industry flows are
                  calculated using unverified T0 values.

                  FactSet has standardized all shares outstanding reporting on a
                  next-day basis. To ensure that assets under management (AUM)
                  and fund flows are synchronized, FactSet synchronizes shares
                  outstanding values and changes with NAVs reported on the
                  previous day, as the creations and redemptions used the
                  previous day's reported NAVs as a transaction price. <p>For
                  more information on Fund Flows Methodology, Time Windows,
                  Makret Holidays, and Missing Values, visit - [OA
                  #17863](https://my.apps.factset.com/oa/pages/17863#Flows_Calculation)</p>
            /factset-funds/v1/status:
              get:
                tags:
                  - Get
                  - Fund's
                  - Current
                  - Status
                  - And
                  - Database
                  - Availability
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                  - Status
                summary: Get Fund's current status and database availability
                description: >
                  Get the funds active status, share class status, and database
                  availability. Most common use is for coverage checks and id
                  resolution checks.
              post:
                tags:
                  - Get
                  - Fund's
                  - Current
                  - Status
                  - And
                  - Database
                  - Availability
                  - For
                  - Large
                  - List
                  - Of
                  - Ids.
                  - Factset
                  - Funds
                  - V1
                  - Summary
                  - Classifications
                  - Benchmark
                  - Details
                  - Costs
                  - Fees
                  - Managers
                  - Related
                  - Prices
                  - Returns
                  - Snapshot
                  - Range
                  - Aum
                  - Flows
                  - Status
                summary: >-
                  Get Fund's current status and database availability for large
                  list of ids.
                description: >
                  Get the funds active status, share class status, and database
                  availability. Most common use is for coverage checks and i
    overlays:
      - type: APIs.io Search
        url: overlays/funds-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/funds-openapi-api-evangelist-ratings.yml
    aid: factset:factset-funds-api
  - name: FactSet Real-Time Quotes API
    description: >-
      The Quotes API combines endpoints for retrieving security end-of-day,
      delayed, and realtime prices with performance key figures and basic
      reference data on the security and market level.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-quotes-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/real-time-quotes-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Quotes API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /basic/assetClass/list:
              get:
                tags:
                  - List
                  - Of
                  - Asset
                  - Classes.
                  - Class
                  - List
                description: List of asset classes as defined by FactSet Digital Solutions.
                summary: List of asset classes.
            /basic/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                summary: List of background text types.
                description: List of background text types.
            /basic/benchmark/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Benchmark
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                summary: List of benchmark types.
                description: List of benchmark types.
            /basic/delivery/list:
              post:
                tags:
                  - List
                  - Of
                  - Deliveries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                summary: List of deliveries.
                description: List of deliveries.
            /basic/frequency/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Frequency
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                summary: List of frequency types.
                description: List of frequency types.
            /basic/language/get:
              get:
                tags:
                  - Details
                  - For
                  - Language.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                description: Details for a language.
                summary: Details for a language.
            /basic/language/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Language
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: Details for a language identified by code.
                summary: Details for a language identified by code.
            /basic/language/list:
              get:
                tags:
                  - List
                  - Of
                  - Languages.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                description: List of languages.
                summary: List of languages.
            /basic/market/get:
              get:
                tags:
                  - Details
                  - Of
                  - Market.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: Details of a market.
                summary: Details of a market.
            /basic/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                description: List of markets.
                summary: List of markets.
            /basic/market/group/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Groups.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market groups.
                summary: List of market groups.
            /basic/market/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Market
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                description: List of market types.
                summary: List of market types.
            /basic/media/kind/list:
              get:
                tags:
                  - List
                  - Of
                  - Media
                  - Kinds.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                summary: List of media kinds.
                description: List of media kinds.
            /basic/media/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Internet
                  - Media
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                description: >-
                  List of Internet media types. See
                  http://www.iana.org/assignments/media-types/ for further
                  details. Not all such Internet media types are available on
                  the MDG.
                summary: List of Internet media types.
            /basic/mic/operating/list:
              post:
                tags:
                  - List
                  - Of
                  - Operating
                  - Market
                  - Identifier
                  - Codes
                  - C).
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                summary: List of operating market identifier codes (MIC).
                description: List of operating market identifier codes (MIC).
            /basic/region/get:
              get:
                tags:
                  - Details
                  - For
                  - Region.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: Details for a region.
                description: Details for a geographic, political, or economic region.
            /basic/region/list:
              get:
                tags:
                  - List
                  - Of
                  - Regions.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                summary: List of regions.
                description: List of geographic, political, and economic regions.
            /basic/region/continent/get:
              get:
                tags:
                  - Details
                  - For
                  - Continent.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: Details for a continent.
                description: Details for a continent.
            /basic/region/continent/list:
              get:
                tags:
                  - List
                  - Of
                  - Continents.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                summary: List of continents.
                description: List of continents.
            /basic/region/country/get:
              get:
                tags:
                  - Details
                  - For
                  - Country.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country.
                description: Details for a country.
            /basic/region/country/getByCode:
              get:
                tags:
                  - Details
                  - For
                  - Country
                  - Identified
                  - By
                  - Code.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: Details for a country identified by code.
                description: Details for a country identified by code.
            /basic/region/country/list:
              get:
                tags:
                  - List
                  - Of
                  - Countries.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                summary: List of countries.
                description: List of countries.
            /basic/timezone/get:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                description: >-
                  Details of a timezone identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone.
            /basic/timezone/getByName:
              get:
                tags:
                  - Details
                  - Of
                  - Timezone
                  - Identified
                  - By
                  - Name.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  Details of a timezone identified by name, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: Details of a timezone identified by name.
            /basic/timezone/list:
              post:
                tags:
                  - List
                  - Of
                  - Timezones.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                description: >-
                  List of timezones identified by id, as specified by the
                  Internet Assigned Numbers Authority. See
                  http://www.iana.org/time-zones for further details. Not all
                  such timezones are available on the MDG.
                summary: List of timezones.
            /basic/valueUnit/get:
              get:
                tags:
                  - Details
                  - Of
                  - Value
                  - Unit.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: Details of a value unit.
                description: Details of a value unit.
            /basic/valueUnit/list:
              post:
                tags:
                  - List
                  - Of
                  - Value
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                summary: List of value units.
                description: List of value units.
            /basic/valueUnit/alternative/list:
              get:
                tags:
                  - List
                  - Of
                  - Alternative
                  - Units.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                description: List of alternative units.
                summary: List of alternative units.
            /basic/valueUnit/currency/list:
              post:
                tags:
                  - List
                  - Of
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                summary: List of currencies.
                description: List of currencies.
            /basic/valueUnit/currency/fractional/get:
              get:
                tags:
                  - Details
                  - Of
                  - Fractional
                  - Currency.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: Details of a fractional currency.
                description: Details of a fractional currency.
            /basic/valueUnit/currency/fractional/list:
              get:
                tags:
                  - List
                  - Of
                  - Fractional
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                summary: List of fractional currencies.
                description: List of fractional currencies.
            /basic/valueUnit/currency/main/list:
              post:
                tags:
                  - List
                  - Of
                  - Main
                  - Currencies.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                summary: List of main currencies.
                description: List of main currencies.
            /category/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: Details of a category.
                description: Details of a category.
            /category/list:
              get:
                tags:
                  - List
                  - Of
                  - Categories.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                summary: List of categories.
                description: List of categories.
            /category/listByLevel:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                summary: List of categories assigned to a category level.
                description: List of categories assigned to a category level.
            /category/listBySystem:
              get:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                summary: List of categories assigned to a category system.
                description: List of categories assigned to a category system.
            /category/dataset/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Datasets.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                summary: List of entitled category datasets.
                description: List of entitled category datasets.
            /category/instrument/list:
              get:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Where
                  - Specific
                  - Dataset
                  - Has
                  - Assigned
                  - Given
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
                description: >-
                  List of instruments where a specific dataset has assigned a
                  given category.
            /category/level/get:
              get:
                tags:
                  - Details
                  - Of
                  - Category
                  - Level.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                summary: Details of a category level.
                description: Details of a category level.
            /category/path/get:
              get:
                tags:
                  - Path
                  - From
                  - The
                  - First
                  - Level
                  - To
                  - Of
                  - Specific
                  - Category.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Path from the first level to the level of a specific category.
                description: Path from the first level to the level of a specific category.
            /category/system/get:
              get:
                tags:
                  - Details
                  - Of
                  - An
                  - Entitled
                  - Category
                  - System.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: Details of an entitled category system.
                description: Details of an entitled category system.
            /category/system/list:
              get:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Category
                  - Systems.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of entitled category systems.
                description: List of entitled category systems.
            /category/system/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Category
                  - System
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                summary: List of category system types.
                description: List of category system types.
            /instrument/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/getByNotation:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                description: Basic data for an instrument.
                summary: Basic data for an instrument.
            /instrument/backgroundText/list:
              get:
                tags:
                  - Background
                  - Texts
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: Background texts of an instrument.
                description: Background texts of an instrument.
            /instrument/backgroundText/type/list:
              post:
                tags:
                  - List
                  - Of
                  - Background
                  - Text
                  - Types
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of background text types for instruments.
                description: List of background text types for instruments.
            /instrument/benchmark/list:
              post:
                tags:
                  - List
                  - Of
                  - Benchmarks
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: List of benchmarks of a financial instrument.
                description: >-
                  Provides a list of benchmark notations for a selected
                  financial instrument, optionally restricted to specific
                  benchmark types.
            /instrument/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Instrument
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                summary: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see.
                description: >-
                  List of categories assigned to a specific instrument the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
            /instrument/complianceProperty/list:
              post:
                tags:
                  - List
                  - Of
                  - Compliance
                  - Properties
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: List of compliance properties for instruments.
                description: List of compliance properties for instruments.
            /instrument/complianceProperty/listByInstrument:
              get:
                tags:
                  - Compliance
                  - Properties
                  - Of
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                summary: Compliance properties of an instrument.
                description: Compliance properties of an instrument.
            /instrument/composite/get:
              get:
                tags:
                  - Composite
                  - Instrument
                  - And
                  - Its
                  - Components.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                summary: Composite instrument and its components.
                description: Composite instrument and its components.
            /instrument/coupon/list:
              get:
                tags:
                  - List
                  - Of
                  - Coupons
                  - For
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                summary: List of coupons for an interest-bearing instrument.
                description: >-
                  List of coupons for an interest-bearing instrument; any other
                  instrument yields empty values. The endpoint provides details
                  regarding the coupon period, the respective interest rate, and
                  payable amount (the latter only for instruments with a fixed
                  nominal value). The list of coupons is generally not available
                  for a perpetual, i.e. without a predefined maturity date,
                  interst-bearing instrument. 


                  If there is no entitled provider supplying a full list of
                  coupons, the list will be synthesized from summary data
                  available from entitled suppliers (if any). Since the exact
                  product terms are not known, e.g. the handling of holidays and
                  weekends, the list may be imprecise.
            /instrument/coupon/dayCountConvention/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Day
                  - Count
                  - Convention
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                summary: List of day count convention types.
                description: List of day count convention types.
            /instrument/coupon/interestRate/type/list:
              get:
                tags:
                  - List
                  - Of
                  - Interest
                  - Rate
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                summary: List of interest rate types.
                description: List of interest rate types.
            /instrument/coupon/keyData/get:
              get:
                tags:
                  - Interest
                  - Rate
                  - Details
                  - For
                  - Selected
                  - Periods
                  - Of
                  - An
                  - Interest-bearing
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                summary: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument.
                description: >-
                  Interest rate details for selected periods of an
                  interest-bearing instrument; any other instrument yields empty
                  values.
            /instrument/crossReference/getByISIN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given ISIN to the respective most recent
                  instrument identifier, retrieved from the Cross Reference
                  Service.
                summary: Translate ISIN to instrument.
            /instrument/crossReference/getByWKN:
              get:
                tags:
                  - Translate
                  - To
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given WKN to the respective most recent instrument
                  identifier, retrieved from the Cross Reference Service.
                summary: Translate WKN to instrument.
            /instrument/crossReference/listByISIN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of ISINs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of ISINs to instruments.
            /instrument/crossReference/listByWKN:
              post:
                tags:
                  - Translate
                  - List
                  - Of
                  - Ns
                  - To
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                description: >-
                  Translate a given list of WKNs to the respective most recent
                  instrument identifiers, retrieved from the Cross Reference
                  Service.
                summary: Translate a list of WKNs to instruments.
            /instrument/crossReference/history/getByISIN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given ISIN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: ISIN to instrument translation history.
            /instrument/crossReference/history/getByWKN:
              get:
                tags:
                  - To
                  - Instrument
                  - Translation
                  - History.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve the complete translation history of a given WKN to
                  the respective instrument association from the Cross Reference
                  Service. The results are sorted in descending order, starting
                  with the most recent.
                summary: WKN to instrument translation history.
            /instrument/exchangeRate/get:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the
                  identifier of the main currencies represented by that exchange
                  rate. 

                   An error is returned if one of the provided parameters is invalid or if no instrument is associated with the given combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/exchangeRate/getByISOCode:
              get:
                tags:
                  - Retrieve
                  - An
                  - Exchange
                  - Rate
                  - Instrument
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                description: >-
                  Retrieve an exchange rate instrument identifier using the ISO
                  4217 code of the main currencies represented by that exchange
                  rate. 


                  An error is returned if one of the provided parameters is
                  invalid or if no instrument is associated with the given
                  combination of parameters.
                summary: Retrieve an exchange rate instrument identifier.
            /instrument/legalEntity/backgroundText/list:
              get:
                tags:
                  - Role-specific
                  - Background
                  - Texts
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                summary: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
                description: >-
                  Role-specific background texts of legal entities related to an
                  instrument.
            /instrument/legalEntity/complianceProperty/list:
              get:
                tags:
                  - Role-specific
                  - Compliance
                  - Properties
                  - Of
                  - Legal
                  - Entities
                  - Related
                  - To
                  - An
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                summary: >-
                  Role-specific compliance properties of legal entities related
                  to an instrument.
                description: >-
                  Role-specic compliance properties of legal entities related to
                  an instrument.
            /instrument/mifid/get:
              get:
                tags:
                  - Mi
                  - Data
                  - For
                  - Financial
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                description: >-
                  MiFID II data for a specified financial instrument. The
                  instruments governed by MiFID II are called "investment
                  products".
                summary: MiFID II data for a financial instrument.
            /instrument/notation/list:
              post:
                tags:
                  - List
                  - Of
                  - Active,
                  - Entitled
                  - Notations
                  - For
                  - Set
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                summary: List of active, entitled notations for a set of instruments.
                description: >-
                  List of active, entitled notations for a set of instruments.
                  By default the list of notations (per instrument) is sorted
                  descending by the trading volume, averaged over one month. All
                  identifiers used as parameters must be valid and entitled.
            /instrument/rating/grade/list:
              post:
                tags:
                  - List
                  - Of
                  - Rating
                  - Grades
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  List of rating grades for a list of instruments. The list can
                  be restricted to rating grades belonging to particular rating
                  systems.
                summary: List of rating grades for a list of instruments.
            /instrument/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Instrument-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: Set of custom instrument-level selection lists.
                summary: Set of custom instrument-level selection lists.
            /instrument/selectionList/listByInstrument:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Instrument,
                  - Returns
                  - The
                  - Instrument-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Instrument
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                description: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
                summary: >-
                  For each given instrument, returns the instrument-level
                  selection lists of which the instrument is a member.
            /instrument/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Instruments
                  - Belonging
                  - To
                  - An
                  - Instrument-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                summary: >-
                  List of instruments belonging to an instrument-level selection
                  list.
                description: >-
                  List of instruments belonging to an instrument-level selection
                  list.
            /notation/get:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a notation.
                summary: Basic data for a notation.
            /notation/list:
              get:
                tags:
                  - Basic
                  - Data
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: Basic data for a list of notations.
                summary: Basic data for a list of notations.
            /notation/category/list:
              post:
                tags:
                  - List
                  - Of
                  - Categories
                  - Assigned
                  - To
                  - Specific
                  - Notation
                  - The
                  - Application
                  - Is
                  - Entitled
                  - See.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                description: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see. Optionally it is possible to
                  restrict the output to only list those for a specific category
                  dataset.
                summary: >-
                  List of categories assigned to a specific notation the
                  application is entitled to see.
            /notation/crossReference/getByFactSetMarketSymbol:
              get:
                tags:
                  - Translate
                  - Fact
                  - Set
                  - Market
                  - Symbol
                  - To
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: Translate a FactSet market symbol to a notation.
                description: >-
                  Translate a FactSet market symbol to a notation. This symbol
                  is also known as TICKER_EXCHANGE.
            /notation/crossReference/listByInstrument:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listByISIN:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: List of entitled notations.
            /notation/crossReference/listBySymbol:
              post:
                tags:
                  - List
                  - Of
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                summary: List of entitled notations.
                description: >-
                  List of entitled notations. Symbols are not globally unique;
                  therefore, a given symbol interpreted in different markets
                  might refer to different instruments.
            /notation/crossReference/factSetIdentifier/get:
              get:
                tags:
                  - Retrieve
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve FactSet identifiers for a given notation.
                description: >-
                  <p>Retrieve FactSet identifiers for a given notation. Security
                  and listing-level identifiers are always included, regional
                  level identifiers are included, if available.
            /notation/crossReference/factSetIdentifier/listByFactSetIdentifier:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Notations
                  - For
                  - Given
                  - Fact
                  - Set
                  - Identifier.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of notations for a given FactSet identifier.
                description: >-
                  <p>Retrieve a list of notations for a given FactSet
                  identifier, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>See the group
                  description for more information about the security's primary
                  listing.</p>
            /notation/crossReference/factSetIdentifier/listByInstrument:
              post:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Fact
                  - Set
                  - Identifiers
                  - For
                  - Given
                  - Instrument.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                summary: Retrieve a list of FactSet identifiers for a given instrument.
                description: >-
                  <p>Retrieve a list of FactSet identifiers for a given
                  instrument, grouped by regional identifiers, if available.
                  Listings without a regional identifier are grouped at the end
                  of the response.</p><p>The notation corresponding to the
                  security's primary listing has the attributes
                  <big><tt>regional.isPrimary</tt></big> and
                  <big><tt>regional.listing.isPrimary</tt></big> both set to
                  true.The security's primary listing might not be among the
                  results depending on the entitlement.</p><p>The result
                  contains only notations that have at least one FactSet
                  identifier (see
                  <big><tt>listing.permanentIdentifier</tt></big>,
                  <big><tt>listing.tickerExchange</tt></big>).</p><p>See the
                  group description for more information about the security's
                  primary listing.</p>
            /notation/keyFigures/year/10/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: End-of-day (EOD) key figures for the time range of ten years.
                description: End-of-day (EOD) key figures for the time range of ten years.
            /notation/keyFigures/year/10/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Ten
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                summary: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of ten years,
                  for a list of notations.
            /notation/keyFigures/month/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: End-of-day (EOD) key figures for the time range of one month.
                description: End-of-day (EOD) key figures for the time range of one month.
            /notation/keyFigures/month/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Month,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                summary: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one month,
                  for a list of notations.
            /notation/keyFigures/week/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one week.
                description: End-of-day (EOD) key figures for the time range of one week.
            /notation/keyFigures/week/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Week,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one week,
                  for a list of notations.
            /notation/keyFigures/year/1/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of one year.
                description: End-of-day (EOD) key figures for the time range of one year.
            /notation/keyFigures/year/1/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - One
                  - Year,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of one year,
                  for a list of notations.
            /notation/keyFigures/month/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months.
            /notation/keyFigures/month/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  months, for a list of notations.
            /notation/keyFigures/year/3/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years.
            /notation/keyFigures/year/3/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Three
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of three
                  years, for a list of notations.
            /notation/keyFigures/year/5/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of five years.
                description: End-of-day (EOD) key figures for the time range of five years.
            /notation/keyFigures/year/5/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Five
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of five years,
                  for a list of notations.
            /notation/keyFigures/month/6/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: End-of-day (EOD) key figures for the time range of six months.
                description: End-of-day (EOD) key figures for the time range of six months.
            /notation/keyFigures/month/6/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Six
                  - Months,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of six months,
                  for a list of notations.
            /notation/keyFigures/year/7/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years.
            /notation/keyFigures/year/7/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Of
                  - Seven
                  - Years,
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                summary: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
                description: >-
                  End-of-day (EOD) key figures for the time range of seven
                  years, for a list of notations.
            /notation/keyFigures/yearToDate/get:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D)..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD)..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD). The time range YTD begins with the last trading day of
                  the previous calendar year for which EOD prices are available
                  and ends with the most recent trading day of the current
                  calendar year for which EOD prices are available..
            /notation/keyFigures/yearToDate/list:
              get:
                tags:
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - The
                  - Time
                  - Range
                  - Year-to-date
                  - D),
                  - List
                  - Of
                  - Notations..
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                summary: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations..
                description: >-
                  End-of-day (EOD) key figures for the time range year-to-date
                  (YTD), for a list of notations. The time range YTD begins with
                  the last trading day of the previous calendar year for which
                  EOD prices are available and ends with the most recent
                  tradingday of the current calendar year for which EOD prices
                  are available..
            /notation/keyFigures/tradingDay/average/get:
              get:
                tags:
                  - Average
                  - End-of-day
                  - D)
                  - Key
                  - Figures
                  - For
                  - Different
                  - Trading
                  - Days
                  - Periods.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods. A trading day is a calendar day on that trading
                  of the notation was possible.
                summary: >-
                  Average end-of-day (EOD) key figures for different trading
                  days periods.
            /notation/market/list:
              post:
                tags:
                  - List
                  - Of
                  - Markets
                  - With
                  - Entitled
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  List of markets with entitled notations. The list contains
                  only markets with at least one active and entitled notation. 

                  All identifiers used as parameters must be valid and entitled.
                summary: List of markets with entitled notations.
            /notation/selectionList/list:
              get:
                tags:
                  - Set
                  - Of
                  - Custom
                  - Notation-level
                  - Selection
                  - Lists.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: Set of custom notation-level selection lists.
                summary: Set of custom notation-level selection lists.
            /notation/selectionList/listByNotation:
              get:
                tags:
                  - For
                  - Each
                  - Given
                  - Notation,
                  - Returns
                  - The
                  - Notation-level
                  - Selection
                  - Lists
                  - Of
                  - Which
                  - Notation
                  - Is
                  - Member.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                description: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
                summary: >-
                  For each given notation, returns the notation-level selection
                  lists of which the notation is a member.
            /notation/selectionList/members/list:
              post:
                tags:
                  - List
                  - Of
                  - Notations
                  - Belonging
                  - To
                  - Notation-level
                  - Selection
                  - List.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                summary: >-
                  List of notations belonging to a notation-level selection
                  list.
                description: >-
                  List of notations belonging to a notation-level selection
                  list.
            /notation/status/get:
              get:
                tags:
                  - Intraday
                  - Trading
                  - Status
                  - Of
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                description: >-
                  Intraday trading status of a notation.<br>The endpoint is
                  subscribable to provide push updates. See attribute
                  `_subscriptionMinimalInterval` for valid update rates.
                summary: Intraday trading status of a notation.
            /prices/get:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/list:
              get:
                tags:
                  - Overview
                  - Of
                  - Trading
                  - 'On'
                  - The
                  - Most
                  - Recent
                  - Day,
                  - Including
                  - Latest
                  - Price,
                  - For
                  - List
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                summary: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
                description: >-
                  Overview of trading on the most recent trading day, including
                  the latest price, for a list of notations.
            /prices/bidAsk/get:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - Notation.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a
                  notation.


                  The endpoint is subscribable to provide push updates. See
                  attribute `_subscriptionMinimalInterval` for valid update
                  rates.
            /prices/bidAsk/list:
              get:
                tags:
                  - Most
                  - Recent
                  - Bid
                  - And
                  - Ask
                  - Prices
                  - (best
                  - Offer)
                  - For
                  - List
                  - Of
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                summary: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
                description: >-
                  Most recent bid and ask prices (best bid / offer) for a list
                  of notations.
            /prices/orderbook/aggregated/get:
              get:
                tags:
                  - Orderbook
                  - Aggregated
                  - By
                  - Price.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                summary: Orderbook aggregated by price.
                description: Orderbook aggregated by price.
            /prices/orderbook/full/get:
              get:
                tags:
                  - Full
                  - Orderbook
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                summary: Full orderbook
                description: Full orderbook
            /prices/tradingSchedule/event/list:
              post:
                tags:
                  - Sequence
                  - Of
                  - Market-related
                  - Events.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Sequence of market-related events.
                description: >-
                  Sequence of market-related events like the opening time or
                  closing time of a market of a specific
                  notation.<br><br>Pagination to a previous page is not
                  supported and `pagination.previous` is always `null`.
            /prices/tradingSchedule/event/type/list:
              get:
                tags:
                  - Trading
                  - Schedule
                  - Event
                  - Types.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                summary: Trading schedule event types.
                description: >-
                  Trading schedule event types define the events which may occur
                  during any period of trading. Types of trading schedule events
                  are for instance OPEN, CLOSE, END_OF_DAY.
            /instrument/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Instruments.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for instruments.
                description: >-
                  Search for instruments whose ISIN, specified NSINs, or name
                  match the search value according to a tolerant full-text match
                  algorithm. Better matching results appear in the response
                  before less relevant matches.
            /notation/search/basic:
              get:
                tags:
                  - Basic
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Basic search for notations.
                description: >-
                  Search for a notation whose ISIN, specified NSINs, name, or
                  symbol match the search value according to a tolerant
                  full-text match algorithm. If more than one notation of an
                  instrument matches, only the notation with the highest
                  monetary trading volume, averaged over one month, is
                  considered. Better matching results appear in the response
                  before less relevant matches. If the parameter popularity is
                  set to true, the popularity of the notation is the primary
                  sort criterion. Popularity is affected mostly by the request
                  frequency of the notation.
            /notation/searchByText:
              post:
                tags:
                  - Text-based
                  - Search
                  - For
                  - Notations.
                  - Class
                  - List
                  - Text
                  - Type
                  - Basic
                  - Benchmark
                  - Delivery
                  - Frequency
                  - Language
                  - Get
                  - By
                  - Code
                  - Market
                  - Group
                  - Media
                  - Kind
                  - Mic
                  - Operating
                  - Region
                  - Continent
                  - Country
                  - Timezone
                  - Name
                  - Unit
                  - Alternative
                  - Currency
                  - Fractional
                  - Main
                  - Category
                  - Level
                  - System
                  - Dataset
                  - Instrument
                  - Path
                  - Notation
                  - Property
                  - Composite
                  - Coupon
                  - Count
                  - Convention
                  - Rate
                  - Data
                  - Reference
                  - History
                  - Entity
                  - Background
                  - Compliance
                  - Mifid
                  - Rating
                  - Grade
                  - Members
                  - Fact
                  - Set
                  - Symbol
                  - Identifier
                  - Figures
                  - Year
                  - '10'
                  - Month
                  - Week
                  - To
                  - Date
                  - Trading
                  - Day
                  - Average
                  - Status
                  - Prices
                  - Ask
                  - Orderbook
                  - Aggregated
                  - Full
                  - Schedule
                  - Event
                  - Search
                summary: Text-based search for notations.
                description: >-
                  Text-based search for notations in selected identifier and
                  name attributes according to a tolerant full-text match
                  algorithm. The results satisfy all selected filters; sorting
                  by various attributes is possible. If more than one notation
                  of an instrument matches, only the notation with the best
                  market priority (according to the parameter `market.priority`)
                  or, in the absence of market priorities, only the notation
                  with the highest trading volume, averaged over one month, is
                  considered.     
                   All identifiers used as parameters must be valid and entitled.
          tags:
            - name: basic
              description: basic endpoints
            - name: category
              description: category endpoints
            - name: instrument
              description: instrument endpoints
            - name: notation
              description: notation endpoints
            - name: prices
              description: prices endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-quotes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-quotes-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-quotes-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---