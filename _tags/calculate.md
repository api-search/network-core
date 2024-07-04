---
name: Calculate
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/calculate.png
url: https://example.com/apis/calculate.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Calculate
apis:
  - name: Adyen Configuration API
    description: >-
      The Configuration API enables you to create a platform where you can
      onboard your users as account holders and create balance accounts, cards,
      and business accounts.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/balanceplatform/2/overview
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/balanceplatform/2/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Configuration API
          tags:
            - name: Platforms
            - name: Account holders
            - name: Balance accounts
            - name: Payment instruments
            - name: Payment instrument groups
            - name: Transaction rules
            - name: Bank account validation
            - name: Network tokens
            - name: Grant accounts
            - name: Grant offers
            - name: Functionality
            - name: Card Orders
            - name: Transfer routes
          paths:
            /accountHolders:
              post:
                tags:
                  - Create
                  - null
                  - Account
                  - Holders
                  - Holders
                summary: Create an account holder
                description: >+
                  Creates an account holder linked to a [legal
                  entity](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/legalEntities).

            /accountHolders/{id}:
              get:
                tags:
                  - Get
                  - null
                  - Account
                  - Holders
                  - Holders
                  - Identifiers
                summary: Get an account holder
                description: Returns an account holder.
              patch:
                tags:
                  - Update
                  - null
                  - Account
                  - Holders
                  - Holders
                  - Identifiers
                summary: Update an account holder
                description: >-
                  Updates an account holder. When updating an account holder
                  resource, if a parameter is not provided in the request, it is
                  left unchanged.
            /accountHolders/{id}/balanceAccounts:
              get:
                tags:
                  - Get
                  - All
                  - Balance
                  - Accounts
                  - Of
                  - null
                  - Account
                  - Holders
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                summary: Get all balance accounts of an account holder
                description: >-
                  Returns a paginated list of the balance accounts associated
                  with an account holder. To fetch multiple pages, use the query
                  parameters. 


                  For example, to limit the page to 5 balance accounts and skip
                  the first 10, use
                  `/accountHolders/{id}/balanceAccounts?limit=5&offset=10`.
            /accountHolders/{id}/taxForms:
              get:
                tags:
                  - Get
                  - Taxes
                  - Forms
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                summary: Get a tax form
                description: >-
                  Generates a tax form for account holders operating in the US.
                  For more information, refer to [Providing tax
                  forms](https://docs.adyen.com/marketplaces-and-platforms/us-tax-forms/).
            /balanceAccounts:
              post:
                tags:
                  - Create
                  - Balance
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                summary: Create a balance account
                description: >-
                  Creates a balance account that holds the funds of the
                  associated account holder.
            /balanceAccounts/{balanceAccountId}/sweeps:
              get:
                tags:
                  - Get
                  - All
                  - Sweeps
                  - For
                  - Balance
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                summary: Get all sweeps for a balance account
                description: >-
                  Returns a list of the sweeps configured for a balance account.


                  To fetch multiple pages, use the query parameters. For
                  example, to limit the page to 5 sweeps and to skip the first
                  10, use
                  `/balanceAccounts/{balanceAccountId}/sweeps?limit=5&offset=10`.
              post:
                tags:
                  - Create
                  - Sweep
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                summary: Create a sweep
                description: >-
                  Creates a sweep that results in moving funds from or to a
                  balance account.


                  A sweep pulls in or pushes out funds based on a defined
                  schedule, amount, currency, and a source or a destination.
            /balanceAccounts/{balanceAccountId}/sweeps/{sweepId}:
              delete:
                tags:
                  - Delete
                  - Sweep
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                summary: Delete a sweep
                description: Deletes a sweep for a balance account.
              get:
                tags:
                  - Get
                  - Sweep
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                summary: Get a sweep
                description: Returns a sweep.
              patch:
                tags:
                  - Update
                  - Sweep
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                summary: Update a sweep
                description: >-
                  Updates a sweep. When updating a sweep resource, note that if
                  a request parameter is not provided, the parameter is left
                  unchanged.
            /balanceAccounts/{id}:
              get:
                tags:
                  - Get
                  - Balance
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                summary: Get a balance account
                description: >-
                  Returns a balance account and its balances for the default
                  currency and other currencies with a non-zero balance.
              patch:
                tags:
                  - Update
                  - Balance
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                summary: Update a balance account
                description: Updates a balance account.
            /balanceAccounts/{id}/paymentInstruments:
              get:
                tags:
                  - Get
                  - Payments
                  - Instruments
                  - Linked
                  - To
                  - Balance
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                summary: Get payment instruments linked to a balance account
                description: >-
                  Returns a paginated list of the payment instruments associated
                  with a balance account. 


                  To fetch multiple pages, use the query parameters.For example,
                  to limit the page to 3 payment instruments which are in active
                  status and to skip the first 6, use
                  `/balanceAccounts/{id}/paymentInstruments?limit=3&offset=6&status=active`.
            /balancePlatforms/{id}:
              get:
                tags:
                  - Get
                  - Balance
                  - Platforms
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                summary: Get a balance platform
                description: Returns a balance platform.
            /balancePlatforms/{id}/accountHolders:
              get:
                tags:
                  - Get
                  - All
                  - Account
                  - Holders
                  - Under
                  - Balance
                  - Platforms
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                summary: Get all account holders under a balance platform
                description: >-
                  Returns a paginated list of all the account holders that
                  belong to the balance platform. To fetch multiple pages, use
                  the query parameters. 


                  For example, to limit the page to 5 account holders and to
                  skip the first 20, use
                  `/balancePlatforms/{id}/accountHolders?limit=5&offset=20`.
            /cardorders:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Cards
                  - Orders
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                summary: Get a list of card orders
                description: Returns a paginated list of card orders.
            /cardorders/{id}/items:
              get:
                tags:
                  - Get
                  - Cards
                  - Orders
                  - Items
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                summary: Get card order items
                description: Returns the item list of a specific card order.
            /grantAccounts/{id}:
              get:
                tags:
                  - Get
                  - Grant
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                summary: Get a grant account
                description: >-
                  Returns the details of the [grant
                  account](https://docs.adyen.com/marketplaces-and-platforms/capital#grant-account).
            /grantOffers:
              get:
                tags:
                  - Get
                  - All
                  - Available
                  - Grant
                  - Offers
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                summary: Get all available grant offers
                description: >-
                  Returns a list of all [grant
                  offers](https://docs.adyen.com/marketplaces-and-platforms/capital#grant-offers)
                  available for `accountHolderId` specified as a query
                  parameter.
            /grantOffers/{grantOfferId}:
              get:
                tags:
                  - Get
                  - Grant
                  - Offers
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                summary: Get a grant offer
                description: Returns the details of a single grant offer.
            /networkTokens/{networkTokenId}:
              get:
                tags:
                  - Get
                  - Networks
                  - Tokens
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                summary: Get a network token
                description: Returns the details of a network token.
              patch:
                tags:
                  - Update
                  - Networks
                  - Tokens
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                summary: Update a network token
                description: Updates the status of the network token.
            /paymentInstrumentGroups:
              post:
                tags:
                  - Create
                  - Payments
                  - Instruments
                  - Group
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                summary: Create a payment instrument group
                description: >-
                  Creates a payment instrument group to associate and group
                  payment instrument resources together. You can apply a
                  transaction rule to a payment instrument group.
            /paymentInstrumentGroups/{id}:
              get:
                tags:
                  - Get
                  - Payments
                  - Instruments
                  - Group
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                summary: Get a payment instrument group
                description: Returns the details of a payment instrument group.
            /paymentInstrumentGroups/{id}/transactionRules:
              get:
                tags:
                  - Get
                  - All
                  - Transactions
                  - Rules
                  - For
                  - Payments
                  - Instruments
                  - Group
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                summary: Get all transaction rules for a payment instrument group
                description: >-
                  Returns a list of all the transaction rules associated with a
                  payment instrument group.
            /paymentInstruments:
              post:
                tags:
                  - Create
                  - Payments
                  - Instruments
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                summary: Create a payment instrument
                description: >-
                  Creates a payment instrument to issue a physical card, a
                  virtual card, or a business account to your user.

                   For more information, refer to [Issue cards](https://docs.adyen.com/issuing/create-cards) or [Issue business accounts](https://docs.adyen.com/marketplaces-and-platforms/business-accounts).
            /paymentInstruments/{id}:
              get:
                tags:
                  - Get
                  - Payments
                  - Instruments
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                summary: Get a payment instrument
                description: Returns the details of a payment instrument.
              patch:
                tags:
                  - Update
                  - Payments
                  - Instruments
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                summary: Update a payment instrument
                description: >-
                  Updates a payment instrument. Once a payment instrument is
                  already active, you can only update its status. However, for
                  cards created with **inactive** status, you can still update
                  the balance account associated with the card.
            /paymentInstruments/{id}/networkTokens:
              get:
                tags:
                  - Lists
                  - Networks
                  - Tokens
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                summary: List network tokens
                description: List the network tokens connected to a payment instrument.
            /paymentInstruments/{id}/reveal:
              get:
                tags:
                  - Get
                  - The
                  - Of
                  - Payments
                  - Instruments
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                summary: Get the PAN of a payment instrument
                description: >-
                  Returns the primary account number (PAN) of a payment
                  instrument.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/issuing/manage-access/api-credentials-web-service#api-permissions):


                  * Balance Platform BCL PCI role
            /paymentInstruments/{id}/transactionRules:
              get:
                tags:
                  - Get
                  - All
                  - Transactions
                  - Rules
                  - For
                  - Payments
                  - Instruments
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                summary: Get all transaction rules for a payment instrument
                description: >-
                  Returns a list of transaction rules associated with a payment
                  instrument.
            /pins/change:
              post:
                tags:
                  - Change
                  - Pin
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                summary: Change Pin
                description: Change Pin
            /pins/publicKey:
              get:
                tags:
                  - Get
                  - Public
                  - Keys
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                summary: Get RSA publicKey
                description: Get RSA publicKey
            /pins/reveal:
              post:
                tags:
                  - Reveal
                  - Pin
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                summary: Reveal Pin
                description: Reveal Pin
            /transactionRules:
              post:
                tags:
                  - Create
                  - Transactions
                  - Rules
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                summary: Create a transaction rule
                description: >-
                  Creates a [transaction
                  rule](https://docs.adyen.com/issuing/transaction-rules). When
                  your user makes a transaction with their Adyen-issued card,
                  the transaction is allowed or declined based on the conditions
                  and outcome defined in the transaction rule. You can apply the
                  transaction rule to several cards, such as all the cards in
                  your platform, or to a specific card. For use cases, see
                  [examples](https://docs.adyen.com/issuing/transaction-rules/examples).
            /transactionRules/{transactionRuleId}:
              delete:
                tags:
                  - Delete
                  - Transactions
                  - Rules
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                  - Rules
                summary: Delete a transaction rule
                description: Deletes a transaction rule.
              get:
                tags:
                  - Get
                  - Transactions
                  - Rules
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                  - Rules
                summary: Get a transaction rule
                description: Returns the details of a transaction rule.
              patch:
                tags:
                  - Update
                  - Transactions
                  - Rules
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                  - Rules
                summary: Update a transaction rule
                description: >-
                  Updates a transaction rule. 


                  * To update only the status of a transaction rule, send only
                  the `status` parameter. All other parameters not provided in
                  the request are left unchanged.


                  * When updating any other parameter, you need to send all
                  existing resource parameters. If you omit a parameter in the
                  request, that parameter is removed from the resource.
            /transferRoutes/calculate:
              post:
                tags:
                  - Calculate
                  - Transfers
                  - Routes
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                  - Rules
                  - Routes
                  - Calculate
                summary: Calculate transfer routes
                description: >-
                  Returns available transfer routes based on a combination of
                  transfer `country`, `currency`, `counterparty`, and
                  `priorities`. Use this endpoint to find optimal transfer
                  priorities and associated requirements before you [make a
                  transfer](https://docs.adyen.com/api-explorer/transfers/latest/post/transfers).
            /validateBankAccountIdentification:
              post:
                tags:
                  - Validate
                  - Bank
                  - Account
                  - Holders
                  - Identifiers
                  - Balance
                  - Accounts
                  - Taxes
                  - Forms
                  - Account
                  - Sweeps
                  - Sweep
                  - Payments
                  - Instruments
                  - Platforms
                  - Card Orders
                  - Items
                  - Offers
                  - Grant
                  - Offers
                  - Tokens
                  - Networks
                  - Tokens
                  - Instruments
                  - Groups
                  - Transactions
                  - Rules
                  - Reveal
                  - Pins
                  - Change
                  - Keys
                  - Rules
                  - Routes
                  - Calculate
                  - Bank
                  - Identification
                summary: Validate a bank account
                description: >-
                  Validates bank account identification details. You can use
                  this endpoint to validate bank account details before you
                  [make a
                  transfer](https://docs.adyen.com/api-explorer/transfers/latest/post/transfers)
                  or [create a transfer
                  instrument](https://docs.adyen.com/api-explorer/legalentity
    overlays:
      - type: APIs.io Search
        url: overlays/configuration-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/configuration-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-configuration-api
  - name: location
    description: >-
      <p>"Suite of geospatial services including Maps, Places, Routes, Tracking,
      and Geofencing"</p>
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: location
          paths:
            /tracking/v0/trackers/{TrackerName}/consumers:
              POST:
                summary: AssociateTrackerConsumer
                description: >-
                  <p>Creates an association between a geofence collection and a
                  tracker resource. This allows the tracker resource to
                  communicate location data to the linked geofence collection.
                  </p> <p>You can associate up to five geofence collections to
                  each tracker resource.</p> <note> <p>Currently not supported —
                  Cross-account configurations, such as creating associations
                  between a tracker resource in one account and a geofence
                  collection in another account.</p> </note>
                tags:
                  - Associate
                  - Trackers
                  - Consumer
                  - Trackers
                  - Names
                  - Consumers
            /tracking/v0/trackers/{TrackerName}/delete-positions:
              POST:
                summary: BatchDeleteDevicePositionHistory
                description: >-
                  <p>Deletes the position history of one or more devices from a
                  tracker resource.</p>
                tags:
                  - Batches
                  - Delete
                  - Device
                  - Positions
                  - History
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
            /geofencing/v0/collections/{CollectionName}/delete-geofences:
              POST:
                summary: BatchDeleteGeofence
                description: >-
                  <p>Deletes a batch of geofences from a geofence
                  collection.</p> <note> <p>This operation deletes the resource
                  permanently.</p> </note>
                tags:
                  - Batches
                  - Delete
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
            /geofencing/v0/collections/{CollectionName}/positions:
              POST:
                summary: BatchEvaluateGeofences
                description: >-
                  <p>Evaluates device positions against the geofence geometries
                  from a given geofence collection.</p> <p>This operation always
                  returns an empty response because geofences are asynchronously
                  evaluated. The evaluation determines if the device has entered
                  or exited a geofenced area, and then publishes one of the
                  following events to Amazon EventBridge:</p> <ul> <li> <p>
                  <code>ENTER</code> if Amazon Location determines that the
                  tracked device has entered a geofenced area.</p> </li> <li>
                  <p> <code>EXIT</code> if Amazon Location determines that the
                  tracked device has exited a geofenced area.</p> </li> </ul>
                  <note> <p>The last geofence that a device was observed within
                  is tracked for 30 days after the most recent device position
                  update.</p> </note> <note> <p>Geofence evaluation uses the
                  given device position. It does not account for the optional
                  <code>Accuracy</code> of a
                  <code>DevicePositionUpdate</code>.</p> </note> <note> <p>The
                  <code>DeviceID</code> is used as a string to represent the
                  device. You do not need to have a <code>Tracker</code>
                  associated with the <code>DeviceID</code>.</p> </note>
                tags:
                  - Batches
                  - Evaluate
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
            /tracking/v0/trackers/{TrackerName}/get-positions:
              POST:
                summary: BatchGetDevicePosition
                description: >-
                  <p>Lists the latest device positions for requested
                  devices.</p>
                tags:
                  - Batches
                  - Get
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
            /geofencing/v0/collections/{CollectionName}/put-geofences:
              POST:
                summary: BatchPutGeofence
                description: >-
                  <p>A batch request for storing geofence geometries into a
                  given geofence collection, or updates the geometry of an
                  existing geofence if a geofence ID is included in the
                  request.</p>
                tags:
                  - Batches
                  - Put
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
            /tracking/v0/trackers/{TrackerName}/positions:
              POST:
                summary: BatchUpdateDevicePosition
                description: >-
                  <p>Uploads position update data for one or more devices to a
                  tracker resource (up to 10 devices per batch). Amazon Location
                  uses the data when it reports the last known device position
                  and position history. Amazon Location retains location data
                  for 30 days.</p> <note> <p>Position updates are handled based
                  on the <code>PositionFiltering</code> property of the tracker.
                  When <code>PositionFiltering</code> is set to
                  <code>TimeBased</code>, updates are evaluated against linked
                  geofence collections, and location data is stored at a maximum
                  of one position per 30 second interval. If your update
                  frequency is more often than every 30 seconds, only one update
                  per 30 seconds is stored for each unique device ID.</p>
                  <p>When <code>PositionFiltering</code> is set to
                  <code>DistanceBased</code> filtering, location data is stored
                  and evaluated against linked geofence collections only if the
                  device has moved more than 30 m (98.4 ft).</p> <p>When
                  <code>PositionFiltering</code> is set to
                  <code>AccuracyBased</code> filtering, location data is stored
                  and evaluated against linked geofence collections only if the
                  device has moved more than the measured accuracy. For example,
                  if two consecutive updates from a device have a horizontal
                  accuracy of 5 m and 10 m, the second update is neither stored
                  or evaluated if the device has moved less than 15 m. If
                  <code>PositionFiltering</code> is set to
                  <code>AccuracyBased</code> filtering, Amazon Location uses the
                  default value <code>{ "Horizontal": 0}</code> when accuracy is
                  not provided on a <code>DevicePositionUpdate</code>.</p>
                  </note>
                tags:
                  - Batches
                  - Update
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
            /routes/v0/calculators/{CalculatorName}/calculate/route:
              POST:
                summary: CalculateRoute
                description: >-
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/calculate-route.html">Calculates
                  a route</a> given the following required parameters:
                  <code>DeparturePosition</code> and
                  <code>DestinationPosition</code>. Requires that you first <a
                  href="https://docs.aws.amazon.com/location-routes/latest/APIReference/API_CreateRouteCalculator.html">create
                  a route calculator resource</a>.</p> <p>By default, a request
                  that doesn't specify a departure time uses the best time of
                  day to travel with the best traffic conditions when
                  calculating the route.</p> <p>Additional options include:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/departure-time.html">Specifying
                  a departure time</a> using either <code>DepartureTime</code>
                  or <code>DepartNow</code>. This calculates a route based on
                  predictive traffic data at the given time. </p> <note> <p>You
                  can't specify both <code>DepartureTime</code> and
                  <code>DepartNow</code> in a single request. Specifying both
                  parameters returns a validation error.</p> </note> </li> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/travel-mode.html">Specifying
                  a travel mode</a> using TravelMode sets the transportation
                  mode used to calculate the routes. This also lets you specify
                  additional route preferences in <code>CarModeOptions</code> if
                  traveling by <code>Car</code>, or
                  <code>TruckModeOptions</code> if traveling by
                  <code>Truck</code>.</p> <note> <p>If you specify
                  <code>walking</code> for the travel mode and your data
                  provider is Esri, the start and destination must be within
                  40km.</p> </note> </li> </ul>
                tags:
                  - Calculate
                  - Routes
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
            /routes/v0/calculators/{CalculatorName}/calculate/route-matrix:
              POST:
                summary: CalculateRouteMatrix
                description: >-
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/calculate-route-matrix.html">
                  Calculates a route matrix</a> given the following required
                  parameters: <code>DeparturePositions</code> and
                  <code>DestinationPositions</code>.
                  <code>CalculateRouteMatrix</code> calculates routes and
                  returns the travel time and travel distance from each
                  departure position to each destination position in the
                  request. For example, given departure positions A and B, and
                  destination positions X and Y,
                  <code>CalculateRouteMatrix</code> will return time and
                  distance for routes from A to X, A to Y, B to X, and B to Y
                  (in that order). The number of results returned (and routes
                  calculated) will be the number of
                  <code>DeparturePositions</code> times the number of
                  <code>DestinationPositions</code>.</p> <note> <p>Your account
                  is charged for each route calculated, not the number of
                  requests.</p> </note> <p>Requires that you first <a
                  href="https://docs.aws.amazon.com/location-routes/latest/APIReference/API_CreateRouteCalculator.html">create
                  a route calculator resource</a>.</p> <p>By default, a request
                  that doesn't specify a departure time uses the best time of
                  day to travel with the best traffic conditions when
                  calculating routes.</p> <p>Additional options include:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/departure-time.html">
                  Specifying a departure time</a> using either
                  <code>DepartureTime</code> or <code>DepartNow</code>. This
                  calculates routes based on predictive traffic data at the
                  given time. </p> <note> <p>You can't specify both
                  <code>DepartureTime</code> and <code>DepartNow</code> in a
                  single request. Specifying both parameters returns a
                  validation error.</p> </note> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/travel-mode.html">Specifying
                  a travel mode</a> using TravelMode sets the transportation
                  mode used to calculate the routes. This also lets you specify
                  additional route preferences in <code>CarModeOptions</code> if
                  traveling by <code>Car</code>, or
                  <code>TruckModeOptions</code> if traveling by
                  <code>Truck</code>.</p> </li> </ul>
                tags:
                  - Calculate
                  - Routes
                  - Matrix
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
            /geofencing/v0/collections:
              POST:
                summary: CreateGeofenceCollection
                description: >-
                  <p>Creates a geofence collection, which manages and stores
                  geofences.</p>
                tags:
                  - Create
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
            /metadata/v0/keys:
              POST:
                summary: CreateKey
                description: >-
                  <p>Creates an API key resource in your Amazon Web Services
                  account, which lets you grant actions for Amazon Location
                  resources to the API key bearer.</p> <note> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/using-apikeys.html">Using
                  API keys</a>.</p> </note>
                tags:
                  - Create
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
            /maps/v0/maps:
              POST:
                summary: CreateMap
                description: >-
                  <p>Creates a map resource in your Amazon Web Services account,
                  which provides map tiles of different styles sourced from
                  global location data providers.</p> <note> <p>If your
                  application is tracking or routing assets you use in your
                  business, such as delivery vehicles or employees, you must not
                  use Esri as your geolocation provider. See section 82 of the
                  <a href="http://aws.amazon.com/service-terms">Amazon Web
                  Services service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
            /places/v0/indexes:
              POST:
                summary: CreatePlaceIndex
                description: >-
                  <p>Creates a place index resource in your Amazon Web Services
                  account. Use a place index resource to geocode addresses and
                  other text queries by using the
                  <code>SearchPlaceIndexForText</code> operation, and reverse
                  geocode coordinates by using the
                  <code>SearchPlaceIndexForPosition</code> operation, and enable
                  autosuggestions by using the
                  <code>SearchPlaceIndexForSuggestions</code> operation.</p>
                  <note> <p>If your application is tracking or routing assets
                  you use in your business, such as delivery vehicles or
                  employees, you must not use Esri as your geolocation provider.
                  See section 82 of the <a
                  href="http://aws.amazon.com/service-terms">Amazon Web Services
                  service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Places
                  - Index
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
            /routes/v0/calculators:
              POST:
                summary: CreateRouteCalculator
                description: >-
                  <p>Creates a route calculator resource in your Amazon Web
                  Services account.</p> <p>You can send requests to a route
                  calculator resource to estimate travel time, distance, and get
                  directions. A route calculator sources traffic and road
                  network data from your chosen data provider.</p> <note> <p>If
                  your application is tracking or routing assets you use in your
                  business, such as delivery vehicles or employees, you must not
                  use Esri as your geolocation provider. See section 82 of the
                  <a href="http://aws.amazon.com/service-terms">Amazon Web
                  Services service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
            /tracking/v0/trackers:
              POST:
                summary: CreateTracker
                description: >-
                  <p>Creates a tracker resource in your Amazon Web Services
                  account, which lets you retrieve current and historical
                  location of devices.</p>
                tags:
                  - Create
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
            /geofencing/v0/collections/{CollectionName}:
              PATCH:
                summary: UpdateGeofenceCollection
                description: >-
                  <p>Updates the specified properties of a given geofence
                  collection.</p>
                tags:
                  - Update
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
            /metadata/v0/keys/{KeyName}:
              PATCH:
                summary: UpdateKey
                description: >-
                  <p>Updates the specified properties of a given API key
                  resource.</p>
                tags:
                  - Update
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
            /maps/v0/maps/{MapName}:
              PATCH:
                summary: UpdateMap
                description: >-
                  <p>Updates the specified properties of a given map
                  resource.</p>
                tags:
                  - Update
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
            /places/v0/indexes/{IndexName}:
              PATCH:
                summary: UpdatePlaceIndex
                description: >-
                  <p>Updates the specified properties of a given place index
                  resource.</p>
                tags:
                  - Update
                  - Places
                  - Index
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /routes/v0/calculators/{CalculatorName}:
              PATCH:
                summary: UpdateRouteCalculator
                description: >-
                  <p>Updates the specified properties for a given route
                  calculator resource.</p>
                tags:
                  - Update
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /tracking/v0/trackers/{TrackerName}:
              PATCH:
                summary: UpdateTracker
                description: >-
                  <p>Updates the specified properties of a given tracker
                  resource.</p>
                tags:
                  - Update
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /tracking/v0/trackers/{TrackerName}/consumers/{ConsumerArn}:
              DELETE:
                summary: DisassociateTrackerConsumer
                description: >-
                  <p>Removes the association between a tracker resource and a
                  geofence collection.</p> <note> <p>Once you unlink a tracker
                  resource from a geofence collection, the tracker positions
                  will no longer be automatically evaluated against
                  geofences.</p> </note>
                tags:
                  - Disassociate
                  - Trackers
                  - Consumer
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
            /tracking/v0/trackers/{TrackerName}/devices/{DeviceId}/positions/latest:
              GET:
                summary: GetDevicePosition
                description: >-
                  <p>Retrieves a device's most recent position according to its
                  sample time.</p> <note> <p>Device positions are deleted after
                  30 days.</p> </note>
                tags:
                  - Get
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
            /tracking/v0/trackers/{TrackerName}/devices/{DeviceId}/list-positions:
              POST:
                summary: GetDevicePositionHistory
                description: >-
                  <p>Retrieves the device position history from a tracker
                  resource within a specified range of time.</p> <note>
                  <p>Device positions are deleted after 30 days.</p> </note>
                tags:
                  - Get
                  - Device
                  - Positions
                  - History
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
            /geofencing/v0/collections/{CollectionName}/geofences/{GeofenceId}:
              PUT:
                summary: PutGeofence
                description: >-
                  <p>Stores a geofence geometry in a given geofence collection,
                  or updates the geometry of an existing geofence if a geofence
                  ID is included in the request. </p>
                tags:
                  - Put
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
            /maps/v0/maps/{MapName}/glyphs/{FontStack}/{FontUnicodeRange}:
              GET:
                summary: GetMapGlyphs
                description: <p>Retrieves glyphs used to display labels on a map.</p>
                tags:
                  - Get
                  - Maps
                  - Glyphs
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
            /maps/v0/maps/{MapName}/sprites/{FileName}:
              GET:
                summary: GetMapSprites
                description: >-
                  <p>Retrieves the sprite sheet corresponding to a map resource.
                  The sprite sheet is a PNG image paired with a JSON document
                  describing the offsets of individual icons that will be
                  displayed on a rendered map.</p>
                tags:
                  - Get
                  - Maps
                  - Sprites
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
            /maps/v0/maps/{MapName}/style-descriptor:
              GET:
                summary: GetMapStyleDescriptor
                description: >-
                  <p>Retrieves the map style descriptor from a map resource.
                  </p> <p>The style descriptor contains speciﬁcations on how
                  features render on a map. For example, what data to display,
                  what order to display the data in, and the style for the data.
                  Style descriptors follow the Mapbox Style Specification.</p>
                tags:
                  - Get
                  - Maps
                  - Styles
                  - Descriptions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
            /maps/v0/maps/{MapName}/tiles/{Z}/{X}/{Y}:
              GET:
                summary: GetMapTile
                description: >-
                  <p>Retrieves a vector data tile from the map resource. Map
                  tiles are used by clients to render a map. they're addressed
                  using a grid arrangement with an X coordinate, Y coordinate,
                  and Z (zoom) level. </p> <p>The origin (0, 0) is the top left
                  of the map. Increasing the zoom level by 1 doubles both the X
                  and Y dimensions, so a tile containing data for the entire
                  world at (0/0/0) will be split into 4 tiles at zoom 1 (1/0/0,
                  1/0/1, 1/1/0, 1/1/1).</p>
                tags:
                  - Get
                  - Maps
                  - Tiles
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
            /places/v0/indexes/{IndexName}/places/{PlaceId}:
              GET:
                summary: GetPlace
                description: >-
                  <p>Finds a place by its unique ID. A <code>PlaceId</code> is
                  returned by other search operations.</p> <note> <p>A PlaceId
                  is valid only if all of the following are the same in the
                  original search request and the call to
                  <code>GetPlace</code>.</p> <ul> <li> <p>Customer Amazon Web
                  Services account</p> </li> <li> <p>Amazon Web Services
                  Region</p> </li> <li> <p>Data provider specified in the place
                  index resource</p> </li> </ul> </note>
                tags:
                  - Get
                  - Places
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /tracking/v0/trackers/{TrackerName}/list-positions:
              POST:
                summary: ListDevicePositions
                description: <p>A batch request to retrieve all device positions.</p>
                tags:
                  - Lists
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /geofencing/v0/list-collections:
              POST:
                summary: ListGeofenceCollections
                description: >-
                  <p>Lists geofence collections in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /geofencing/v0/collections/{CollectionName}/list-geofences:
              POST:
                summary: ListGeofences
                description: <p>Lists geofences stored in a given geofence collection.</p>
                tags:
                  - Lists
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /metadata/v0/list-keys:
              POST:
                summary: ListKeys
                description: >-
                  <p>Lists API key resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /maps/v0/list-maps:
              POST:
                summary: ListMaps
                description: >-
                  <p>Lists map resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /places/v0/list-indexes:
              POST:
                summary: ListPlaceIndexes
                description: >-
                  <p>Lists place index resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Places
                  - Indexes
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /routes/v0/list-calculators:
              POST:
                summary: ListRouteCalculators
                description: >-
                  <p>Lists route calculator resources in your Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from the specified Amazon Location
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /tracking/v0/trackers/{TrackerName}/list-consumers:
              POST:
                summary: ListTrackerConsumers
                description: >-
                  <p>Lists geofence collections currently associated to the
                  given tracker resource.</p>
                tags:
                  - Lists
                  - Trackers
                  - Consumers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /tracking/v0/list-trackers:
              POST:
                summary: ListTrackers
                description: >-
                  <p>Lists tracker resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /places/v0/indexes/{IndexName}/search/position:
              POST:
                summary: SearchPlaceIndexForPosition
                description: >-
                  <p>Reverse geocodes a given coordinate and returns a legible
                  address. Allows you to search for Places or points of interest
                  near a given position.</p>
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
            /places/v0/indexes/{IndexName}/search/suggestions:
              POST:
                summary: SearchPlaceIndexForSuggestions
                description: >-
                  <p>Generates suggestions for addresses and points of interest
                  based on partial or misspelled free-form text. This operation
                  is also known as autocomplete, autosuggest, or fuzzy
                  matching.</p> <p>Optional parameters let you narrow your
                  search results by bounding box or country, or bias your search
                  toward a specific position on the globe.</p> <note> <p>You can
                  search for suggested place names near a specified position by
                  using <code>BiasPosition</code>, or filter results within a
                  bounding box by using <code>FilterBBox</code>. These
                  parameters are mutually exclusive; using both
                  <code>BiasPosition</code> and <code>FilterBBox</code> in the
                  same command returns an error.</p> </note>
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Suggestions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
                  - Suggestions
            /places/v0/indexes/{IndexName}/search/text:
              POST:
                summary: SearchPlaceIndexForText
                description: >-
                  <p>Geocodes free-form text, such as an address, name, city, or
                  region to allow you to search for Places or points of
                  interest. </p> <p>Optional parameters let you narrow your
                  search results by bounding box or country, or bias your search
                  toward a specific position on the globe.</p> <note> <p>You can
                  search for places near a given position using
                  <code>BiasPosition</code>, or filter results within a bounding
                  box using <code>FilterBBox</code>. Providing both parameters
                  simultaneously returns an error.</p> </note> <p>Search results
                  are returned in order of highest to lowest rele
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Text
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
                  - Suggestions
                  - Te
    overlays:
      - type: APIs.io Search
        url: overlays/location-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/location-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:location
  - name: FactSet Universal Screening API
    description: >-
      Use the Universal Screening API to calculate your saved screens and then
      output the results in a convenient JSON format or archive the results to
      an Open FactSet Database (OFDB) file
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/universal-screening-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/universal-screening-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/universal-screening-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/universal-screening-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/universal-screening-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/universal-screening-api#changelog
      - type: OpenAPI
        data:
          info:
            title: Universal Screening API
          openapi: 3.0.2
          externalDocs:
            description: Read more about STACH 2.0's column organized schema
            url: https://factset.github.io/stachschema/#/v2/ColumnOrganized
          paths:
            /v2/job/archive:
              post:
                description: >-
                  Begins archive of screen to OFDB. Subject to rate limiting by
                  serial.
                tags:
                  - V2
                  - Job
                  - Archive
            /v2/job/calculate:
              post:
                description: >-
                  Begins calculation of screen. Subject to rate limiting by
                  serial.
                tags:
                  - V2
                  - Job
                  - Archive
                  - Calculate
            /v2/job/{id}/status:
              get:
                description: Polls the job with a given screen ID and returns job status
                tags:
                  - V2
                  - Job
                  - Archive
                  - Calculate
                  - Id
                  - Status
            /v2/jobs:
              get:
                description: >-
                  Retrieve list of all active job ids started by requester's
                  username-serial
                tags:
                  - V2
                  - Job
                  - Archive
                  - Calculate
                  - Id
                  - Status
                  - Jobs
              delete:
                description: >-
                  Delete all active jobs started by the requester's
                  username-serial
                tags:
                  - V2
                  - Job
                  - Archive
                  - Calculate
                  - Id
                  - Status
                  - Jobs
            /v2/job/{id}:
              delete:
                description: >-
                  Delete a specified job started by the requester's
                  username-serial
                tags:
                  - V2
                  - Job
                  - Archive
                  - Calculate
                  - Id
                  - Status
                  - Jobs
              get:
                description: >-
                  Retrieve results of complete screen calculation. Screens with
                  more than 10,000 rows will be returned in a paginated format.
                  Results may be fetched in pages of 1,000 - 100,000 results
                  with 10,000 being the default page size.
                tags:
                  - V2
                  - Job
                  - Archive
                  - Calculate
                  - Id
                  - Status
                  - Jo
    overlays:
      - type: APIs.io Search
        url: overlays/universal-screening-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/universal-screening-openapi-api-evangelist-ratings.yml
    aid: factset:factset-universal-screening-api
  - name: FactSet Open Risk API
    description: >-
      Through this API one can get a comprehensive access to factor-based linear
      risk analytics engine, offering flexible and powerful risk analyses with
      full capability.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/openrisk-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/openrisk-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/openrisk-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/openrisk-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/openrisk-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/openrisk-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Open Risk API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          tags:
            - name: About
            - name: Operations
          paths:
            /linear/{version}/riskmodels:
              get:
                summary: Get available risk models
                description: >-
                  Get the list of available risk models, including their
                  respective model codes required for use with other routes.
                tags:
                  - Get
                  - Available
                  - Risk
                  - Models
                  - Linear
                  - Version
                  - Riskmodels
            /linear/{version}/riskmodels/{modelCode}:
              get:
                summary: Get risk model details
                description: >-
                  Get the meta data of the risk model for the corresponding
                  modelCode. modelCode can be obtained via
                  '/linear/{version}/riskmodels/' route.
                tags:
                  - Get
                  - Risk
                  - Model
                  - Details
                  - Linear
                  - Version
                  - Riskmodels
                  - Code
            /linear/{version}/stats:
              get:
                summary: Get available risk statistics details
                description: >-
                  All base risk statistic names and their respective support
                  and/or requirement for certain name-settings statistics
                  options (such as: correlated specific risk, covariance
                  isolation method, etc.), available levels, and security group
                  calculation methodology. When 'securityGroupMethod' is
                  'statSpecific', please refer to statistics documentation
                  service for more information.
                tags:
                  - Get
                  - Available
                  - Risk
                  - Statistics
                  - Details
                  - Linear
                  - Version
                  - Riskmodels
                  - Code
                  - Stats
            /linear/{version}/stats-names-only:
              get:
                summary: Get available risk statistics names
                description: >-
                  All available risk statistic names including statistics names
                  containing risk statistics options such as CSR (correlated
                  specific risk)
                tags:
                  - Get
                  - Available
                  - Risk
                  - Statistics
                  - Names
                  - Linear
                  - Version
                  - Riskmodels
                  - Code
                  - Stats
                  - Names
                  - Only
            /linear/{version}/health:
              get:
                summary: Get health of service
                description: Health status of the service
                tags:
                  - Get
                  - Health
                  - Of
                  - Service
                  - Linear
                  - Version
                  - Riskmodels
                  - Code
                  - Stats
                  - Names
                  - Only
                  - Health
            /linear/{version}/calculate/from-holdings:
              post:
                summary: Calculate risk statistics
                description: >-
                  Calculate predicted risk statistics for provided holdings
                  using risk model data. Asset symbols and market values/weights
                  are required.
                tags:
                  - Calculate
                  - Risk
                  - Statistics
                  - Linear
                  - Version
                  - Riskmodels
                  - Code
                  - Stats
                  - Names
                  - Only
                  - Health
                  - Calculate
                  - From
                  - Holdings
            /linear/{version}/generate/id-mapping:
              post:
                summary: Generate risk model ID mapping
                description: >-
                  Resolve all input holdings IDs against a risk model for
                  coverage and provide a mapping to security indices in the
                  model or the reason for exclusion
                tags:
                  - Generate
                  - Risk
                  - Model
                  - Mapping
                  - Linear
                  - Version
                  - Riskmodels
                  - Code
                  - Stats
                  - Names
                  - Only
                  - Health
                  - Calculate
                  - From
                  - Holdings
                  - Generate
                  - Id
                  - Mapping
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-
    overlays:
      - type: APIs.io Search
        url: overlays/open-risk-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/open-risk-openapi-api-evangelist-ratings.yml
    aid: factset:factset-open-risk-api
  - name: FactSet Investment Banking Office Refresh API
    description: Refresh FactSet models (e.g., Excel templates with =FDS codes).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/investment-banking-office-refresh-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/investment-banking-office-refresh-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Investment Banking Office Refresh API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          paths:
            /refresh/calculate:
              post:
                summary: Upload a spreadsheet file
                description: >-
                  Upload a spreadsheet file (in the Open Office XML format) for
                  FactSet to refresh.
                tags:
                  - Upload
                  - Spreadsheet
                  - File
                  - Refresh
                  - Calculate
            /refresh/{id}/status:
              get:
                summary: Get the status of the refresh job with the given resource ID
                description: Check the status of the given job by the resource ID
                tags:
                  - Get
                  - The
                  - Status
                  - Of
                  - Refresh
                  - Job
                  - With
                  - Given
                  - Resource
                  - Refresh
                  - Calculate
                  - Id
                  - Status
            /refresh/{id}:
              get:
                summary: Retrieve a calculated file by resource ID.
                description: >-
                  If the requested job is complete, the calculated file will be
                  returned.
                tags:
                  - Retrieve
                  - Calculated
                  - File
                  - By
                  - Resource
                  - D.
                  - Refresh
                  - Calculate
                  - Id
                  - Status
          tags:
            - name: nu
    overlays:
      - type: APIs.io Search
        url: overlays/investment-banking-office-refresh-openapi-original.yml
      - type: APIs.io Search
        url: overlays/investment-banking-office-refresh-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/investment-banking-office-refresh-openapi-api-evangelist-ratings.yml
    aid: factset:factset-investment-banking-office-refresh-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---