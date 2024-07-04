---
name: Basic
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/basic.png
url: https://example.com/apis/basic.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Basic
apis:
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
  - name: FactSet ETF Profile and Prices API
    description: >-
      Access FactSet-collected profile data and pricing for Exchange Traded
      Funds (ETFs).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/etf-profile-and-prices-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/etf-profile-and-prices-api#changelog
      - type: OpenAPI
        data:
          host: api.factset.com
          swagger: '2.0'
          consumes:
            - application/json
          produces:
            - application/json
          paths:
            /factset/etf/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Profile
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                description: >-
                  An ETP can be profiled by defining several common attributes
                  such as issuer, fund description, and benchmark.
                summary: Retrieve basic profile information for a specified ETP.
            /factset/etf/allocation/asset/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Asset
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  asset class. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's asset allocations.
            /factset/etf/allocation/country/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Country
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  country names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's country allocations.
            /factset/etf/allocation/currency/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Currency
                  - Allocations.
                  - By
                  - Symbol
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  currency. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's currency allocations.
            /factset/etf/allocation/economicDevelopment/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Economic
                  - Development
                  - Status.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  List of allocations classified by a holding's economic
                  development status (e.g. developed market, frontier market,
                  emerging market).
                summary: >-
                  List of allocations classified by a holding's economic
                  development status.
            /factset/etf/allocation/exchange/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Exchange
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  exchanges. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's exchange allocations.
            /factset/etf/allocation/industry/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Industry
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  industry. The response will be sorted by weight in descending
                  order.
                summary: This endpoint returns selected ETP's industry allocations.
            /factset/etf/allocation/marketCapitalization/listBySymbol:
              get:
                tags:
                  - List
                  - Of
                  - Allocations
                  - Classified
                  - By
                  - Holding's
                  - Total
                  - Market
                  - Capitalization.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  List of allocations classified by a holding's total market
                  capitalization (e.g. Small Cap, Mid Cap, Large Cap). Response
                  will be sorted by weight in descending order.
                summary: >-
                  List of allocations classified by a holding's total market
                  capitalization.
            /factset/etf/allocation/region/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Region
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  region names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's region allocations.
            /factset/etf/allocation/sector/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Sector
                  - Allocations.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  This endpoint returns selected ETP's allocations grouped by
                  sector names. The response will be sorted by weight in
                  descending order.
                summary: This endpoint returns selected ETP's sector allocations.
            /factset/etf/analytics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Analytics
                  - Datapoints
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet's proprietary analytical datapoints include ETP
                  attributes specific to lending, corporate actions, and
                  benchmarks.
                summary: FactSet proprietary analytics datapoints for ETPs.
            /factset/etf/analytics/holdings/statistics/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Portfolio
                  - Statistics
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates several proprietary portfolio statistics
                  for ETPs including average maturity, credit quality,
                  price/book ratio, price/earnings ratio, and dividend yield.
                summary: FactSet's portfolio statistics for ETPs.
            /factset/etf/analytics/score/getBySymbol:
              get:
                tags:
                  - Fact
                  - Set
                  - Proprietary
                  - Rankings.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  FactSet calculates various proprietary fund rankings including
                  unique scores, fund grades, segment averages, and
                  recommendations.
                summary: FactSet proprietary ETP rankings.
            /factset/etf/analytics/trade/getBySymbol:
              get:
                tags:
                  - Trade
                  - Statistics
                  - For
                  - Specific
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  Various metrics of an ETP's liquidity including creation
                  metrics, premium/discount, spread, and tracking error
                  statistics.
                summary: Trade statistics for specific ETP.
            /factset/etf/characteristics/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Basic
                  - Characteristic
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  An ETP has many unique characteristics specific to its
                  composition that differentiate it from other products. This
                  includes details on leverage, hedging, derivatives, and
                  service providers.
                summary: Retrieve basic characteristic information for a specified ETP.
            /factset/etf/class/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Classification
                  - Specific
                  - To
                  - Asset
                  - Class,
                  - Geography,
                  - Or
                  - Investment
                  - Strategy.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                description: >-
                  ETP classification is divided into three categories: Asset
                  Class, Geography, and Investment Strategy. Asset class is
                  determined based on the various asset types held by the fund,
                  A fund's geography can be classified by region (e.g.
                  Asia-Pac), specific geography (e.g. China) or economic
                  development (e.g. BRIC). An ETP's investment strategy is
                  classified in broad categories (e.g. Large Cap) and more
                  granular categorizations.
                summary: >-
                  Retrieve an ETP's classification specific to asset class,
                  geography, or investment strategy.
            /factset/etf/class/category/broad/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Broad
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                description: List of ETP class broad categories.
                summary: List of ETP class broad categories.
            /factset/etf/class/category/focus/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Focus
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                description: List of ETP class focus categories.
                summary: List of ETP class focus categories.
            /factset/etf/class/category/niche/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Niche
                  - Categories.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                description: List of ETP class niche categories.
                summary: List of ETP class niche categories.
            /factset/etf/class/geography/list:
              get:
                tags:
                  - List
                  - Of
                  - Class
                  - Geographies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: List of ETP class geographies.
                summary: List of ETP class geographies.
            /factset/etf/competitors/listBySymbol:
              get:
                tags:
                  - Fact
                  - Set's
                  - Proprietary
                  - List
                  - Of
                  - Competing
                  - Companies.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  FactSet defines and maintains a proprietary list of competing
                  companies based on a number of attributes specific to a fund.
                summary: FactSet's proprietary list of competing companies.
            /factset/etf/distribution/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Current
                  - Distribution
                  - Details.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                description: >-
                  Retrieve distribution-related details for a specific ETP
                  including dividend and capital gain distribution details.
                summary: Retrieve an ETP's current distribution details.
            /factset/etf/fundFlows/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - An
                  - P's
                  - Cash
                  - Inflow/outflows
                  - For
                  - Various
                  - Time
                  - Periods.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                description: >-
                  Retrieve the amount invested or divested in a specific ETP
                  over various time periods including one-day, one-week,
                  one-month, one-year, and YTD.
                summary: >-
                  Retrieve an ETP's cash inflow/outflows for various time
                  periods.
            /factset/etf/growthOfTenK/listBySymbol:
              get:
                tags:
                  - This
                  - Endpoint
                  - Returns
                  - Selected
                  - P's
                  - Growth
                  - Of
                  - '10'
                  - Calculated
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Growth of 10K (or growth of 10,000) is a commonly used chart
                  that highlights the change in the value of an initial 10,000
                  investment in the ETP during a given period of time. Often,
                  this period of time is either since inception or the
                  calculation between the pre-defined range.
                summary: >-
                  This endpoint returns selected ETP's Growth of 10K calculated
                  values.
            /factset/etf/holdings/listBySymbol:
              get:
                tags:
                  - Holdings
                  - Details
                  - For
                  - An
                  - Individual
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                description: >-
                  Retrieve an ETP's holdings information including security,
                  shares held, and weight.
                summary: Holdings details for an individual ETP.
            /factset/etf/marketAggregates/getBySymbol:
              get:
                tags:
                  - Market
                  - Aggregate
                  - Data
                  - For
                  - Ps.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                description: >-
                  Market Aggregates combines FactSet Estimates, FactSet
                  Fundamentals, and FactSet Prices data to derive ratios and per
                  share values on an aggregate level. The resulting index values
                  can be used to identify market trends and compare a
                  combination of portfolios, benchmarks, and individual
                  securities.
                summary: Market aggregate data for ETPs.
            /factset/etf/premiumDiscount/summary/listBySymbol:
              get:
                tags:
                  - Summary
                  - Of
                  - Premium
                  - Discount
                  - Data.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: Summary of ETP premium discount data.
                summary: Summary of ETP premium discount data.
            /factset/etf/price/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Values.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  Retrieve an ETP's historical NAV and shares outstanding for a
                  specified time range.
                summary: Retrieve historical ETP NAV values.
            /factset/etf/returns/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Total
                  - Return
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  An ETP's total return data can be returned for various time
                  frames including 1-month, 3-month, YTD, 1-year, 3-year, and
                  5-year. Total return calculations include price performance
                  plus reinvested and compounded distributions. Market price is
                  used to calcualte market returns. Portfolio nav is used to
                  calcualte nav returns.
                summary: Retrieve total return data for a specified ETP.
            /factset/etf/strategy/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - Various
                  - Classification
                  - Details
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                description: >-
                  ETP's can be classified in many different ways including
                  investment strategy, security weightings, and fund
                  composition.
                summary: Retrieve various classification details for a specified ETP.
            /factset/etf/strategy/segment/list:
              get:
                tags:
                  - Retrieve
                  - List
                  - Of
                  - Strategy
                  - Segments.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve the various segments assigned to a specific ETP.
                  Segment data is used to group funds for comparison and
                  relative performance analyses.
                summary: Retrieve a list of ETP strategy segments.
            /factset/etf/structure/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Basic
                  - Structure
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                description: >-
                  Retrieve details on a fund's structure including its type,
                  investment style (active/passive), and legal structure.
                summary: Retrieve the basic structure information for a specified ETP.
            /factset/etf/taxesAndFees/us/getBySymbol:
              get:
                tags:
                  - Retrieve
                  - The
                  - Tax
                  - And
                  - Fee
                  - Related
                  - Information
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                description: >-
                  Retrieve various fee and tax related details on a specified
                  ETP including expense ratio and tax treatment for dividends
                  and capital gains.
                summary: >-
                  Retrieve the tax and fee related information for a specified
                  ETP.
            /factset/etf/timeSeries/listBySymbol:
              get:
                tags:
                  - Retrieve
                  - Historical
                  - Data
                  - For
                  - Specified
                  - P.
                  - By
                  - Symbol
                  - Development
                  - List
                  - Capitalization
                  - Factset
                  - Etf
                  - Class
                  - Category
                  - Broad
                  - Focus
                  - Niche
                  - Geography
                  - Flows
                  - Get
                  - Of
                  - Ten
                  - Aggregates
                  - Discount
                  - Summary
                  - Strategy
                  - Segment
                  - And
                  - Fees
                  - Us
                  - Series
                description: >-
                  Retrieve the historical NAV data and the respective fund flows
                  and shares outstanding for a specified fund and time period.
                  Please refer currency.fund in /factset/etf/getBySymbol for
                  currency value.
                summary: Retrieve historical NAV data for a specified ETP.
          info:
            title: Prime Developer Trial
          x-interface-version: 1
          x-documenter-version: 5.38.1
          x-api-version: 2.9.1
          tags:
            - name: factset
              description: factset endpoints
          responses:
            ErrorResponse:
              description: Generic error response for all errors (400 ... 599 error codes)
              schema:
                type: object
                properties:
                  meta:
                    $ref: '#/definitions/ErrorMetaObject'
                  errors:
                    $ref: '#/definitions/ErrorObject'
          definitions:
            ErrorMetaObject:
              type: object
              properties:
                status:
                  $ref: '#/definitions/StatusObject'
            ErrorObject:
              type: array
              description: >-
                The errors member contains additional information about a failed
                request.
              items:
                type: object
                properties:
                  details:
                    type: string
                    description: >-
                      A human-readable, unstructured explanation specific to
                      this occurrence of the failure.
                  encryptedDetails:
                    type: string
                    description: >-
                      Base64-encoded, internal details about the error, in
                      addition to "details".
                  type:
                    type: number
                    format: int32
                    description: Internal error type of the Foundation API protocol.
                  attribute:
                    type: array
                    description: >-
                      For a validation error, a reference to the request
                      parameter that failed validation; otherwise, an empty
                      array.
                    items:
                      type: object
                      properties:
                        name:
                          type: string
                          description: Element of the path denoting the request parameter.
                        index:
                          type: number
                          format: int32
                          description: >-
                            If the attribute "name" designates an array, index
                            of the array element; otherwise the special value
                            -1.
                      x-property-sort:
                        - name
                        - index
                x-property-sort:
                  - detail
                  - encryptedDetails
                  - type
                  - attribute
            AttributesMember:
              type: array
              description: >-
                Limit the attributes returned in the response to the specified
                set.
              items:
                type: string
                maxLength: 100
                exclusiveMaximum: false
              maxItems: 50
              uniqueItems: true
            LanguageMember:
              type: string
              format: isoLanguage
              description: ISO 639-1 code of the language.
              maxLength: 2
              minLength: 2
              exclusiveMinimum: false
              exclusiveMaximum: false
            StatusObject:
              type: object
              properties:
                code:
                  type: number
                  format: int32
                  description: >-
                    The HTTP status code of the response, mirroring the code
                    from the Status-Line of the HTTP response message (see
                    [RFC2616] section 6.1).
              description: The status member contains the status code of the response.
              required:
                - code
            CursorBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the cursor-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of `total` is estimated.
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - total
                - isEstimatedTotal
                - next
                - previous
              x-property-sort:
                - total
                - isEstimatedTotal
                - next
                - previous
            CursorBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the cursor-based pagination strategy;
                a total element count is not supported.
              properties:
                next:
                  type: string
                  description: >-
                    The next cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination, otherwise `null`.
                previous:
                  type: string
                  description: >-
                    The previous cursor position to use in the parameter
                    `pagination.cursor` for an endpoint that supports
                    cursor-based pagination. If a previous cursor position is
                    not supported or available, `previous` is `null`.
              required:
                - next
                - previous
              x-property-sort:
                - next
                - previous
            OffsetBasedPaginationOutputObject:
              type: object
              description: Pagination attributes for the offset-based pagination strategy.
              properties:
                total:
                  type: number
                  format: int32
                  description: Total number of entries in the result set.
                isEstimatedTotal:
                  type: boolean
                  description: Flag indicating that the value of "total" is estimated.
              required:
                - total
                - isEstimatedTotal
              x-property-sort:
                - total
                - isEstimatedTotal
            OffsetBasedPaginationOutputObjectWithoutTotal:
              type: object
              description: >-
                Pagination attributes for the offset-based pagination strategy;
                a total element count is not supported.
              properties:
                hasNext:
                  type: boolean
                  description: >-
                    Flag indicating that a subsequent request with the same
                    parameters, except that the parameter `pagination.offset` is
                    incremented by `pagination.limit`, would yield additional
                    results.
              required:
                - hasNext
              x-property-sort:
                - hasNext
            PartialOutputObject:
              type: object
              properties:
                isPartial:
                  type: boolean
                  description: >-
                    Flag indicating that the response is a possibly incomplete
                    array or an object containing a possibly incomplete array,
                    due to hitting a processing time limit. If `true`, some
                    matching results might be missing from the array, or
                    elements for matching results might be incorrectly included
                    (for example, when priority sorting would have removed the
                    element). Depending on the use case, such a response may be
                    unsuitable.
              description: >-
                Object denoting that the endpoint response is possibly
                incomplete.
              required:
                - isPartial
              x-property-sort:
                - isPartial
          basePath: /wealth/v1
          schemes:
            - https
          securityDefinitions:
            Basic:
              type: nu
    overlays:
      - type: APIs.io Search
        url: overlays/etf-profile-and-prices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/etf-profile-and-prices-openapi-api-evangelist-ratings.yml
    aid: factset:factset-etf-profile-and-prices-api
  - name: FactSet Options API
    description: >-
      The FactSet Options API provides Chains and related pricing data such as
      mid bid-ask price, reference data (e.g., strike price), and risk measures
      (e.g., Greeks and implied volatility).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-options-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-options-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Options API
          tags:
            - name: Option Chains & Screening
              description: >-
                Generate a list or universe of options ids based on underlying
                securities or other conditions
            - name: Snapshot
              description: >-
                A generic profile for a list of option securities as of a
                specific date
            - name: Reference
              description: Option Reference Information and Dates
            - name: Prices & Volume
              description: >-
                Option Prices & Volume information for a requested time-range
                for the option security or aggregated for all options associated
                to the underlying security
            - name: Risk Measures
              description: >-
                Option Risk measures such as Greeks, Implied Volatilities, and
                Calculators
          paths:
            /factset-options/v1/chains:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Underlying
                  - Option
                  - Identifiers
                  - For
                  - Specified
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                summary: >-
                  Returns all the underlying option identifiers for the
                  specified underlying Security identifier
                description: >
                  Returns all the underlying option identifiers for the
                  underlying security identifier. Specify the date and or
                  exhcange for the list of options associated to the id. 

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/option-screening:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Option
                  - Identifiers
                  - Based
                  - 'On'
                  - Conditions
                  - Provided
                  - As
                  - Input
                  - In
                  - Request
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                summary: >-
                  Returns all the option identifiers based on the conditions
                  provided as input in the request
                description: >
                  Returns all the option identifiers based on the conditions
                  provided as input in the request. Conditions are as follows
                  and will follow "AND" logic if more than one condition is
                  applied and allows up to **three conditions** using AND
                  Logic.If a condition is used the accompanying value MUST be
                  used - 

                  |conditions|description|

                  |||

                  |P_OPT_UNDERLYING_SECURITY_E|Underlying Security Equal To|

                  |P_OPT_STRIKE_PRICE_E|Strike Price Equal To|

                  |P_OPT_EXP_DATEN_E|Expiration Date (YYYYMMDD) Equal To|

                  |P_OPT_VOLUME_G|Volume Greater Than|

                  |P_OPT_VOLUME_GE|Volume Greater Than or Equal To|

                  |P_OPT_VOLUME_L|Volume Less Than|

                  |P_OPT_VOLUME_LE|Volume Less Than or Equal To|

                  |P_OPT_VOLUME_E|Volume Equal To|

                  |P_OPT_OPTION_TYPE_E|Option Type (1= Equity, 2=Index)|

                  |P_OPT_CALL_OR_PUT_E|Call or Put (0=Call, 1=Put)|

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/snapshot:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Profile
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - As
                  - Specific
                  - Date
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                summary: >-
                  Returns all the profile information for the list of
                  identifiers as of a specific date
                description: >
                  Returns all the profile information for the list of
                  identifiers for a specific date. The data includes - 

                  * Expiration Date

                  * Greek - Delta

                  * Implied Volatility

                  * Price 

                  * Style

                  * Type

                  * Underlying Security

                  * Underlying Security Price

                  * Open Interest

                  * Name

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/references:
              post:
                tags:
                  - Returns
                  - Basic
                  - Reference
                  - Details
                  - For
                  - The
                  - Options
                  - Such
                  - As
                  - Currency,
                  - Exchange,
                  - Symbols,
                  - Flags
                  - And
                  - More
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                summary: >-
                  Returns basic reference details for the options such as
                  currency, exchange, symbols, flags and more
                description: >
                  Returns basic reference details for the options. Data items
                  include - 

                  * Name

                  * Exchange

                  * Call or Put Flag

                  * Call or Put Pair Symbol

                  * Other symbols such as OPRA17 and OCC21

                  * Currency

                  * Underlying Security Symbols

                  * Expiration Month, Dates, and Frequency


                  *For details or definitions of all available response fields
                  visit the associated schema.*

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/dates:
              post:
                tags:
                  - Returns
                  - Option
                  - Security
                  - Dates
                  - Such
                  - As
                  - Expiration
                  - And
                  - Trade.
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                summary: Returns option security dates such as expiration and trade.
                description: >
                  Returns all relevant dates such as  for the specified Option
                  identifier. Data Items include - 

                  * Expiration Date

                  * First Dates for Ask, Bid, Settlement, and Trade

                  * Last Dates for Ask, Bid, Settlement, and Trade

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/prices:
              post:
                tags:
                  - Returns
                  - The
                  - Pricing
                  - Related
                  - Information
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                summary: >-
                  Returns the pricing related information for the specified
                  option identifier
                description: >
                  Returns the pricing related information for the specified
                  option identifier. Items include - 

                  * Ask

                  * Bid

                  * Mid

                  * Mid Bid Ask

                  * Settlement

                  * Last Price Type (Settlement or MidBidAsk)

                  * Last Price

                  * Strike Price

                  * Underlying Security Price

                  * 52 Week High/Low

                  * Open, High, Low for day. Note securities must be trading for
                  day requested.

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/underlying-volume:
              post:
                tags:
                  - Returns
                  - The
                  - Aggregate
                  - Volume
                  - And
                  - Open
                  - Interest
                  - For
                  - List
                  - Of
                  - Options
                  - Under
                  - Specified
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                summary: >-
                  Returns the aggregate volume and open interest for the list of
                  the options under the specified security identifier
                description: >
                  Return the Volume and Open Interest details for list of the
                  options for the specified underlying security identifier. The
                  data is aggregated for all options contracts associated to the
                  underlying id, or specified in the request only the contracts
                  listed on a specific exchange. Data Includes - 

                  * Put Call Ratio 

                  * Total Put Volume & Open Interest

                  * Total Call Volume & Open Interest

                  * Total Put & Call Volume & Open Interest

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/volume:
              post:
                tags:
                  - Returns
                  - The
                  - Volume
                  - Details
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                summary: Returns the volume details for the specified option identifier
                description: >
                  Returns the volume details for the specified option identifier
                  for a specified exchange. Data items include - 

                  * Open Interest

                  * Volume

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/greeks:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Greeks
                  - Details
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                summary: >-
                  Returns all the Greeks details for the specified option
                  identifier
                description: >
                  Returns all the greeks details for the specified option
                  identifier. Greeks provide quantifiable factors for measuring
                  the option's price sensativity. Greeks include -


                  |Greek|Description|

                  |||

                  |Delta| The ratio comparing the change in the price of the
                  underlying asset to the corresponding change in the price of a
                  derivative. Sometimes referred to as the "hedge ratio". For
                  example, with respect to call options, a delta of 0.7 means
                  that for every $1 the underlying stock increases, the call
                  option will increase by $0.70. Put option deltas, on the other
                  hand, will be negative, because as the underlying security
                  increases, the value of the option will decrease. So a put
                  option with a delta of -0.7 will decrease by $0.70 for every
                  $1 the underlying increases in price. As an in-the-money call
                  option nears expiration, it will approach a delta of 1.00, and
                  as an in-the-money put option nears expiration, it will
                  approach a delta of -1.00.|

                  |Gamma| The rate of change for delta with respect to the
                  underlying asset's price. Mathematically, gamma is the first
                  derivative of delta and is used when trying to gauge the price
                  of an option relative to the amount it is in or out of the
                  money. When the option being measured is deep in or out of the
                  money, gamma is small. When the option is near the money,
                  gamma is largest.|

                  |Rho|The rate at which the price of a derivative changes
                  relative to a change in the risk-free rate of interest. Rho
                  measures the sensitivity of an option or options portfolio to
                  a change in interest rate.|

                  |Theta|A measure of the rate of decline in the value of an
                  option due to the passage of time. Theta can also be referred
                  to as the time decay on the value of an option. If everything
                  is held constant, then the option will lose value as time
                  moves closer to the maturity of the option. For example, if
                  the strike price of an option is $1,150 and theta is 53.80,
                  then in theory the value of the option will drop $53.80 per
                  day. The measure of theta quantifies the risk that time
                  imposes on options as options are only exercisable for a
                  certain period of time.|

                  |Vega|The amount that the price of an option changes compared
                  to a 1% change in volatility. Vega changes when there are
                  large price movements in the underlying asset and vega falls
                  as the option gets closer to maturity. Vega can change even if
                  there is no change in the price of the underlying asset, this
                  would happen if there is a change in expected volatility. For
                  example, if the vega of an option is -96.94 and if implied
                  volatility were to rise by 1% then the option value would fall
                  by $96.94.|


                  Note
                    * Each step in the binomial model represents a change in time, therefore, point estimates of the Greeks can be calculated for American options. The following can be used to calculate the Greeks for the Binomial Option Pricing Model (BOPM) pricing model, using the notation fstep,node so f1,1 represents the option price at the first step, top node (nodes are counted at each step starting with 0 at the bottom. See [Constructing the Tree](https://my.apps.factset.com/oa/pages/17735#tree) for more information).
                    
                  For more detials on calculation methodologies, visit [OA
                  14933](https://my.apps.factset.com/oa/pages/14933). 

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/implied-volatility:
              post:
                tags:
                  - Returns
                  - The
                  - Implied
                  - Volatility
                  - Information
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                  - Implied
                  - Volatility
                summary: >-
                  Returns the implied volatility information for the specified
                  option identifier
                description: >
                  Returns the Implied Volatility for the specified option across
                  European and American contracts. For more details regarding
                  Implied Volatility calculations visit - [OA
                  14932](https://my.apps.factset.com/oa/pages/14932)


                  *Currently the following exchanges are not supported for API
                  use cases - CME, CMEE, CBT, CBTE, NYM, NYME*
            /factset-options/v1/atm-implied-volatility:
              post:
                tags:
                  - Returns
                  - The
                  - At-the-money
                  - M)
                  - Implied
                  - Volatility
                  - Details
                  - For
                  - Specified
                  - Underlying
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                  - Implied
                  - Volatility
                  - Atm
                summary: >-
                  Returns the at-the-money (ATM) implied volatility details for
                  the specified underlying security identifier
                description: >
                  Returns weighted average of the implied volatilities from the
                  options listed for a specified security identifier. 


                  There are three different methods available for calculating
                  at-the-money implied volatility (ATM IV), which gives a
                  weighted average of the implied volatilities from the options
                  listed on a given stock. They are ATM IV (Filtered), ATM IV
                  (Filtered with Smoothing), and ATM IV (Market). Each of these
                  ATM IV calculations is available for just the calls on a given
                  stock, just the puts, or the composite of both the calls and
                  puts.

                  This at-the-money implied volatility market can calculated for
                  different periods -

                  * One Month

                  * Two Months

                  * Three Months

                  * Four Months

                  * Five Months

                  * Six Months


                  *For more details regarding ATM Volatility calculations, visit
                  [OA 16276](https://my.apps.factset.com/oa/pages/16276)*

                    *Currently only OPRA Exchange traded op
    overlays:
      - type: APIs.io Search
        url: overlays/options-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/options-openapi-api-evangelist-ratings.yml
    aid: factset:factset-options-api
  - name: FactSet Real-Time Price Alerting API
    description: >-
      Basic Price Alerting deals with generation of alerts based on current
      price data. Users can define an upper or lower limit and choose on which
      price type those limit conditions apply.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-price-alerting-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Price Alerting API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /alerting/prices/basic/alert/get:
              get:
                tags:
                  - Details
                  - Of
                  - An
                  - Alert.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                description: >-
                  Details of an alert. The details include the trigger
                  definition at the time of alert creation.
                summary: Details of an alert.
            /alerting/prices/basic/alert/list:
              get:
                tags:
                  - List
                  - Of
                  - Alerts.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                  - List
                description: List of alerts in descending order of creation.
                summary: List of alerts.
            /alerting/prices/basic/trigger/get:
              get:
                tags:
                  - Details
                  - Of
                  - Trigger.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                  - List
                  - Trigger
                description: Details of a trigger.
                summary: Details of a trigger.
            /alerting/prices/basic/trigger/list:
              post:
                tags:
                  - List
                  - Of
                  - Triggers.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                  - List
                  - Trigger
                description: >-
                  Returns a list of triggers sorted in descending order of
                  creation.
                summary: List of triggers.
          tags:
            - name: alerting
              description: alerting endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-price-alerting-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-price-alerting-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-price-alerting-api
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
  - name: OpenAI Models API
    description: >-
      List and describe the various models available in the API. You can refer
      to the Models documentation to understand what models are available and
      the differences between them.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/api-reference/models
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' models'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Models
              description: List and describe the various models available in the API.
          paths:
            /models:
              get:
                tags:
                  - Lists
                  - The
                  - Currently
                  - Available
                  - Models,
                  - And
                  - Provides
                  - Basic
                  - Information
                  - About
                  - Each
                  - One
                  - Such
                  - As
                  - Owner
                  - Availability.
                  - Models
                summary: >-
                  Lists the currently available models, and provides basic
                  information about each one such as the owner and availability.
            /models/{model}:
              get:
                tags:
                  - Retrieves
                  - Model
                  - Instance,
                  - Providing
                  - Basic
                  - Information
                  - About
                  - The
                  - Such
                  - As
                  - Owner
                  - And
                  - Permissioning.
                  - Models
                  - Model
                summary: >-
                  Retrieves a model instance, providing basic information about
                  the model such as the owner and permissioning.
              delete:
                tags:
                  - Delete
                  - Fine-tuned
                  - Model.
                  - You
                  - Must
                  - Have
                  - The
                  - Owner
                  - Role
                  - In
                  - Your
                  - Organization
                  - To
                  - Models
                  - Model
                summary: >-
                  Delete a fine-tuned model. You must have the Owner role in
                  your organization to delete a model.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/models-openapi-search.yml
      - type: APIs.io Search
        url: overlays/models-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/models-openapi-api-evangelist-ratings.yml
    aid: openai:openai-models-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---