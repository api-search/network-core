---
name: Close
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/close.png
url: https://example.com/apis/close.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Close
apis:
  - name: Adyen Account API
    description: >-
      This API is used for the classic integration. If you are just starting
      your implementation, refer to our new integration guide instead. The
      Account API provides endpoints for managing account-related entities on
      your platform. These related entities include account holders, accounts,
      bank accounts, shareholders, and verification-related documents. The
      management operations include actions such as creation, retrieval,
      updating, and deletion of them.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/Account/6/overview
    baseURL: https://cal-test.adyen.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/Account/6/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Account API
            x-timestamp: '2023-05-30T15:27:20Z'
          x-groups:
            - Account holders
            - Accounts
            - Verification
          tags:
            - name: Account holders
            - name: Verifications
            - name: Accounts
          paths:
            /checkAccountHolder:
              post:
                tags:
                  - Triggers
                  - Verification
                  - Account
                  - Holders
                summary: Trigger verification
                description: >-
                  Triggers the verification of an account holder even if the
                  checks are not yet required for the volume that they are
                  currently processing.
            /closeAccount:
              post:
                tags:
                  - Close
                  - null
                  - Account
                  - Account
                  - Holders
                summary: Close an account
                description: >-
                  Closes an account. If an account is closed, you cannot process
                  transactions, pay out its funds, or reopen it. If payments are
                  made to a closed account, the payments are sent to your liable
                  account.
            /closeAccountHolder:
              post:
                tags:
                  - Close
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                summary: Close an account holder
                description: >-
                  Changes the [status of an account
                  holder](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#account-holder-statuses)
                  to **Closed**. This state is final. If an account holder is
                  closed, you can't process transactions, pay out funds, or
                  reopen it. If payments are made to an account of an account
                  holder with a **Closed**
                  [`status`](https://docs.adyen.com/api-explorer/#/Account/latest/post/getAccountHolder__resParam_verification-accountHolder-checks-status),
                  the payments are sent to your liable account.
            /closeStores:
              post:
                tags:
                  - Close
                  - Stores
                  - Account
                  - Holders
                  - Stores
                summary: Close stores
                description: Closes stores associated with an account holder.
            /createAccount:
              post:
                tags:
                  - Create
                  - null
                  - Account
                  - Account
                  - Holders
                  - Stores
                summary: Create an account
                description: >-
                  Creates an account under an account holder. An account holder
                  can have [multiple
                  accounts](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#create-additional-accounts).
            /createAccountHolder:
              post:
                tags:
                  - Create
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                summary: Create an account holder
                description: >-
                  Creates an account holder that [represents the sub-merchant's
                  entity](https://docs.adyen.com/marketplaces-and-platforms/classic/account-structure#your-platform)
                  in your platform. The details that you need to provide in the
                  request depend on the sub-merchant's legal entity type. For
                  more information, refer to [Account holder and
                  accounts](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#legal-entity-types).
            /deleteBankAccounts:
              post:
                tags:
                  - Delete
                  - Bank
                  - Accounts
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                summary: Delete bank accounts
                description: 'Deletes bank accounts associated with an account holder. '
            /deleteLegalArrangements:
              post:
                tags:
                  - Delete
                  - Legal
                  - Arrangements
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                summary: Delete legal arrangements
                description: >-
                  Deletes legal arrangements and/or legal arrangement entities
                  associated with an account holder.
            /deletePayoutMethods:
              post:
                tags:
                  - Delete
                  - Payouts
                  - Methods
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                summary: Delete payout methods
                description: Deletes payout methods associated with an account holder.
            /deleteShareholders:
              post:
                tags:
                  - Delete
                  - Shareholders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                summary: Delete shareholders
                description: Deletes shareholders associated with an account holder.
            /deleteSignatories:
              post:
                tags:
                  - Delete
                  - Signatories
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                summary: Delete signatories
                description: Deletes signatories associated with an account holder.
            /getAccountHolder:
              post:
                tags:
                  - Get
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                summary: Get an account holder
                description: Returns the details of an account holder.
            /getTaxForm:
              post:
                tags:
                  - Get
                  - Taxes
                  - Forms
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                summary: Get a tax form
                description: >-
                  Generates a tax form for account holders operating in the US.
                  For more information, refer to [Providing tax
                  forms](https://docs.adyen.com/marketplaces-and-platforms/classic/tax-forms).
            /getUploadedDocuments:
              post:
                tags:
                  - Get
                  - Documents
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                summary: Get documents
                description: >
                  Returns documents that were previously uploaded for an account
                  holder. Adyen uses the documents during the [verification
                  process](https://docs.adyen.com/marketplaces-and-platforms/classic/verification-process).
            /suspendAccountHolder:
              post:
                tags:
                  - Suspend
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                summary: Suspend an account holder
                description: >-
                  Changes the [status of an account
                  holder](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#account-holder-statuses)
                  to **Suspended**.
            /unSuspendAccountHolder:
              post:
                tags:
                  - Unsuspend
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                summary: Unsuspend an account holder
                description: >-
                  Changes the [status of an account
                  holder](https://docs.adyen.com/marketplaces-and-platforms/classic/account-holders-and-accounts#account-holder-statuses)
                  from **Suspended** to **Inactive**. 

                  Account holders can have a **Suspended**
                  [`status`](https://docs.adyen.com/api-explorer/#/Account/latest/post/getAccountHolder__resParam_verification-accountHolder-checks-status)
                  if you suspend them through the
                  [`/suspendAccountHolder`](https://docs.adyen.com/api-explorer/#/Account/v5/post/suspendAccountHolder)
                  endpoint or if a verification deadline expires.


                  You can only unsuspend account holders if they do not have
                  verification checks with a **FAILED**
                  [`status`](https://docs.adyen.com/api-explorer/#/Account/latest/post/getAccountHolder__resParam_verification-accountHolder-checks-status).
            /updateAccount:
              post:
                tags:
                  - Update
                  - null
                  - Account
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                summary: Update an account
                description: Updates the description or payout schedule of an account.
            /updateAccountHolder:
              post:
                tags:
                  - Update
                  - null
                  - Account
                  - Holders
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                summary: Update an account holder
                description: >+
                  Updates the `accountHolderDetails` and `processingTier` of an
                  account holder, and adds bank accounts and shareholders.


                  When updating `accountHolderDetails`, parameters that are not
                  included in the request are left unchanged except for the
                  following object:


                  * `metadata`: Updating the metadata replaces the entire
                  object. This means that to update an existing key-value pair,
                  you must provide the changes, as well as other existing
                  key-value pairs.


                  When updating any field in the following objects, you must
                  submit all the fields required for validation:

                   * `address`

                  * `fullPhoneNumber`


                  * `bankAccountDetails.BankAccountDetail`


                  * `businessDetails.shareholders.ShareholderContact`

                   For example, to update the `address.postalCode`, you must also submit the `address.country`, `.city`, `.street`, `.postalCode`, and possibly `.stateOrProvince` so that the address can be validated.

                  To add a bank account or shareholder, provide the bank account
                  or shareholder details without a `bankAccountUUID` or a
                  `shareholderCode`.

            /updateAccountHolderState:
              post:
                tags:
                  - Update
                  - Payouts
                  - Or
                  - Processing
                  - States
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                  - States
                summary: Update payout or processing state
                description: >-
                  Disables or enables the processing or payout state of an
                  account holder.
            /uploadDocument:
              post:
                tags:
                  - Uploads
                  - Document
                  - Account
                  - Holders
                  - Stores
                  - Bank
                  - Accounts
                  - Legal
                  - Arrangements
                  - Payouts
                  - Methods
                  - Shareholders
                  - Signatories
                  - Taxes
                  - Forms
                  - Uploaded
                  - Documents
                  - Suspend
                  - States
                  - Document
                summary: Upload a document
                description: >-
                  Uploads a document for an account holder. Adyen uses the
                  documents during the [verification
                  process](https://docs.adyen.com/marketplaces-and-platfo
    overlays:
      - type: APIs.io Search
        url: overlays/accounts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/accounts-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-account-api
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
  - aid: stripe:stripe-charges-api
    name: Stripe Charges API
    description: >-
      The Charge object represents a single attempt to move money into your
      Stripe account. PaymentIntent confirmation is the most common way to
      create Charges, but transferring money to a different Stripe account
      through Connect also creates Charges. Some legacy payment flows create
      Charges directly, which is not recommended for new integrations.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/api/charges
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/api/charges
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Charges API
          paths:
            /v1/charges:
              get:
                description: >-
                  <p>Returns a list of charges you’ve previously created. The
                  charges are returned in sorted order, with the most recent
                  charges appearing first.</p>
                tags:
                  - V1
                  - Charges
              post:
                description: >-
                  <p>Use the <a href="/docs/api/payment_intents">Payment Intents
                  API</a> to initiate a new payment instead

                  of using this method. Confirmation of the PaymentIntent
                  creates the <code>Charge</code>

                  object used to request payment, so this method is limited to
                  legacy integrations.</p>
                tags:
                  - V1
                  - Charges
            /v1/charges/search:
              get:
                description: >-
                  <p>Search for charges you’ve previously created using Stripe’s
                  <a href="/docs/search#search-query-language">Search Query
                  Language</a>.

                  Don’t use search in read-after-write flows where strict
                  consistency is necessary. Under normal operating

                  conditions, data is searchable in less than a minute.
                  Occasionally, propagation of new or updated data can be up

                  to an hour behind during outages. Search functionality is not
                  available to merchants in India.</p>
                tags:
                  - V1
                  - Charges
                  - Search
            /v1/charges/{charge}:
              get:
                description: >-
                  <p>Retrieves the details of a charge that has previously been
                  created. Supply the unique charge ID that was returned from
                  your previous request, and Stripe will return the
                  corresponding charge information. The same information is
                  returned when creating or refunding the charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
              post:
                description: >-
                  <p>Updates the specified charge by setting the values of the
                  parameters passed. Any parameters not provided will be left
                  unchanged.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
            /v1/charges/{charge}/capture:
              post:
                description: >-
                  <p>Capture the payment of an existing, uncaptured charge that
                  was created with the <code>capture</code> option set to
                  false.</p>


                  <p>Uncaptured payments expire a set number of days after they
                  are created (<a href="/docs/charges/placing-a-hold">7 by
                  default</a>), after which they are marked as refunded and
                  capture attempts will fail.</p>


                  <p>Don’t use this method to capture a PaymentIntent-initiated
                  charge. Use <a
                  href="/docs/api/payment_intents/capture">Capture a
                  PaymentIntent</a>.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
            /v1/charges/{charge}/dispute:
              get:
                description: <p>Retrieve a dispute for a specified charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
              post:
                description: ''
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
            /v1/charges/{charge}/dispute/close:
              post:
                description: ''
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
            /v1/charges/{charge}/refund:
              post:
                description: >-
                  <p>When you create a new refund, you must specify either a
                  Charge or a PaymentIntent object.</p>


                  <p>This action refunds a previously created charge that’s not
                  refunded yet.

                  Funds are refunded to the credit or debit card that’s
                  originally charged.</p>


                  <p>You can optionally refund only part of a charge.

                  You can repeat this until the entire charge is refunded.</p>


                  <p>After you entirely refund a charge, you can’t refund it
                  again.

                  This method raises an error when it’s called on an
                  already-refunded charge,

                  or when you attempt to refund more money than is left on a
                  charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
            /v1/charges/{charge}/refunds:
              get:
                description: >-
                  <p>You can see a list of the refunds belonging to a specific
                  charge. Note that the 10 most recent refunds are always
                  available by default on the charge object. If you need more
                  than those 10, you can use this API method and the
                  <code>limit</code> and <code>starting_after</code> parameters
                  to page through additional refunds.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refunds
              post:
                description: >-
                  <p>When you create a new refund, you must specify a Charge or
                  a PaymentIntent object on which to create it.</p>


                  <p>Creating a new refund will refund a charge that has
                  previously been created but not yet refunded.

                  Funds will be refunded to the credit or debit card that was
                  originally charged.</p>


                  <p>You can optionally refund only part of a charge.

                  You can do so multiple times, until the entire charge has been
                  refunded.</p>


                  <p>Once entirely refunded, a charge can’t be refunded again.

                  This method will raise an error when called on an
                  already-refunded charge,

                  or when trying to refund more money than is left on a
                  charge.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refunds
            /v1/charges/{charge}/refunds/{refund}:
              get:
                description: <p>Retrieves the details of an existing refund.</p>
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refunds
              post:
                description: <p>Update a specified r
                tags:
                  - V1
                  - Charges
                  - Search
                  - Charge
                  - Capture
                  - Dispute
                  - Close
                  - Refund
                  - Refun
    overlays:
      - type: APIs.io Search
        url: overlays/charges-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/charges-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---