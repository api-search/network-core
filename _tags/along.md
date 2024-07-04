---
name: Along
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/along.png
url: https://example.com/apis/along.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Along
apis:
  - name: FactSet IRN Contacts API
    description: >-
      Contacts API allows users to create, update and delete Contacts as well as
      configure settings in the Internal Research Notes Contacts application.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/irn-contacts-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/irn-contacts-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/irn-contacts-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/irn-contacts-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/irn-contacts-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/irn-contacts-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: IRN API v1
          paths:
            /v1/contact-relationships:
              get:
                tags:
                  - Get
                  - All
                  - The
                  - Relationships
                  - Where
                  - Given
                  - Symbol
                  - Or
                  - Contact
                  - Identifier
                  - Has
                  - Been
                  - Tagged
                  - In
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                summary: >-
                  Get all the relationships where the given symbol or contact
                  identifier has been tagged in a relationship
              post:
                tags:
                  - Create
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                summary: Create a contact relationship
            /v1/contact-relationships/{contactRelationshipId}:
              get:
                tags:
                  - Get
                  - Details
                  - 'On'
                  - Specific
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                summary: Get details on a specific contact relationship
              patch:
                tags:
                  - Update
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                summary: Update a contact relationship
              delete:
                tags:
                  - Delete
                  - Contact
                  - Relationship
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                summary: Delete a contact relationship
            /v1/contacts:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Contacts
                  - In
                  - Your
                  - Group
                  - Along
                  - With
                  - Some
                  - Their
                  - Standard
                  - Field
                  - Data
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: >-
                  Get list of all contacts in your group along with some of
                  their standard field data
              post:
                tags:
                  - Create
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: Create a contact
            /v1/contacts/{contactId}:
              get:
                tags:
                  - Get
                  - All
                  - Custom
                  - Field
                  - And
                  - Standard
                  - Details
                  - 'On'
                  - Specific
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: >-
                  Get all custom field and standard field details on a specific
                  contact
              patch:
                tags:
                  - Edit
                  - Contact’s
                  - Standard
                  - Field
                  - And
                  - Custom
                  - Data
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: Edit a contact’s standard field and custom field data
              delete:
                tags:
                  - Delete
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                summary: Delete a contact
            /v1/contacts/{contactId}/about:
              get:
                tags:
                  - Get
                  - The
                  - About
                  - Field
                  - Content
                  - For
                  - Specific
                  - Contact
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                summary: Get the About field content for a specific contact
            /v1/contacts/{contactId}/events:
              get:
                tags:
                  - Get
                  - Contact’s
                  - Audit
                  - History
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                  - Events
                summary: Get a contact’s audit history
            /v1/contacts/{contactId}/records:
              get:
                tags:
                  - Get
                  - All
                  - Notes
                  - And
                  - Meetings
                  - Where
                  - Specific
                  - Contact
                  - Was
                  - Tagged
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                  - Events
                  - Records
                summary: Get all notes and meetings where a specific contact was tagged
            /v1/contacts/{contactId}/relationships:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Contact’s
                  - Relationships
                  - V1
                  - Contact
                  - Relationships
                  - Relationship
                  - Id
                  - Contacts
                  - About
                  - Events
                  - Records
                summary: Returns a list of a contact’s relationships
          tags:
            - name: Contacts
            - name: Cont
    overlays:
      - type: APIs.io Search
        url: overlays/irn-contacts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/irn-contacts-openapi-api-evangelist-ratings.yml
    aid: factset:factset-irn-contacts-api
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
  - name: FactSet IRN Custom Symbols API
    description: >-
      This API allows users to create, read, edit and delete IRN custom symbols
      as well as configure settings in the Internal Research Notes Symbol
      Manager application.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/irn-custom-symbols-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/irn-custom-symbols-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/irn-custom-symbols-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/irn-custom-symbols-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/irn-custom-symbols-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/irn-custom-symbols-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: IRN API v1
          paths:
            /v1/custom-symbols:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - All
                  - Custom
                  - Symbols
                  - In
                  - Your
                  - Group
                  - Along
                  - With
                  - Some
                  - Their
                  - Standard
                  - Field
                  - And
                  - Fields
                  - Data
                  - V1
                  - Custom
                  - Symbols
                summary: >-
                  Get list of all custom symbols in your group along with some
                  of their standard field and custom fields data
              post:
                tags:
                  - Create
                  - Custom
                  - Symbol
                  - V1
                  - Custom
                  - Symbols
                summary: Create a custom symbol
            /v1/custom-symbols/{customSymbolId}:
              get:
                tags:
                  - Get
                  - All
                  - Custom
                  - Field
                  - And
                  - Standard
                  - Details
                  - 'On'
                  - Specific
                  - Symbol
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                summary: >-
                  Get all custom field and standard field details on a specific
                  custom symbol
              patch:
                tags:
                  - Edit
                  - Custom
                  - Symbol’s
                  - Standard
                  - Field
                  - And
                  - Data
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                summary: Edit a custom symbol’s standard field and custom field data
              delete:
                tags:
                  - Delete
                  - Custom
                  - Symbol
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                summary: Delete a custom symbol
            /v1/custom-symbols/{customSymbolId}/records:
              get:
                tags:
                  - Get
                  - All
                  - Notes
                  - And
                  - Meetings
                  - Where
                  - Specific
                  - Custom
                  - Symbol
                  - Was
                  - Tagged
                  - As
                  - Primary
                  - Or
                  - Related
                  - Identifier
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                summary: >-
                  Get all notes and meetings where a specific customSymbol was
                  tagged as primary or related identifier
            /v1/custom-symbols/standard-symbol-metadata/{standardSymbol}:
              get:
                tags:
                  - Get
                  - All
                  - Custom
                  - Field
                  - And
                  - Standard
                  - Details
                  - 'On'
                  - Specific
                  - Symbol
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                summary: >-
                  Get all custom field and standard field details on a specific
                  standard symbol
            /v1/symbol-relationships/{symbolId}/relationships:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Symbol’s
                  - Relationships
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                summary: Returns a list of a symbol’s relationships
            /v1/symbol-relationships/{symbolRelationshipId}:
              get:
                tags:
                  - Get
                  - Details
                  - 'On'
                  - Specific
                  - Symbol
                  - Relationship
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                summary: Get details on a specific symbol relationship
              delete:
                tags:
                  - Delete
                  - Symbol
                  - Relationship
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                summary: Delete a symbol relationship
            /v1/custom-symbols/{customSymbolId}/link-standard-symbol:
              post:
                tags:
                  - Link
                  - Custom
                  - Symbol
                  - To
                  - Standard
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                  - Link
                  - Standard
                summary: Link custom symbol to standard symbol
            /v1/custom-symbols/standard-symbol-metadata:
              post:
                tags:
                  - Create
                  - Standard
                  - Symbol
                  - Metadata
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                  - Link
                  - Standard
                  - Metadata
                summary: Create standard symbol metadata
            /v1/symbol-relationships:
              post:
                tags:
                  - Create
                  - Symbol
                  - Relationship
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                  - Link
                  - Standard
                  - Metadata
                summary: Create a symbol relationship
            /v1/symbol-relationships/{symbol}:
              put:
                tags:
                  - Edit
                  - Symbol
                  - Relationship
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                  - Link
                  - Standard
                  - Metadata
                summary: Edit a symbol relationship
            /v1/custom-symbols/standard-symbol-metadata/{standardSymbolId}:
              patch:
                tags:
                  - Edit
                  - Standard
                  - Symbol’s
                  - Field
                  - And
                  - Custom
                  - Data
                  - V1
                  - Custom
                  - Symbols
                  - Symbol
                  - Id
                  - Records
                  - Relationships
                  - Relationship
                  - Link
                  - Standard
                  - Metadata
                summary: Edit a standard symbol’s standard field and custom field data
          tags:
            - name: CustomSymbols
            - name: CustomSymbols - Relationships
            - name: nu
    overlays:
      - type: APIs.io Search
        url: overlays/irn-custom-symbols-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/irn-custom-symbols-openapi-api-evangelist-ratings.yml
    aid: factset:factset-irn-custom-symbols-api
  - name: FactSet Content Feeds Data Dictionary
    description: >-
      Browse data items and definitions available through FactSet's off platform
      product offerings.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/content-feeds-data-dictionary
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: CTS Data Dictionary API
          paths:
            /navigator/products:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Products
                  - For
                  - Navigator.
                  - Navigator
                  - Products
                summary: Get the list of products for Navigator.
            /navigator/data_items/{Product_id}:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Data
                  - Items
                  - Associated
                  - With
                  - Product
                  - For
                  - Navigator.
                  - Navigator
                  - Products
                  - Product_id
                summary: >-
                  Get the list of data items associated with a product for
                  Navigator.
            /navigator/sources/{DataItem_id}:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Sources
                  - Where
                  - The
                  - Specified
                  - Data
                  - Item
                  - Can
                  - Be
                  - Found,
                  - For
                  - Each
                  - Delivery
                  - Method,
                  - Filtered
                  - To
                  - Appearances
                  - Given
                  - Within
                  - Product.
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                summary: >-
                  Get a list of sources where the specified data item can be
                  found, for each delivery method, filtered to the appearances
                  of the given data item within the specified product.
            /navigator/sources:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Sources
                  - By
                  - Delivery
                  - Method
                  - For
                  - The
                  - Given
                  - Product_id
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                summary: >-
                  Get a list of sources by delivery method for the given
                  product_id
            /navigator/table_fields/{Table_id}:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Fields
                  - Associated
                  - With
                  - Table
                  - For
                  - Navigator,
                  - And
                  - Code
                  - Information
                  - Specified
                  - Data
                  - Item,
                  - If
                  - Applicable.
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                  - Table_id
                summary: >-
                  Get the list of fields associated with a table for Navigator,
                  and the code information for the specified data item, if
                  applicable.
            /navigator/basic_search:
              post:
                tags:
                  - Returns
                  - The
                  - Data
                  - Items
                  - (along
                  - With
                  - Products
                  - They
                  - Belong
                  - To)
                  - That
                  - Contain
                  - At
                  - Least
                  - One
                  - Of
                  - Search
                  - Terms
                  - As
                  - Substring
                  - Either
                  - Their
                  - Na
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                  - Table_id
                  - Basic_search
                summary: >-
                  Returns the data items (along with the products they belong
                  to) that contain at least one of the search terms as a
                  substring of either their
    overlays:
      - type: APIs.io Search
        url: overlays/content-feeds-data-dictionary-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/content-feeds-data-dictionary-openapi-api-evangelist-ratings.yml
    aid: factset:factset-content-feeds-data-dictionary
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---