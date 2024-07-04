---
name: Accountholders
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/accountholders.png
url: https://example.com/apis/accountholders.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Accountholders
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
            - name: Card orders
            - name: Transfer routes
          paths:
            /accountHolders:
              post:
                tags:
                  - Create
                  - An
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
                  - An
                  - Account
                  - Holders
                  - Holders
                  - Identifiers
                summary: Get an account holder
                description: Returns an account holder.
              patch:
                tags:
                  - Update
                  - An
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
                  - An
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---