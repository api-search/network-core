---
name: Batch Processing
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/batch-processing.png
url: https://example.com/apis/batch-processing.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Batch Processing
apis:
  - name: Factset Formula API
    description: >-
      Use FactSet’s flexible, formula-based API to retrieve data from almost all
      available content sets FactSet offers through FactSet's FQL and Screening
      formulas.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/formula-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/formula-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/formula-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/formula-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/formula-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/formula-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Formula API
          paths:
            /v1/time-series:
              get:
                summary: >-
                  Retrieve data items (FQL formulas) for a list of identifiers
                  or defined universe.
                description: >
                  The `/time-series` endpoint is closely aligned with FactSet’s
                  powerful data retrieval language **FactSet Query Language
                  (FQL)** which is optimized for time-series analysis. FQL can
                  also perform sophisticated statistical, mathematical, logical,
                  and other complex operations on the data.

                    This endpoint has a unique **TIMESERIES** data object that pairs the requested data with FactSet provided dates. This helps reduce the need for additional data requests and reduces the work required by users.

                  The `/time-series` endpoint supports Long Running asynchronous
                  requests up to **20 minutes** via the `batch` parameter. *This
                  feature is available to Individual Users subscribed to the
                  Performance Package and Performance Package Plus Performance
                  Tiers and all Production Users. If you are unsure which
                  Performance Tier you are subscribed to or you would like to
                  gain access to the batch capabilities, please contact your
                  FactSet Account Team or "Report Issue" above and our support
                  teams can assist.*
                tags:
                  - Retrieve
                  - Data
                  - Items
                  - Formulas)
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Or
                  - Defined
                  - Universe.
                  - V1
                  - Time
                  - Series
              post:
                summary: >-
                  Retrieve data items (FQL formulas) for a list of identifiers
                  or defined universe.
                description: >
                  The `/time-series` endpoint is closely aligned with FactSet’s
                  powerful data retrieval language **FactSet Query Language
                  (FQL)** which is optimized for time-series analysis. FQL can
                  also perform sophisticated statistical, mathematical, logical,
                  and other complex operations on the data.

                    This endpoint has a unique **TIMESERIES** data object that pairs the requested data with FactSet provided dates. This helps reduce the need for additional data requests and reduces the work required by users.

                  The `/time-series` endpoint supports Long Running asynchronous
                  requests up to **20 minutes** via the `batch` parameter. *This
                  feature is available to Individual Users subscribed to the
                  Performance Package and Performance Package Plus Performance
                  Tiers and all Production Users. If you are unsure which
                  Performance Tier you are subscribed to or you would like to
                  gain access to the batch capabilities, please contact your
                  FactSet Account Team or "Report Issue" above and our support
                  teams can assist.*
                tags:
                  - Retrieve
                  - Data
                  - Items
                  - Formulas)
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Or
                  - Defined
                  - Universe.
                  - V1
                  - Time
                  - Series
            /v1/cross-sectional:
              get:
                summary: >-
                  Retrieve data items (Screening formulas) for a list of
                  identifiers or defined universe.
                description: >
                  The `/cross-sectional` endpoint is closely aligned with
                  FactSet’s powerful data retrieval **Screening language** which
                  is optimized for analysis of data items at single point in
                  time for different entities and is extremely efficient for
                  large universes.



                  The `/cross-sectional` endpoint supports Long Running
                  asynchronous requests up to **10 minutes** via the `batch`
                  parameter. *This feature is available to Individual Users
                  subscribed to the Performance Package and Performance Package
                  Plus Performance Tiers and all Production Users. If you are
                  unsure which Performance Tier you are subscribed to or you
                  would like to gain access to the batch capabilities, please
                  contact your FactSet Account Team or "Report Issue" above and
                  our support teams can assist.*


                  ***


                  ### Iterated Cross-Sectional Functionality



                  This endpoint supports the ability to automatically iterate
                  through different cross sections over time. The **Iterated
                  Cross-Sectional Functionality (ICSF)** expands the
                  Cross-Sectional endpoint to support retrieving data items for
                  *multiple dates*, allowing users to take advantage of the
                  Screening engine’s efficiency even when history is required. 



                  Use the parameters `startDate`, `endDate`, and `frequency` in
                  the Cross-Sectional endpoint to provide your desired dates.
                  Specify “0” in date argument of the Screening formulas
                  provided in the formulas parameter and/or the universe
                  parameter. Lastly, the Iterated Cross-Sectional Functionality
                  is required to run as a `batch` request. Therefore, the batch
                  parameter must be set to “Y”. 



                  Access to backtesting and batch functionality is required to
                  leverage the Iterated Cross-Sectional Functionality. 


                  **When to use ICSF:**


                  The ICSF can offer better performance than Time-Series
                  requests when the date range is relatively small, and so it is
                  recommended to use ICSF if the number of IDs requested is
                  greater than the number of dates. If the number of dates is
                  greater than the number of IDs in the request, it is
                  recommended to use Time-Series.


                  *Note: This is a general rule of thumb and performance may
                  vary depending on the formulas in use.*
                tags:
                  - Retrieve
                  - Data
                  - Items
                  - Screening
                  - Formulas)
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Or
                  - Defined
                  - Universe.
                  - V1
                  - Time
                  - Series
                  - Cross
                  - Sectional
              post:
                summary: >-
                  Retrieve data items (Screening formulas) for a list of
                  identifiers or defined universe.
                description: >
                  The `/cross-sectional` endpoint is closely aligned with
                  FactSet’s powerful data retrieval **Screening language** which
                  is optimized for analysis of data items at single point in
                  time for different entities and is extremely efficient for
                  large universes.



                  The `/cross-sectional` endpoint supports Long Running
                  asynchronous requests up to **10 minutes** via the `batch`
                  parameter. *This feature is available to Individual Users
                  subscribed to the Performance Package and Performance Package
                  Plus Performance Tiers and all Production Users. If you are
                  unsure which Performance Tier you are subscribed to or you
                  would like to gain access to the batch capabilities, please
                  contact your FactSet Account Team or "Report Issue" above and
                  our support teams can assist.*


                  ***


                  ### Iterated Cross-Sectional Functionality



                  This endpoint supports the ability to automatically iterate
                  through different cross sections over time. The **Iterated
                  Cross-Sectional Functionality (ICSF)** expands the
                  Cross-Sectional endpoint to support retrieving data items for
                  *multiple dates*, allowing users to take advantage of the
                  Screening engine’s efficiency even when history is required. 



                  Use the parameters `startDate`, `endDate`, and `frequency` in
                  the Cross-Sectional endpoint to provide your desired dates.
                  Specify “0” in date argument of the Screening formulas
                  provided in the formulas parameter and/or the universe
                  parameter. Lastly, the Iterated Cross-Sectional Functionality
                  is required to run as a `batch` request. Therefore, the batch
                  parameter must be set to “Y”. 



                  Access to backtesting and batch functionality is required to
                  leverage the Iterated Cross-Sectional Functionality. 


                  **When to use ICSF:**


                  The ICSF can offer better performance than Time-Series
                  requests when the date range is relatively small, and so it is
                  recommended to use ICSF if the number of IDs requested is
                  greater than the number of dates. If the number of dates is
                  greater than the number of IDs in the request, it is
                  recommended to use Time-Series. 


                  *Note: This is a general rule of thumb and performance may
                  vary depending on the formulas in use.*
                tags:
                  - Retrieve
                  - Data
                  - Items
                  - Screening
                  - Formulas)
                  - For
                  - List
                  - Of
                  - Identifiers
                  - Or
                  - Defined
                  - Universe.
                  - V1
                  - Time
                  - Series
                  - Cross
                  - Sectional
            /v1/batch-status:
              get:
                summary: Returns the status for a Batch Request
                description: >
                  Return the status for the underlying batch request that is
                  specified by the id.

                    The Formula API supports Long Running asynchronous requests up to **20 minutes** via the `batch` parameter in the `/time-series` endpoint and up to **10 minutes** in the `/cross-sectional` endpoint.

                    *This feature is available to Individual Users subscribed to the Performance Package and Performance Package Plus Performance Tiers and all Production Users. If you are unsure which Performance Tier you are subscribed to or you would like to gain access to the batch capabilities, please contact your FactSet Account Team or "Report Issue" above and our support teams can assist.*
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - V1
                  - Time
                  - Series
                  - Cross
                  - Sectional
                  - Batch
                  - Status
              post:
                summary: Returns the status for a Batch Request
                description: >
                  Return the status for the underlying batch request that is
                  specified by the id.

                    The Formula API supports Long Running asynchronous requests up to **20 minutes** via the `batch` parameter in the `/time-series` endpoint and up to **10 minutes** in the `/cross-sectional` endpoint.

                    *This feature is available to Individual Users subscribed to the Performance Package and Performance Package Plus Performance Tiers and all Production Users. If you are unsure which Performance Tier you are subscribed to or you would like to gain access to the batch capabilities, please contact your FactSet Account Team or "Report Issue" above and our support teams can assist.*
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - V1
                  - Time
                  - Series
                  - Cross
                  - Sectional
                  - Batch
                  - Status
            /v1/batch-result:
              get:
                summary: Returns the response for a Batch Request
                description: >
                  Returns the response data for the underlying batch request
                  that is specified by the id.

                    The Formula API supports Long Running asynchronous requests up to **20 minutes** via the `batch` parameter in the `/time-series` endpoint and up to **10 minutes** in the `/cross-sectional` endpoint.

                    *This feature is available to Individual Users subscribed to the Performance Package and Performance Package Plus Performance Tiers and all Production Users. If you are unsure which Performance Tier you are subscribed to or you would like to gain access to the batch capabilities, please contact your FactSet Account Team or "Report Issue" above and our support teams can assist.*
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - Request
                  - V1
                  - Time
                  - Series
                  - Cross
                  - Sectional
                  - Batch
                  - Status
                  - Result
              post:
                summary: Returns the status for a Batch Request
                description: >
                  Returns the response data for the underlying batch request
                  that is specified by the id.

                    The Formula API supports Long Running asynchronous requests up to **20 minutes** via the `batch` parameter in the `/time-series` endpoint and up to **10 minutes** in the `/cross-sectional` endpoint.

                    *This feature is available to Individual Users subscribed to the Performance Package and Performance Package Plus Performance Tiers and all Production Users. If you are unsure which Performance Tier you are subscribed to or you would like to gain access to the batch capabilities, please contact your FactSet Account Team or "Report Issue" above and our support teams can assist.*
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - V1
                  - Time
                  - Series
                  - Cross
                  - Sectional
                  - Batch
                  - Status
                  - Resu
    overlays:
      - type: APIs.io Search
        url: overlays/formula-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/formula-openapi-api-evangelist-ratings.yml
    aid: factset:factset-formula-api
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
  - name: FactSet Prices API
    description: >-
      Gain access to comprehensive global coverage for equity prices, returns,
      volume, shares, splits, and dividends. Security types include Common
      Stock, ADR, GDR, Preferred, Closed-ended Fund, Exchange Traded Fund, Unit,
      Open-ended Fund, Exchange…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/factset-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-prices-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/factset-prices-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Prices API
          paths:
            /factset-prices/v1/prices:
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
                  - Prices
                  - V1
                summary: >-
                  Gets end-of-day Open, High, Low, Close for a list of
                  securities.
                description: >
                  Gets security prices, Open, High, Low, Close, Volume, and
                  currency for a specified date range and frequency. Prices are
                  updated and at different times across the different regions
                  around the globe. The Prices API automatically defaults
                  relative price dates to the local region which is determined
                  by the local region of the requested security id. To learn
                  more about relative dates please visit [OA Page
                  4627](https://my.apps.factset.com/oa/pages/4627)


                  */prices* endpoint currently supports Long Running
                  asynchronous requests up to **10 minutes** via `batch`
                  parameter. **Additional Approvals needed for access**. Id
                  limits increased to **5000 ids** per request using batch
                  parameter.
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
                  - Prices
                  - V1
                summary: >-
                  Requests end-of-day Open, High, Low, Close for a large list of
                  securities.
                description: >

                  Gets security prices, Open, High, Low, Close, Volume, and
                  currency for a specified date range and frequency.


                  */prices* endpoint currently supports Long Running
                  asynchronous requests up to **10 minutes** via `batch`
                  parameter. **Additional Approvals needed for access**. Id
                  limits increased to **5000 ids** per request using batch
                  parameter.
            /factset-prices/v1/fixed-income:
              get:
                tags:
                  - Gets
                  - Pricing
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                summary: Gets pricing for a list of Fixed Income securities
                description: >
                  Get BID, MID, ASK, and Issuer Entity ID for a list of Fixed
                  Income Securities as of a requested date range. Available for
                  U.S. Corporate, Treasury and Agency bonds, Municipals, and
                  non-U.S. Corporate and Government bonds. To learn more about
                  Fixed Income Prices database, please review
                  [OA:15995](https://my.apps.factset.com/oa/pages/15995)
              post:
                tags:
                  - Requests
                  - Pricing
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities
                  - Date
                  - Range
                  - Requested
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                summary: >-
                  Requests pricing for a list of Fixed Income securities for
                  date range requested
                description: >
                  Get BID, MID, ASK, and Issuer Entity ID for a list of Fixed
                  Income Securities as of a requested date range. Available for
                  U.S. Corporate, Treasury and Agency bonds, Municipals, and
                  non-U.S. Corporate and Government bonds. To learn more about
                  Fixed Income Prices database, please review
                  [OA:15995](https://my.apps.factset.com/oa/pages/15995)
            /factset-prices/v1/references:
              get:
                tags:
                  - Gets
                  - Security
                  - Reference
                  - Details
                  - For
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                summary: Gets security reference details for a list of securities
                description: >
                  Gets security reference details for a list of `ids`, such as
                  Name, Security Type, Currency, Country, Primary Exchange,
                  Local Index, and dates of First and Last Trade.
              post:
                tags:
                  - Requests
                  - Security
                  - Reference
                  - Details
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                summary: Requests security reference details a list of securities
                description: >
                  Gets security reference details for a large list of `ids`,
                  such as Name, Security Type, Currency, Country, Primary
                  Exchange, Local Index, and dates of First and Last Trade.
            /factset-prices/v1/returns:
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
                  - Range
                  - And
                  - Rolling
                  - Period
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                summary: >-
                  Gets Returns for a list of `ids` as of given date range and
                  rolling Period
                description: >-
                  The simple or compound return for the requested frequency
                  and/or rollingPeriod. Depending on the input parameters the
                  return will adjust accordingly. If you simply use frequency
                  and no rollingPeriod, the return value will represent the
                  frequency period. If you use rollingPeriod, the values will be
                  returned in actual period ends (e.g. actual month, actual
                  week, daily, etc.). General Return Calculation Details found
                  on [Online Assistant Page
                  #8748](https://oa.apps.factset.com/pages/8748)
              post:
                tags:
                  - Requests
                  - Security
                  - Returns
                  - For
                  - The
                  - Given
                  - Date
                  - Range
                  - And
                  - Rolling
                  - Period.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                summary: >-
                  Requests security returns for the given date range and
                  rollingPeriod.
                description: >-
                  The simple or compound return for the requested frequency
                  and/or rollingPeriod. Depending on the input parameters the
                  return will adjust accordingly. If you simply use frequency
                  and no rollingPeriod, the return value will represent the
                  frequency period. If you use rollingPeriod, the values will be
                  returned in actual period ends (e.g. actual month, actual
                  week, daily, etc.). General Return Calculation Details found
                  on [Online Assistant Page
                  #8748](https://oa.apps.factset.com/pages/8748)
            /factset-prices/v1/returns-snapshot:
              get:
                tags:
                  - Returns
                  - The
                  - Price
                  - Performance
                  - Of
                  - Security
                  - And
                  - Annualized
                  - Compound
                  - Total
                  - Returns.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                summary: >-
                  Returns the price performance of the security and annualized
                  compound total returns.
                description: >
                  Retrieves various return periods as of a given date for a
                  requested list of securities. This endpoint is very helpful
                  for quickly retrieving a list of pre-calculated returns for
                  application development.<p> Return periods include
                    * oneDay
                    * weekToDate
                    * monthToDate
                    * quarterToDate
                    * yearToDate
                    * oneMonth
                    * threeMonth
                    * sixMonth
                    * nineMonth
                    * oneYear
                    * twoYearAnnualized
                    * threeYearAnnualized
                    * fiveYearAnnualized
                    * tenYearAnnualized
                    * twentyYearAnnualized
                    * thirtyYearAnnualized
                    * ipoToDateAnnualized
                    </p>
              post:
                tags:
                  - Returns
                  - The
                  - Price
                  - Performance
                  - Of
                  - Security
                  - And
                  - Annualized
                  - Compound
                  - Total
                  - Returns.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                summary: >-
                  Returns the price performance of the security and annualized
                  compound total returns.
                description: >
                  Retrieves various return periods as of a given date for a
                  requested list of securities. This endpoint is very helpful
                  for quickly retrieving a list of pre-calculated returns for
                  application development.<p> Return periods include
                    * oneDay
                    * weekToDate
                    * monthToDate
                    * quarterToDate
                    * yearToDate
                    * oneMonth
                    * threeMonth
                    * sixMonth
                    * nineMonth
                    * oneYear
                    * twoYearAnnualized
                    * threeYearAnnualized
                    * fiveYearAnnualized
                    * tenYearAnnualized
                    * twentyYearAnnualized
                    * thirtyYearAnnualized
                    * ipoToDateAnnualized
                    </p>
            /factset-prices/v1/dividends:
              get:
                tags:
                  - Gets
                  - Dividend
                  - Information
                  - For
                  - Given
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                summary: >-
                  Gets dividend information for a given date range and list of
                  securities
                description: >-
                  Get the dividend amounts, dates, types, and flags over a
                  specified date range. You may request future dates to receive
                  information for declared dividends.
              post:
                tags:
                  - Requests
                  - Dividend
                  - Information
                  - For
                  - Given
                  - Date
                  - Range
                  - And
                  - List
                  - Of
                  - Securities
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                summary: >-
                  Requests dividend information for a given date range and list
                  of securities
                description: >-
                  Get the dividend amounts, dates, types, and flags over a
                  specified date range
            /factset-prices/v1/splits:
              get:
                tags:
                  - Gets
                  - Full
                  - History
                  - Of
                  - Security
                  - Splits
                  - For
                  - List
                  - '`ids`'
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                summary: Gets full history of security Splits for a list of `ids`
                description: >-
                  Gets the entire history of splits for a given list of
                  identifiers. Information returned includes the split factor, a
                  plain text comment regarding the type of split, and the event
                  date.
              post:
                tags:
                  - Requests
                  - Splits
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                summary: Requests splits for a list of `ids`
                description: >-
                  Gets the entire history of splits for a given list of
                  identifiers. Information returned includes the split factor, a
                  plain text comment regarding the type of split, and the event
                  date.
            /factset-prices/v1/shares:
              get:
                tags:
                  - Gets
                  - Shares
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                summary: Gets shares for a list of `ids` as of given date range.
                description: >-
                  Gets security shares for a list of 'ids' and given date range.
                  Share values returned include security-level and
                  company-level.
              post:
                tags:
                  - Requests
                  - Shares
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                summary: Requests shares for a list of `ids` as of given date range.
                description: >-
                  Gets security shares for a list of 'ids' and given date range.
                  Share values returned include security-level and
                  company-level.
            /factset-prices/v1/market-value:
              get:
                tags:
                  - Gets
                  - The
                  - Security
                  - Level
                  - And
                  - Company
                  - Market
                  - Values
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range
                  - Frequency.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                summary: >-
                  Gets the security level and company level market values for a
                  list of `ids` as of given date range and frequency.
                description: >
                  Gets market capitalization of list of ids for the company
                  level, security level, calendar, frequency, and currency for a
                  specified date range.
              post:
                tags:
                  - Requests
                  - The
                  - Market
                  - Value
                  - For
                  - List
                  - Of
                  - '`ids`'
                  - As
                  - Given
                  - Date
                  - Range.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                summary: >-
                  Requests the market value for a list of `ids` as of given date
                  range.
                description: >-
                  Requests the market value for a list of `ids` as of given date
                  range.
            /factset-prices/v1/high-low:
              get:
                tags:
                  - Gets
                  - The
                  - Price
                  - High
                  - And
                  - Low
                  - Of
                  - Securities
                  - For
                  - List
                  - '`ids`'
                  - As
                  - Given
                  - Date,
                  - Period
                  - Frequency.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                summary: >-
                  Gets the price high and price low of securities for a list of
                  `ids` as of given date, period and frequency.
                description: >
                  For given security(s), gets the high and low prices with the
                  respective dates on which they occurred. This service gives
                  options for fetching the price as of the close or intraday.
              post:
                tags:
                  - Requests
                  - The
                  - Price
                  - High
                  - And
                  - Low
                  - Of
                  - Securities
                  - For
                  - List
                  - '`ids`'
                  - As
                  - Given
                  - Date,
                  - Period
                  - Frequency.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                summary: >-
                  Requests the price high and price low of securities for a list
                  of `ids` as of given date, period and frequency.
                description: >
                  For given security(s), gets the high and low prices with the
                  respective dates on which they occurred. This service gives
                  options for fetching the price as of the close or intraday.
            /factset-prices/v1/database-rollover:
              get:
                summary: Gets the latest relative rollover date for the database.
                description: >
                  Gets zero relative date and last update time for FactSet
                  databases. The dates represent the date that the rollover
                  event happened; the date and time is in **eastern time
                  zone**.  <p>Depending on the ids requested and their
                  respective regions, a requested startDate or endDate used in
                  the various Prices API may reflect different previous close
                  dates. This relative "zero" date, meaning - as of yesterday's
                  close - will vary across global regions. This API is designed
                  to help production systems account for regional rollover dates
                  to know when to trigger their processes for different regions
                  to reflect the latest close. The response gives context for
                  AMERICAS, ASIA PACIFIC, and EUROPE. </p>
                tags:
                  - Gets
                  - The
                  - Latest
                  - Relative
                  - Rollover
                  - Date
                  - For
                  - Database.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
              post:
                summary: Gets the latest relative rollover date for the database.
                description: >
                  Gets zero relative date and last update time for FactSet
                  databases. The dates represent the date that the rollover
                  event happened; the date and time is in **eastern time
                  zone**.  <p>Depending on the ids requested and their
                  respective regions, a requested startDate or endDate used in
                  the various Prices API may reflect different previous close
                  dates. This relative "zero" date, meaning - as of yesterday's
                  close - will vary across global regions. This API is designed
                  to help production systems account for regional rollover dates
                  to know when to trigger their processes for different regions
                  to reflect the latest close. The response gives context for
                  AMERICAS, ASIA PACIFIC, and EUROPE. </p>
                tags:
                  - Gets
                  - The
                  - Latest
                  - Relative
                  - Rollover
                  - Date
                  - For
                  - Database.
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
            /batch/v1/status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                summary: Returns the status for a Batch Request
                description: >-
                  Return the status for the underlying batch request that is
                  specified by the id.
              post:
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                summary: Returns the status for a Batch Request
                description: >-
                  Return the status for the underlying batch request that is
                  specified by the id. 
            /batch/v1/result:
              get:
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                  - Result
                summary: Returns the response for a Batch Request
                description: >-
                  Returns the response data for the underlying batch request
                  that is specified by the id.
              post:
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - Request
                  - Factset
                  - Prices
                  - V1
                  - Fixed
                  - Income
                  - References
                  - Returns
                  - Snapshot
                  - Dividends
                  - Splits
                  - Shares
                  - Market
                  - Value
                  - High
                  - Low
                  - Database
                  - Rollover
                  - Batch
                  - Status
                  - Result
                summary: Returns the response for a Batch Request
                description: >-
                  Return the response data for the underlying batch request that
                  is s
    overlays:
      - type: APIs.io Search
        url: overlays/prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-prices-api
  - name: FactSet Fundamentals API
    description: >-
      Gain access to current, comprehensive, and comparative information on
      securities in worldwide developed and emerging markets. Composed of annual
      and interim/quarterly data and detailed historical financial statement
      content, FactSet Fundamentals…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-fundamentals-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Fundamentals API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/factset-fundamentals-api
          paths:
            /fundamentals:
              get:
                tags:
                  - Returns
                  - Company
                  - Fundamental
                  - Data.
                  - Fundamentals
                summary: Returns Company Fundamental Data.
                description: >
                  Retrieves FactSet Fundamental standardized data for specified
                  securities. Use the ```/metrics``` endpoint to retrieve a full
                  list of valid metrics or data items.



                  The ```/fundamentals``` endpoint currently supports Long
                  Running asynchronous requests up to **20 minutes** via batch
                  parameter. Id limits are increased to 2000 ids per request
                  when using batch capability. This 2000 id limit has been
                  derived based on single metric for one day. This feature is
                  available for all users.       
              post:
                tags:
                  - Returns
                  - Company
                  - Fundamental
                  - Data.
                  - Fundamentals
                summary: Returns Company Fundamental Data.
                description: >
                  Retrieves FactSet Fundamental standardized data for specified
                  securities. Use the ```/metrics``` endpoint to retrieve a full
                  list of valid metrics or data items.



                  The ```/fundamentals``` endpoint currently supports Long
                  Running asynchronous requests up to **20 minutes** via batch
                  parameter. Id limits are increased to 30000 ids per request
                  when using batch capability. This 30000 id limit has been
                  derived based on single metric for one day. This feature is
                  available for all users. 
            /segments:
              get:
                tags:
                  - Returns
                  - Company
                  - Segments
                  - Data.
                  - Fundamentals
                  - Segments
                summary: Returns Company Segments data.
                description: >
                  Retrieves Fundamentals Metrics data for individual companies.


                  The ```/segments``` endpoint currently supports Long Running
                  asynchronous requests up to **20 minutes** via batch
                  parameter. Id limits are increased to 2000 ids per request
                  when using batch capability.This 2000 id limit has been
                  derived based on single metric for one day. This feature is
                  available for all users.
              post:
                tags:
                  - Returns
                  - Company
                  - Segment
                  - Data.
                  - Fundamentals
                  - Segments
                summary: Returns Company Segment Data.
                description: >
                  Retrieves Sales Metrics data for specified companies.


                  The ```/segments``` endpoint currently supports Long Running
                  asynchronous requests up to **20 minutes** via batch
                  parameter. Id limits are increased to 30000 ids per request
                  when using batch capability.This 30000 id limit has been
                  derived based on single metric for one day. This feature is
                  available for all users.
            /metrics:
              get:
                summary: Returns available FactSet Fundamental metrics and ratios.
                tags:
                  - Returns
                  - Available
                  - Fact
                  - Set
                  - Fundamental
                  - Metrics
                  - And
                  - Ratios.
                  - Fundamentals
                  - Segments
                  - Metrics
                description: >
                  Returns list of available FF_* metrics that can be used in the
                  `metrics` parameter of related endpoints. These are related to
                  FactSet Fundamentals standardized data. As Reported will be
                  available in future endpoints. Leave Category and Subcategory
                  blank to request all available items. The Endpoint Data model
                  is optimized for time-series data with periodicity. Some items
                  in this list are non-time series.

                  **For methodology definitions, reference the `OApageID` or
                  `OAurl` response items to launch the available methodology
                  page.**
            /batch-status:
              get:
                tags:
                  - Returns
                  - The
                  - Status
                  - For
                  - Batch
                  - |
                    Request
                  - Fundamentals
                  - Segments
                  - Metrics
                  - Batch
                  - Status
                summary: |
                  Returns the status for a Batch Request
                description: >-
                  Return the status for the underlying batch request that is
                  specified by the id.
            /batch-result:
              get:
                tags:
                  - Returns
                  - The
                  - Response
                  - For
                  - Batch
                  - |
                    Request
                  - Fundamentals
                  - Segments
                  - Metrics
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
        url: overlays/fundamentals-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/fundamentals-openapi-api-evangelist-ratings.yml
    aid: factset:factset-fundamentals-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---