---
name: Benefactors
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/benefactors.png
url: https://example.com/apis/benefactors.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Benefactors
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---