---
name: Contracts
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/contracts.png
url: https://example.com/apis/contracts.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Contracts
apis:
  - name: Adyen Recurring API
    description: >-
      The Recurring APIs allow you to manage and remove your tokens or saved
      payment details. Tokens should be created with validation during a payment
      request. For more information, refer to our [Tokenization
      documentation](https://docs.adyen.com/online-payments/tokenization).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/online-payments/tokenization
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/online-payments/tokenization
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Recurring API
          tags:
            - name: General
          paths:
            /createPermit:
              post:
                tags:
                  - Create
                  - New
                  - Permits
                  - Linked
                  - To
                  - Recurring
                  - Contracts
                  - Permits
                summary: Create new permits linked to a recurring contract.
                description: >-
                  Create permits for a recurring contract, including support for
                  defining restrictions.
            /disable:
              post:
                tags:
                  - Disable
                  - Stored
                  - Payments
                  - Details
                  - Permits
                  - Disable
                summary: Disable stored payment details
                description: >-
                  Disables stored payment details to stop charging a shopper
                  with this particular recurring detail ID.


                  For more information, refer to [Disable stored
                  details](https://docs.adyen.com/classic-integration/recurring-payments/disable-stored-details/).
            /disablePermit:
              post:
                tags:
                  - Disable
                  - null
                  - Existing
                  - Permits
                  - Permits
                  - Disable
                summary: Disable an existing permit.
                description: >-
                  Disable a permit that was previously linked to a
                  recurringDetailReference.
            /listRecurringDetails:
              post:
                tags:
                  - Get
                  - Stored
                  - Payments
                  - Details
                  - Permits
                  - Disable
                  - Recurring
                  - Details
                summary: Get stored payment details
                description: >-
                  Lists the stored payment details for a shopper, if there are
                  any available. The recurring detail ID can be used with a
                  regular authorisation request to charge the shopper. A summary
                  of the payment detail is returned for presentation to the
                  shopper.


                  For more information, refer to [Retrieve stored
                  details](https://docs.adyen.com/classic-integration/recurring-payments/retrieve-stored-details/).
            /notifyShopper:
              post:
                tags:
                  - Ask
                  - Issuer
                  - To
                  - Notify
                  - The
                  - Shopper
                  - Permits
                  - Disable
                  - Recurring
                  - Details
                  - Shopper
                summary: Ask issuer to notify the shopper
                description: >-
                  Sends a request to the issuer so they can inform the shopper
                  about the upcoming recurring payment. This endpoint is used
                  only for local acquiring in India. For more information, refer
                  to [Recurring card payments in
                  India](https://docs.adyen.com/payment-methods/cards/cards-recurring-india).
            /scheduleAccountUpdater:
              post:
                tags:
                  - Schedules
                  - Running
                  - The
                  - Account
                  - Updater
                  - Permits
                  - Disable
                  - Recurring
                  - Details
                  - Shopper
                  - Account
                  - Updater
                summary: Schedule running the Account Updater
                description: >-
                  When making the API call, you can submit either the credit
                  card information, or the recurring detail reference and the
                  shopper reference:

                  * If the card information is provided, all the sub-fields for
                  `card` are mandatory.

                  * If the recurring detail reference is provided, the fields
                  for `shopperReference` and `selectedRecurr
    overlays:
      - type: APIs.io Search
        url: overlays/recurring-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/recurring-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-recurring-api
  - name: managedblockchain-query
    description: >-
      <p>Amazon Managed Blockchain (AMB) Query provides you with convenient
      access to multi-blockchain network data, which makes it easier for you to
      extract contextual data related to blockchain activity. You can use AMB
      Query to read data from public blockchain networks, such as Bitcoin
      Mainnet and Ethereum Mainnet. You can also get information such as the
      current and historical balances of addresses, or you can get a list of
      blockchain transactions for a given time period. Additionally, you can get
      details of a given transaction, such as transaction events, which you can
      further analyze or use in business logic for your applications.</p>
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
            title: managedblockchain-query
          paths:
            /batch-get-token-balance:
              POST:
                summary: BatchGetTokenBalance
                description: >-
                  <p>Gets the token balance for a batch of tokens by using the
                  <code>BatchGetTokenBalance</code> action for every token in
                  the request.</p> <note> <p>Only the native tokens BTC and ETH,
                  and the ERC-20, ERC-721, and ERC 1155 token standards are
                  supported.</p> </note>
                tags:
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Batches
                  - Get
                  - Tokens
                  - Balance
            /get-asset-contract:
              POST:
                summary: GetAssetContract
                description: >-
                  <p>Gets the information about a specific contract deployed on
                  the blockchain.</p> <note> <ul> <li> <p>The Bitcoin blockchain
                  networks do not support this operation.</p> </li> <li>
                  <p>Metadata is currently only available for some
                  <code>ERC-20</code> contracts. Metadata will be available for
                  additional contracts in the future.</p> </li> </ul> </note>
                tags:
                  - Get
                  - Assets
                  - Contracts
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
            /get-token-balance:
              POST:
                summary: GetTokenBalance
                description: >-
                  <p>Gets the balance of a specific token, including native
                  tokens, for a given address (wallet or contract) on the
                  blockchain.</p> <note> <p>Only the native tokens BTC and ETH,
                  and the ERC-20, ERC-721, and ERC 1155 token standards are
                  supported.</p> </note>
                tags:
                  - Get
                  - Tokens
                  - Balance
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
            /get-transaction:
              POST:
                summary: GetTransaction
                description: >-
                  <p>Gets the details of a transaction.</p> <note> <p>This
                  action will return transaction details for all transactions
                  that are <i>confirmed</i> on the blockchain, even if they have
                  not reached <a
                  href="https://docs.aws.amazon.com/managed-blockchain/latest/ambq-dg/key-concepts.html#finality">finality</a>.
                  </p> </note>
                tags:
                  - Get
                  - Transactions
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
                  - Transactions
            /list-asset-contracts:
              POST:
                summary: ListAssetContracts
                description: >-
                  <p>Lists all the contracts for a given contract type deployed
                  by an address (either a contract address or a wallet
                  address).</p> <p>The Bitcoin blockchain networks do not
                  support this operation.</p>
                tags:
                  - Lists
                  - Assets
                  - Contracts
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
                  - Transactions
                  - Lists
                  - Contracts
            /list-token-balances:
              POST:
                summary: ListTokenBalances
                description: >-
                  <p>This action returns the following for a given blockchain
                  network:</p> <ul> <li> <p>Lists all token balances owned by an
                  address (either a contract address or a wallet address).</p>
                  </li> <li> <p>Lists all token balances for all tokens created
                  by a contract.</p> </li> <li> <p>Lists all token balances for
                  a given token.</p> </li> </ul> <note> <p>You must always
                  specify the network property of the <code>tokenFilter</code>
                  when using this operation.</p> </note>
                tags:
                  - Lists
                  - Tokens
                  - Balances
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
                  - Transactions
                  - Lists
                  - Contracts
                  - Balances
            /list-transaction-events:
              POST:
                summary: ListTransactionEvents
                description: >-
                  <p>An array of <code>TransactionEvent</code> objects. Each
                  object contains details about the transaction event.</p>
                  <note> <p>This action will return transaction details for all
                  transactions that are <i>confirmed</i> on the blockchain, even
                  if they have not reached <a
                  href="https://docs.aws.amazon.com/managed-blockchain/latest/ambq-dg/key-concepts.html#finality">finality</a>.
                  </p> </note>
                tags:
                  - Lists
                  - Transactions
                  - Events
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
                  - Transactions
                  - Lists
                  - Contracts
                  - Balances
                  - Events
            /list-transactions:
              POST:
                summary: ListTransactions
                description: >-
                  <p>Lists all of the transactions on a given wallet address or
                  to a specific con
                tags:
                  - Lists
                  - Transactions
                  - Batches
                  - Get
                  - Tokens
                  - Balance
                  - Assets
                  - Contracts
                  - Transactions
                  - Lists
                  - Contracts
                  - Balances
                  - Events
                  - Transactions
    overlays:
      - type: APIs.io Search
        url: overlays/managedblockchain-query-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/managedblockchain-query-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:managedblockchain-query
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---