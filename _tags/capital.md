---
name: Capital
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/capital.png
url: https://example.com/apis/capital.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Capital
apis:
  - name: Adyen Transfers API
    description: >-
      This API provides endpoints that you can use to transfer funds, whether
      when [paying out to a transfer
      instrument](https://docs.adyen.com/marketplaces-and-platforms/payout-to-users/on-demand-payouts),
      [sending funds to third
      parties](https://docs.adyen.com/marketplaces-and-platforms/business-accounts/send-receive-funds)
      for users with business bank accounts, or to [request a payout for a grant
      offer](https://docs.adyen.com/marketplaces-and-platforms/capital). The API
      also supports use cases for [getting transactions for business bank
      accounts](https://docs.adyen.com/marketplaces-and-platforms/business-accounts/transactions-api)
      and getting [grants and its outstanding
      balances](https://docs.adyen.com/marketplaces-and-platforms/capital#get-balances).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/marketplaces-and-platforms/payout-to-users/on-demand-payouts
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/payout-to-users/on-demand-payouts
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Transfers API
          tags:
            - name: Transfers
            - name: Transactions
            - name: Capital
          paths:
            /grants:
              get:
                tags:
                  - Get
                  - Capital
                  - Account
                  - Grants
                summary: Get a capital account
                description: Returns a list of grants with status and outstanding balances.
              post:
                tags:
                  - Request
                  - Grant
                  - Payouts
                  - Grants
                summary: Request a grant payout
                description: Requests the payout of the selected grant offer.
            /grants/{id}:
              get:
                tags:
                  - Get
                  - Grant
                  - References
                  - Details
                  - Grants
                  - Identifiers
                summary: Get grant reference details
                description: >-
                  Returns the details of a capital account specified in the
                  path.
            /transactions:
              get:
                tags:
                  - Get
                  - All
                  - Transactions
                  - Grants
                  - Identifiers
                  - Transactions
                summary: Get all transactions
                description: >+
                  >Versions 1 and 2 of the Transfers API are deprecated. If you
                  are just starting your implementation, use the latest version.


                  Returns all the transactions related to a balance account,
                  account holder, or balance platform.


                  When making this request, you must include at least one of the
                  following:

                  - `balanceAccountId`

                  - `accountHolderId`

                  - `balancePlatform`.


                  This endpoint supports cursor-based pagination. The response
                  returns the first page of results, and returns links to the
                  next and previous pages when applicable. You can use the links
                  to page through the results.

            /transactions/{id}:
              get:
                tags:
                  - Get
                  - Transactions
                  - Grants
                  - Identifiers
                  - Transactions
                summary: Get a transaction
                description: >-
                  >Versions 1 and 2 of the Transfers API are deprecated. If you
                  are just starting your implementation, use the latest version.


                  Returns a transaction.
            /transfers:
              post:
                tags:
                  - Transfers
                  - Funds
                  - Grants
                  - Identifiers
                  - Transactions
                  - Transfers
                summary: Transfer funds
                description: >-
                  >Versions 1 and 2 of the Transfers API are deprecated. If you
                  are just starting your implementation, use the latest version.


                  Starts a request to transfer funds to [balance
                  accounts](https://docs.adyen.com/api-explorer/#/balanceplatform/latest/post/balanceAccounts),
                  [transfer
                  instruments](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/transferInstruments),
                  or third-party bank accounts. Adyen sends the outcome of the
                  transfer request through webhooks.


                  To use this endpoint, you need an additional role for your API
                  credential and transfers must be enabled for the source
                  balance account. Your Adyen contact will set these up for you.
            /transfers/{transferId}/returns:
              post:
                tags:
                  - Returns
                  - Transfers
                  - Grants
                  - Identifiers
                  - Transactions
                  - Transfers
                  - Returns
                summary: Return a transfer
                description: Returns previously transferred funds w
    overlays:
      - type: APIs.io Search
        url: overlays/transfers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/transfers-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-transfers-api
  - name: FactSet Capital Structure Report Builder API
    description: >-
      Curated data from multiple sources for comprehensive capital analysis
      reports
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/capital-structure-report-builder-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: FactSet Capital Structure Report Builder API
            description: ''
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: Read more about STACH 2.0's row organized schema
            url: https://factset.github.io/stachschema/#/v2/RowOrganized
          tags:
            - name: Capital Structure
          paths:
            /dcs-detail:
              get:
                tags:
                  - Debt
                  - Capital
                  - Structure
                  - S)
                  - Dcs
                  - Detail
                summary: Debt Capital Structure (DCS)
            /source-of-capital:
              get:
                tags:
                  - Source
                  - Of
                  - Capital
                  - Dcs
                  - Detail
                  - Source
                  - Of
                  - Capital
                summary: Source of Capital
            /dcs-summary:
              get:
                tags:
                  - Debt
                  - Capital
                  - Struc
                  - Dcs
                  - Detail
                  - Source
                  - Of
                  - Capital
                  - Summary
                summary: Debt Capital Str
    overlays:
      - type: APIs.io Search
        url: overlays/capital-structure-report-builder-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/capital-structure-report-builder-openapi-api-evangelist-ratings.yml
    aid: factset:factset-capital-structure-report-builder-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---