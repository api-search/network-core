---
name: Balances
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/balances.png
url: https://example.com/apis/balances.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Balances
apis:
  - name: Adyen Funds API
    description: >-
      The Fund API provides endpoints for managing the funds in the accounts on
      your platform. These management operations include, for example, the
      transfer of funds from one account to another, the payout of funds to an
      account holder, and the retrieval of balances in an account.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/marketplaces-and-platforms/classic/fund-transfer/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/classic/fund-transfer/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Fund API
            x-timestamp: '2023-05-30T15:27:19Z'
          x-groups:
            - General
            - Migration
          tags:
            - name: General
          paths:
            /accountHolderBalance:
              post:
                tags:
                  - Get
                  - The
                  - Balances
                  - Of
                  - null
                  - Account
                  - Holders
                  - Holders
                  - Balance
                summary: Get the balances of an account holder
                description: >-
                  Returns the account balances of an account holder. An
                  account's balances are organized according by currencies. This
                  mean that an account may have multiple balances: one for each
                  currency.
            /accountHolderTransactionList:
              post:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Transactions
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                summary: Get a list of transactions
                description: >-
                  Returns a list of transactions for an account holder's
                  accounts. You can specify the accounts and transaction
                  statuses to be included on the list. The call returns a
                  maximum of 50 transactions for each account. To retrieve all
                  transactions, you must make another call with the 'page' value
                  incremented. Transactions are listed in chronological order,
                  with the most recent transaction first.
            /debitAccountHolder:
              post:
                tags:
                  - Send
                  - Direct
                  - Debit
                  - Request
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                  - Account
                summary: Send a direct debit request
                description: >-
                  Sends a direct debit request to an account holder's bank
                  account. If the direct debit is successful, the funds are
                  settled in the accounts specified in the split instructions.
                  Adyen sends the result of the direct debit in a
                  [`DIRECT_DEBIT_INITIATED`](https://docs.adyen.com/api-explorer/#/NotificationService/latest/post/DIRECT_DEBIT_INITIATED)
                  notification webhook.

                   To learn more about direct debits, see [Top up accounts](https://docs.adyen.com/marketplaces-and-platforms/classic/top-up-accounts).
            /payoutAccountHolder:
              post:
                tags:
                  - Pay
                  - Out
                  - From
                  - null
                  - Account
                  - To
                  - The
                  - Holders
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                  - Account
                summary: Pay out from an account to the account holder
                description: >-
                  Pays out a specified amount from an account to the bank
                  account of account holder.
            /refundFundsTransfer:
              post:
                tags:
                  - Refunds
                  - Funds
                  - Transfers
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                  - Account
                  - Funds
                  - Transfers
                summary: Refund a funds transfer
                description: >-
                  Refunds funds transferred from one account to another. Both
                  accounts must be in the same platform, but can have different
                  account holders. 
            /refundNotPaidOutTransfers:
              post:
                tags:
                  - Refunds
                  - All
                  - Transactions
                  - Of
                  - null
                  - Account
                  - Since
                  - The
                  - Most
                  - Recent
                  - Payouts
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                  - Account
                  - Funds
                  - Transfers
                  - Not
                  - Paid
                  - Out
                  - Transfers
                summary: >-
                  Refund all transactions of an account since the most recent
                  payout
                description: >-
                  Refunds all the transactions of an account that have taken
                  place since the most recent payout. This request is on a
                  account basis (as opposed to a payment basis), so only the
                  portion of the payment that was made to the specified account
                  is refunded. The commissions, fees, and payments to other
                  accounts remain in the accounts to which they were sent as
                  designated by the original payment's split details.
            /setupBeneficiary:
              post:
                tags:
                  - Designate
                  - Beneficiary
                  - Account
                  - And
                  - Transfers
                  - The
                  - Benefactor's
                  - Current
                  - Balance
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                  - Account
                  - Funds
                  - Transfers
                  - Not
                  - Paid
                  - Out
                  - Transfers
                  - Beneficiary
                summary: >-
                  Designate a beneficiary account and transfer the benefactor's
                  current balance
                description: >-
                  Defines a benefactor and a beneficiary relationship between
                  two accounts. At the time of benefactor/beneficiary setup, the
                  funds in the benefactor account are transferred to the
                  beneficiary account, and any further payments to the
                  benefactor account are automatically sent to the beneficiary
                  account. A series of benefactor/beneficiaries may not exceed
                  four beneficiaries and may not have a cycle in it.
            /transferFunds:
              post:
                tags:
                  - Transfers
                  - Funds
                  - Between
                  - Platforms
                  - Accounts
                  - Holders
                  - Balance
                  - Transactions
                  - Lists
                  - Account
                  - Funds
                  - Transfers
                  - Not
                  - Paid
                  - Out
                  - Transfers
                  - Beneficiary
                summary: Transfer funds between platform accounts
                description: >-
                  Transfers funds from one account to another account. Both
                  accounts must be in the same platform, but can have different
                  account holders. The transfer must include a transfer code,
                  which should be determined by the platform, in 
    overlays:
      - type: APIs.io Search
        url: overlays/funds-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/funds-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-funds-api
  - name: Adyen Stored Value API
    description: A set of API endpoints to manage stored value products.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/payment-methods/gift-cards/stored-value-api/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/payment-methods/gift-cards/stored-value-api/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Stored Value API
          x-groups:
            - General
          tags:
            - name: General
          paths:
            /changeStatus:
              post:
                tags:
                  - Changes
                  - The
                  - Status
                  - Of
                  - Payments
                  - Methods
                  - Status
                summary: Changes the status of the payment method.
                description: >-
                  Changes the status of the provided payment method to the
                  specified status.
            /checkBalance:
              post:
                tags:
                  - Checks
                  - The
                  - Balances
                  - Status
                  - Balance
                summary: Checks the balance.
                description: Checks the balance of the provided payment method.
            /issue:
              post:
                tags:
                  - Issues
                  - New
                  - Cards
                  - Status
                  - Balance
                  - Issues
                summary: Issues a new card.
                description: Issues a new card of the given payment method.
            /load:
              post:
                tags:
                  - Loads
                  - The
                  - Payments
                  - Methods
                  - Status
                  - Balance
                  - Issues
                  - Load
                summary: Loads the payment method.
                description: Loads the payment method with the specified funds.
            /mergeBalance:
              post:
                tags:
                  - Merge
                  - The
                  - Balance
                  - Of
                  - Two
                  - Cards
                  - Status
                  - Balance
                  - Issues
                  - Load
                summary: Merge the balance of two cards.
                description: >-
                  Increases the balance of the paymentmethod by the full amount
                  left on the source paymentmethod
            /voidTransaction:
              post:
                tags:
                  - Voids
                  - Transactions
                  - Status
                  - Balance
                  - Issues
                  - Load
                  - Transactions
                summary: Voids a transaction.
                description: Voids the
    overlays:
      - type: APIs.io Search
        url: overlays/stored-value-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/stored-value-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-stored-value-api
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