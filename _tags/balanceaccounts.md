---
name: Balanceaccounts
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/balanceaccounts.png
url: https://example.com/apis/balanceaccounts.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Balanceaccounts
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
  - name: Adyen Configuration Webhooks API
    description: >-
      Adyen sends webhooks to inform your system about events that occur in your
      platform. These events include, for example, when an account holders
      capabilities are updated, or when a sweep configuration is created or
      updated. When an event occurs, Adyen makes an HTTP POST request to a URL
      on your server and includes the details of the event in the request body.
      You can use these webhooks to build your implementation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/balanceplatform-webhooks/1/overview
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/api-explorer/balanceplatform-webhooks/1/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Configuration webhooks
          tags:
            - name: Account holder
            - name: Balance Accounts
            - name: Payment instrument
            - name: Card Orders
          x-staticResponse: response.json
          webhooks:
            balancePlatform.accountHolder.created:
              post:
                tags:
                  - Account holder
                summary: Account holder created
                description: >-
                  Adyen sends this webhook when you successfully [create an
                  account
                  holder](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/accountHolders).
                operationId: post-balancePlatform.accountHolder.created
                x-sortIndex: 1
                x-methodName: accountHolderCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-accountHolder-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.created-balancePlatform-accountHolder-created
                        balancePlatform-accountHolder-created-lem-v3:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.created-balancePlatform-accountHolder-created-lem-v3
                      schema:
                        $ref: '#/components/schemas/AccountHolderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-accountHolder-created:
                            $ref: '#/components/examples/WebhookAck'
                          balancePlatform-accountHolder-created-lem-v3:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.accountHolder.updated:
              post:
                tags:
                  - Account holder
                summary: Account holder updated
                description: >-
                  Adyen sends this webhook when you successfully [update an
                  account
                  holder](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/accountHolders/_id_).
                operationId: post-balancePlatform.accountHolder.updated
                x-sortIndex: 2
                x-methodName: accountHolderUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-accountHolder-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.updated-balancePlatform-accountHolder-updated
                        balancePlatform-accountHolder-updated-lem-v3:
                          $ref: >-
                            #/components/examples/post-balancePlatform.accountHolder.updated-balancePlatform-accountHolder-updated-lem-v3
                      schema:
                        $ref: '#/components/schemas/AccountHolderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-accountHolder-updated:
                            $ref: '#/components/examples/WebhookAck'
                          balancePlatform-accountHolder-updated-lem-v3:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccount.created:
              post:
                tags:
                  - Balance account
                summary: Balance account created
                description: >-
                  Adyen sends this webhook when you successfully [create a
                  balance
                  account](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/balanceAccounts).
                operationId: post-balancePlatform.balanceAccount.created
                x-sortIndex: 1
                x-methodName: balanceAccountCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-balanceAccount-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccount.created-balancePlatform-balanceAccount-created
                      schema:
                        $ref: '#/components/schemas/BalanceAccountNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-balanceAccount-created:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccount.updated:
              post:
                tags:
                  - Balance account
                summary: Balance account updated
                description: >-
                  Adyen sends this webhook when you successfully [update a
                  balance
                  account](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/balanceAccounts/_id_).
                operationId: post-balancePlatform.balanceAccount.updated
                x-sortIndex: 2
                x-methodName: balanceAccountUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-balanceAccount-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccount.updated-balancePlatform-balanceAccount-updated
                      schema:
                        $ref: '#/components/schemas/BalanceAccountNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-balanceAccount-updated:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccountSweep.created:
              post:
                tags:
                  - Balance account
                summary: Sweep created
                description: >-
                  Adyen sends this webhook when you successfully [create a
                  sweep](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/balanceAccounts/_balanceAccountId_/sweeps).
                operationId: post-balancePlatform.balanceAccountSweep.created
                x-sortIndex: 3
                x-methodName: sweepCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-sweep-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccountSweep.created-balancePlatform-sweep-created
                      schema:
                        $ref: >-
                          #/components/schemas/SweepConfigurationNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-sweep-created:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccountSweep.deleted:
              post:
                tags:
                  - Balance account
                summary: Sweep deleted
                description: >-
                  Adyen sends this webhook when you successfully [delete a
                  sweep](https://docs.adyen.com/api-explorer/balanceplatform/latest/delete/balanceAccounts/_balanceAccountId_/sweeps/_sweepId_).
                operationId: post-balancePlatform.balanceAccountSweep.deleted
                x-sortIndex: 5
                x-methodName: sweepDeleted
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-sweep-deleted:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccountSweep.deleted-balancePlatform-sweep-deleted
                      schema:
                        $ref: >-
                          #/components/schemas/SweepConfigurationNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-sweep-deleted:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.balanceAccountSweep.updated:
              post:
                tags:
                  - Balance account
                summary: Sweep updated
                description: >-
                  Adyen sends this webhook when you successfully [update a
                  sweep](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/balanceAccounts/_balanceAccountId_/sweeps/_sweepId_).
                operationId: post-balancePlatform.balanceAccountSweep.updated
                x-sortIndex: 4
                x-methodName: sweepUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-sweep-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.balanceAccountSweep.updated-balancePlatform-sweep-updated
                      schema:
                        $ref: >-
                          #/components/schemas/SweepConfigurationNotificationRequest
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-sweep-updated:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.cardorder.created:
              post:
                tags:
                  - Card order
                summary: Card order created
                description: >-
                  Adyen sends this webhook to indicate a successful creation of
                  a card order after you create a [payment
                  instrument](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/paymentInstruments)
                  of `type` **card** and `formFactor` **physical**.
                operationId: post-balancePlatform.cardorder.created
                x-sortIndex: 1
                x-methodName: cardOrderCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/CardOrderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.cardorder.updated:
              post:
                tags:
                  - Card order
                summary: Card order updated
                description: >-
                  Adyen sends this webhook when there is an update in card order
                  status.
                operationId: post-balancePlatform.cardorder.updated
                x-sortIndex: 2
                x-methodName: cardOrderUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/CardOrderNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.paymentInstrument.created:
              post:
                tags:
                  - Payment instrument
                summary: Payment instrument created
                description: >-
                  Adyen sends this webhook when you successfully [create a
                  payment
                  instrument](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/paymentInstruments). 

                  >The webhook does not include the card number when creating
                  virtual cards. You can only get the card number in the
                  response of the POST
                  [/paymentInstruments](https://docs.adyen.com/api-explorer/balanceplatform/latest/post/paymentInstruments#responses-200-card-number)
                  request.
                operationId: post-balancePlatform.paymentInstrument.created
                x-sortIndex: 1
                x-methodName: paymentInstrumentCreated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-paymentInstrument-created:
                          $ref: >-
                            #/components/examples/post-balancePlatform.paymentInstrument.created-balancePlatform-paymentInstrument-created
                      schema:
                        $ref: '#/components/schemas/PaymentNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-paymentInstrument-created:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeeded.
            balancePlatform.paymentInstrument.updated:
              post:
                tags:
                  - Payment instrument
                summary: Payment instrument updated
                description: >-
                  Adyen sends this webhook when you successfully [update a
                  payment
                  instrument](https://docs.adyen.com/api-explorer/balanceplatform/latest/patch/paymentInstruments/_id_). 
                operationId: post-balancePlatform.paymentInstrument.updated
                x-sortIndex: 2
                x-methodName: paymentInstrumentUpdated
                security:
                  - BasicAuth: []
                requestBody:
                  content:
                    application/json:
                      examples:
                        balancePlatform-paymentInstrument-updated:
                          $ref: >-
                            #/components/examples/post-balancePlatform.paymentInstrument.updated-balancePlatform-paymentInstrument-updated
                      schema:
                        $ref: '#/components/schemas/PaymentNotificationRequest'
                responses:
                  '200':
                    content:
                      application/json:
                        examples:
                          balancePlatform-paymentInstrument-updated:
                            $ref: '#/components/examples/WebhookAck'
                        schema:
                          $ref: >-
                            #/components/schemas/BalancePlatformNotificationResponse
                    description: OK - the request has succeede
    overlays:
      - type: APIs.io Search
        url: overlays/configuration-webhooks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/configuration-webhooks-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-configuration-webhooks-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---