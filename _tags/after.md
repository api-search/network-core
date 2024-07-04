---
name: After
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/after.png
url: https://example.com/apis/after.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - After
apis:
  - name: FactSet Intraday Tick History API
    description: >-
      FactSet’s Tick History provides cost-effective access to consolidated
      real-time and delayed global exchange data. Proprietary technology
      normalizes data from over 200 global exchanges and across 19 tick history
      fields. Asset types integrated…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/factset-intraday-tick-history-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-intraday-tick-history-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-intraday-tick-history-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-intraday-tick-history-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-intraday-tick-history-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-intraday-tick-history-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Tick History
            license:
              name: Apache 3.0
              url: http://www.apache.org/licenses/LICENSE-2.0.html
          externalDocs:
            description: Data Service Manual
            url: >-
              https://www.factset.com/hubfs/Website_Downloads/Exchange%20DataFeed/data%20service%20manual%202.0b.pdf
          paths:
            /TickHistory/history:
              get:
                tags:
                  - Tick
                  - History
                  - Service
                  - Returns
                  - Trade
                  - Data
                  - And
                  - Associated
                  - Quotes
                  - For
                  - Client
                  - Specified
                  - Interval
                  - Time
                  - Period
                  - Tick
                  - History
                summary: >-
                  Tick History service returns trade data and associated quotes
                  for a client specified interval and time period
                description: >-
                  When using an HTTP GET request, the seach criteria is sent via
                  the query string in the URL. Please make sure that all
                  requests contain a date within the past trailing year. Fields
                  are added using ampersands, with enumerations seperated by
                  commas. <p>**Try it Out** - references a sandbox environment
                  to simulate live reponses. Available `id` is limited to
                  BABA-USA,WALMEX-MX,7203-TKS,VOD-LON,NPN-JSE,MABAX,NZF,SPY-USA,AGG-USA,GLD-USA,AOR-USA,MNA-USA,UUP-USA,SP50-SPX,ESX-STX,XAO-ASX,WD-MSX,NG00-USA,GC00-USA,CC00-USA,C00-USA,FC00-USA,ER00-USA,EURUSD-FX1,USDMXN-FX1,AUDJPY-FX1,EURCZK-FX1,USDILS-FX1,USDZAR-FX1,US10YY-TU1,FDS#190621C00145000-USA,FDS#190621P00145000-USA.
                  Current day data is not available.</p>
            /TickHistory/firsttrade:
              get:
                tags:
                  - Request
                  - Returns
                  - Data
                  - For
                  - The
                  - First
                  - Trade
                  - (official
                  - And
                  - Unofficial)
                  - After
                  - Specified
                  - Time
                  - Tick
                  - History
                  - Firsttrade
                summary: >-
                  Request returns data for the first trade (official and
                  unofficial) after the specified time
                description: ''
            /TickHistory/lasttrade:
              get:
                tags:
                  - Request
                  - Returns
                  - Data
                  - For
                  - The
                  - Last
                  - Trade
                  - And
                  - Associated
                  - Quotes
                  - Before
                  - Specified
                  - Time
                  - Tick
                  - History
                  - Firsttrade
                  - Lasttrade
                summary: >-
                  Request returns data for the last trade and associated quotes
                  before the specified time
                description: ''
            /TickHistory/qat:
              get:
                tags:
                  - Request
                  - Returns
                  - Quote
                  - At
                  - The
                  - Specified
                  - Time
                  - Tick
                  - History
                  - Firsttrade
                  - Lasttrade
                  - Qat
                summary: Request returns a quote at the specified time
                description: ''
            /TickHistory/tradesattime:
              get:
                tags:
                  - Request
                  - Returns
                  - The
                  - Before
                  - And
                  - After
                  - Trade
                  - Data
                  - Along
                  - With
                  - Associated
                  - Quotes
                  - For
                  - Specified
                  - Time
                  - Tick
                  - History
                  - Firsttrade
                  - Lasttrade
                  - Qat
                  - Tradesattime
                summary: >-
                  Request returns the before and after trade data along with the
                  associated quotes for the specified time
                description: nu
    overlays:
      - type: APIs.io Search
        url: overlays/intraday-tick-history-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/intraday-tick-history-openapi-api-evangelist-ratings.yml
    aid: factset:factset-intraday-tick-history-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---