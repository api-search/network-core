---
name: Corporate
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/corporate.png
url: https://example.com/apis/corporate.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Corporate
apis:
  - name: FactSet Global Prices API
    description: >-
      FactSet Global Prices API currently covers listing and composite level
      prices, volume, turnover, and VWAP data on a seven day week basis for a
      global equity universe.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-global-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-global-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-global-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-global-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-global-prices-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-global-prices-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Global Prices API
          tags:
            - name: Prices
              description: >-
                Get Security Open, High, Low, Close, Volume for a list of ids
                and date range
            - name: Returns
              description: >-
                Gets the returns data for the list of ids, date range and
                currency
          paths:
            /factset-global-prices/v1/prices:
              get:
                tags:
                  - Gets
                  - End-of-day
                  - Open,
                  - High,
                  - Low,
                  - Close
                  - For
                  - List
                  - Of
                  - Securities.
                  - Factset
                  - Global
                  - Prices
                  - V1
                summary: >-
                  Gets end-of-day Open, High, Low, Close for a list of
                  securities.
                description: >
                  Gets security prices', Open, High, Low, Close, Volume, VWAP,
                  Trade Count, and Turn Over for a specified list of securities,
                  date range, currency, and adjustment factors.
              post:
                tags:
                  - Requests
                  - End-of-day
                  - Open,
                  - High,
                  - Low,
                  - Close
                  - For
                  - Large
                  - List
                  - Of
                  - Securities.
                  - Factset
                  - Global
                  - Prices
                  - V1
                summary: >-
                  Requests end-of-day Open, High, Low, Close for a large list of
                  securities.
                description: >-
                  Gets security prices', Open, High, Low, Close, Volume, VWAP,
                  Trade Count, and Turn Over for a specified list of securities,
                  date range, currency, and adjustment factors.
            /factset-global-prices/v1/corporate-actions:
              get:
                tags:
                  - Gets
                  - Corporate
                  - Actions
                  - Information.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                summary: Gets Corporate Actions information.
                description: >
                  Gets the Corporate Actions amounts, dates, types, and flags
                  over a specified date range.

                  You may request future dates to receive information for
                  declared events.


                  Event Categories:

                  * __Cash Dividends__ (CASH_DIVS)
                    * **DVC** - Dividend
                    * **DVCD** - Dividend with DRP Option
                    * **DRP** - Dividend Reinvestment
                  * __Stock Distributions__ (STOCK_DIST)
                    * **DVS** - Stock Dividend
                    * **DVSS** - Stock Dividend, Special
                    * **BNS** - Bonus Issue
                    * **BNSS** - Bonus Issue, Special
                  * __Spin Offs__ (SPINOFFS)
                    * **SPO** - Spin Off
                  * __Rights Issue__ (RIGHTS)
                    * **DSR** - Rights Issue
                  * __Splits__ (SPLITS)
                    * **FSP** - Forward Split
                    * **RSP** - Reverse Split
                    * **SPL** - Split
                    * **EXOS** - Exchange of Securities
              post:
                tags:
                  - Requests
                  - Corporate
                  - Actions
                  - Information.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                summary: Requests Corporate Actions information.
                description: >-
                  Gets the Corporate Actions amounts, dates, types, and flags
                  over a specified date range. You may request future dates to
                  receive information for declared events. <p>**_startDate and
                  endDate are required parameters. The input startDate must come
                  before the input endDate._**
            /factset-global-prices/v1/annualized-dividends:
              get:
                tags:
                  - Gets
                  - Indicated
                  - Annualized
                  - Dividend
                  - Information.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                summary: Gets Indicated Annualized Dividend information.
                description: >
                  Gets the Annualized dividend of the latest reported dividend.

                  The annualized dividend calculations does not involve
                  cancelled dividends.
              post:
                tags:
                  - Gets
                  - Indicated
                  - Annualized
                  - Dividend
                  - Information.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                summary: Gets Indicated Annualized Dividend information.
                description: >-
                  Gets the Annualized dividend of the latest reported dividend.
                  The annualized dividend calculations does not involve
                  cancelled dividends.
            /factset-global-prices/v1/returns:
              get:
                tags:
                  - Gets
                  - Returns
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                  - Returns
                summary: Gets Returns for a list of `ids` as of given date range.
                description: >
                  Returns for the requested ids and currency for the given
                  dates. Depending on the input parameters the return data is
                  provided. 
              post:
                tags:
                  - Gets
                  - Returns
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                  - Returns
                summary: Gets Returns for a list of `ids` as of given date range.
                description: >-
                  Returns for the requested ids and currency for the given
                  dates. Depending on the input parameters the return data is
                  provided.
            /factset-global-prices/v1/security-shares:
              get:
                tags:
                  - Gets
                  - Shares
                  - Outstanding
                  - Information
                  - For
                  - Securities.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                  - Returns
                  - Security
                  - Shares
                summary: Gets Shares Outstanding information for securities.
                description: >-
                  Returns security level shares outstanding data for the given
                  ids and dates. At this time, all values returned are split
                  adjusted.
              post:
                tags:
                  - Gets
                  - Shares
                  - Outstanding
                  - Information
                  - For
                  - Securities.
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                  - Returns
                  - Security
                  - Shares
                summary: Gets Shares Outstanding information for securities.
                description: >-
                  Returns security level shares outstanding data for the given
                  ids and dates. At this time, all values returned are split
                  adjusted.
            /factset-global-prices/v1/batch-status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - |
                    Request
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                  - Returns
                  - Security
                  - Shares
                  - Batch
                  - Status
                summary: |
                  Returns the status for a Batch Request
                description: >-
                  Return the status for the underlying batch request that is
                  specified by the id.
            /factset-global-prices/v1/batch-result:
              get:
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - |
                    Request
                  - Factset
                  - Global
                  - Prices
                  - V1
                  - Corporate
                  - Actions
                  - Annualized
                  - Dividends
                  - Returns
                  - Security
                  - Shares
                  - Batch
                  - Status
                  - Result
                summary: |
                  Returns the response for a Batch Request
                description: >
                  Returns the response data for the underlying batch request
                  that is specified by the id.


                  By default, this endpoint will return data as JSON. If you
                  wish to receive your data in CSV format, you can edit the
                  header to have the "accept" parameter as "text/csv" instead of
    overlays:
      - type: APIs.io Search
        url: overlays/global-prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/global-prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-global-prices-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---