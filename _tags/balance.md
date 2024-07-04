---
name: Balance
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/balance.png
url: https://example.com/apis/balance.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Balance
apis:
  - name: Adyen Balance Control API
    description: >-
      The Balance Control API lets you transfer funds between merchant accounts
      that belong to the same legal entity and are under the same company
      account.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/BalanceControl/1/overview
    baseURL: https://cal-test.adyen.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/BalanceControl/1/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Balance Control API
          x-groups:
            - General
          tags:
            - name: General
          paths:
            /balanceTransfer:
              post:
                tags:
                  - Start
                  - Balance
                  - Transfers
                  - Transfers
                summary: Start a balance transfer
                description: >
                  Starts a balance transfer request between merchant accounts.
                  The following conditions must be met before you can
                  successfully transfer balances:


                  * The source and destination merchant accounts must be under
                  the same company account and legal entity.


                  * The source merchant account must have sufficient funds.


                  * The source and destination merchant accounts must have at
                  least one common processing currency.


                  When sending multiple API requests with the same source and
                  destination merchant accounts, send the requests sequentially
                  and *not* in parallel. Some requests may not be processed if 
    overlays:
      - type: APIs.io Search
        url: overlays/balance-control-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/balance-control-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-balance-control-api
  - name: Adyen Checkout API
    description: This is the description of your API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/Checkout/71/overview
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/Checkout/71/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Checkout API
          tags:
            - name: Payments
            - name: Donations
            - name: Payment Links
            - name: Modifications
            - name: Recurring
            - name: Orders
            - name: Utilities
            - name: Classic Checkout SDK
          paths:
            /applePay/sessions:
              post:
                tags:
                  - Get
                  - null
                  - Apple
                  - Pay
                  - Sessions
                  - Pay
                  - Sessions
                summary: Get an Apple Pay session
                description: >-
                  You need to use this endpoint if you have an API-only
                  integration with Apple Pay which uses Adyen's Apple Pay
                  certificate.


                  The endpoint returns the Apple Pay session data which you need
                  to complete the [Apple Pay session
                  validation](https://docs.adyen.com/payment-methods/apple-pay/api-only?tab=adyen-certificate-validation_1#complete-apple-pay-session-validation).
            /cancels:
              post:
                tags:
                  - Cancel
                  - null
                  - Authorised
                  - Payments
                  - Pay
                  - Sessions
                  - Cancels
                summary: Cancel an authorised payment
                description: >-
                  Cancels the authorisation on a payment that has not yet been
                  [captured](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/captures),
                  and returns a unique reference for this request. You get the
                  outcome of the request asynchronously, in a
                  [**TECHNICAL_CANCEL**
                  webhook](https://docs.adyen.com/online-payments/cancel#cancellation-webhook).


                  If you want to cancel a payment using the
                  [`pspReference`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments__resParam_pspReference),
                  use the
                  [`/payments/{paymentPspReference}/cancels`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/cancels)
                  endpoint instead.


                  If you want to cancel a payment but are not sure whether it
                  has been captured, use the
                  [`/payments/{paymentPspReference}/reversals`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/reversals)
                  endpoint instead.


                  For more information, refer to
                  [Cancel](https://docs.adyen.com/online-payments/cancel).
            /cardDetails:
              post:
                tags:
                  - Get
                  - The
                  - Lists
                  - Of
                  - Brands
                  - 'On'
                  - Cards
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                summary: Get the list of brands on the card
                description: >+
                  Send a request with at least the first 6 digits of the card
                  number to get a response with an array of brands on the card.
                  If you include [your supported
                  brands](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/cardDetails__reqParam_supportedBrands)
                  in the request, the response also tells you if you support
                  each [brand that was
                  identified](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/cardDetails__resParam_details).


                  If you have an API-only integration and collect card data, use
                  this endpoint to find out if the shopper's card is co-branded.
                  For co-branded cards, you must let the shopper choose the
                  brand to pay with  if you support both brands.

            /donations:
              post:
                tags:
                  - Start
                  - Transactions
                  - For
                  - Donations
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                summary: Start a transaction for donations
                description: >-
                  Takes in the donation token generated by the `/payments`
                  request and uses it to make the donation for the donation
                  account specified in the request.


                  For more information, see
                  [Donations](https://docs.adyen.com/online-payments/donations).
            /orders:
              post:
                tags:
                  - Create
                  - null
                  - Orders
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                summary: Create an order
                description: >-
                  Creates an order to be used for partial payments. Make a POST
                  `/orders` call before making a `/payments` call when
                  processing payments with different payment methods.
            /orders/cancel:
              post:
                tags:
                  - Cancel
                  - null
                  - Orders
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                summary: Cancel an order
                description: >-
                  Cancels an order. Cancellation of an order results in an
                  automatic rollback of all payments made in the order, either
                  by canceling or refunding the payment, depending on the type
                  of payment method.
            /originKeys:
              post:
                tags:
                  - Create
                  - Origin
                  - Keys
                  - Values
                  - For
                  - Domains
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                summary: Create originKey values for domains
                description: >-
                  This operation takes the origin domains and returns a JSON
                  object containing the corresponding origin keys for the
                  domains. 

                  > If you're still using origin key for your Web Drop-in or
                  Components integration, we recommend [switching to client
                  key](https://docs.adyen.com/development-resources/client-side-authentication/migrate-from-origin-key-to-client-key).
                  This allows you to use a single key for all origins, add or
                  remove origins without generating a new key, and detect the
                  card type from the number entered in your payment form. 
            /paymentLinks:
              post:
                tags:
                  - Create
                  - Payments
                  - Link
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                summary: Create a payment link
                description: >-
                  Creates a payment link to our hosted payment form where
                  shoppers can pay. The list of payment methods presented to the
                  shopper depends on the `currency` and `country` parameters
                  sent in the request.


                  For more information, refer to [Pay by Link
                  documentation](https://docs.adyen.com/online-payments/pay-by-link#create-payment-links-through-api).
            /paymentLinks/{linkId}:
              get:
                tags:
                  - Get
                  - Payments
                  - Link
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                summary: Get a payment link
                description: >-
                  Retrieves the payment link details using the payment link
                  `id`.
              patch:
                tags:
                  - Update
                  - The
                  - Status
                  - Of
                  - Payments
                  - Link
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                summary: Update the status of a payment link
                description: >-
                  Updates the status of a payment link. Use this endpoint to
                  [force the expiry of a payment
                  link](https://docs.adyen.com/online-payments/pay-by-link#update-payment-link-status).
            /paymentMethods:
              post:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Available
                  - Payments
                  - Methods
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                summary: Get a list of available payment methods
                description: >-
                  Queries the available payment methods for a transaction based
                  on the transaction context (like amount, country, and
                  currency). Besides giving back a list of the available payment
                  methods, the response also returns which input details you
                  need to collect from the shopper (to be submitted to
                  `/payments`).


                  Although we highly recommend using this endpoint to ensure you
                  are always offering the most up-to-date list of payment
                  methods, its usage is optional. You can, for example, also
                  cache the `/paymentMethods` response and update it once a
                  week.
            /paymentMethods/balance:
              post:
                tags:
                  - Get
                  - The
                  - Balance
                  - Of
                  - Gifts
                  - Cards
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                summary: Get the balance of a gift card
                description: >-
                  Retrieves the balance remaining on a shopper's gift card. To
                  check a gift card's balance, make a POST
                  `/paymentMethods/balance` call and include the gift card's
                  details inside a `paymentMethod` object.
            /paymentSession:
              post:
                tags:
                  - Create
                  - Payments
                  - Sessions
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                summary: Create a payment session
                description: >-
                  Provides the data object that can be used to start the
                  Checkout SDK. To set up the payment, pass its amount,
                  currency, and other required parameters. We use this to
                  optimise the payment flow and perform better risk assessment
                  of the transaction.


                  For more information, refer to [How it
                  works](https://docs.adyen.com/online-payments#howitworks).
            /payments:
              post:
                tags:
                  - Start
                  - Transactions
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                summary: Start a transaction
                description: >-
                  Sends payment parameters (like amount, country, and currency)
                  together with other required input details collected from the
                  shopper. To know more about required parameters for specific
                  payment methods, refer to our [payment method
                  guides](https://docs.adyen.com/payment-methods). 

                  The response depends on the [payment
                  flow](https://docs.adyen.com/payment-methods#payment-flow):

                  * For a direct flow, the response includes a `pspReference`
                  and a `resultCode` with the payment result, for example
                  **Authorised** or **Refused**. 

                  * For a redirect or additional action, the response contains
                  an `action` object. 
            /payments/details:
              post:
                tags:
                  - Submit
                  - Details
                  - For
                  - Payments
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                summary: Submit details for a payment
                description: >+
                  Submits details for a payment created using `/payments`. This
                  step is only needed when no final state has been reached on
                  the `/payments` request, for example when the shopper was
                  redirected to another page to complete the payment.

            /payments/result:
              post:
                tags:
                  - Verify
                  - Payments
                  - Results
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                summary: Verify a payment result
                description: >-
                  Verifies the payment result using the payload returned from
                  the Checkout SDK.


                  For more information, refer to [How it
                  works](https://docs.adyen.com/online-payments#howitworks).
            /payments/{paymentPspReference}/amountUpdates:
              post:
                tags:
                  - Update
                  - null
                  - Authorised
                  - Amount
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                summary: Update an authorised amount
                description: >-
                  Increases or decreases the authorised payment amount and
                  returns a unique reference for this request. You get the
                  outcome of the request asynchronously, in an
                  [**AUTHORISATION_ADJUSTMENT**
                  webhook](https://docs.adyen.com/development-resources/webhooks/understand-notifications#event-codes).


                  You can only update authorised amounts that have not yet been
                  [captured](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/captures).


                  The amount you specify in the request is the updated amount,
                  which is larger or smaller than the initial authorised amount.


                  For more information, refer to [Authorisation
                  adjustment](https://docs.adyen.com/online-payments/adjust-authorisation#use-cases).
            /payments/{paymentPspReference}/cancels:
              post:
                tags:
                  - Cancel
                  - null
                  - Authorised
                  - Payments
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                summary: Cancel an authorised payment
                description: >-
                  Cancels the authorisation on a payment that has not yet been
                  [captured](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/paymentPspReference/captures),
                  and returns a unique reference for this request. You get the
                  outcome of the request asynchronously, in a [**CANCELLATION**
                  webhook](https://docs.adyen.com/online-payments/cancel#cancellation-webhook).


                  If you want to cancel a payment but don't have the
                  [`pspReference`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments__resParam_pspReference),
                  use the
                  [`/cancels`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/cancels)
                  endpoint instead.


                  If you want to cancel a payment but are not sure whether it
                  has been captured, use the
                  [`/payments/{paymentPspReference}/reversals`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/reversals)
                  endpoint instead.


                  For more information, refer to
                  [Cancel](https://docs.adyen.com/online-payments/cancel).
            /payments/{paymentPspReference}/captures:
              post:
                tags:
                  - Capture
                  - null
                  - Authorised
                  - Payments
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                summary: Capture an authorised payment
                description: >2-
                   Captures an authorised payment and returns a unique reference for this request. You get the outcome of the request asynchronously, in a [**CAPTURE** webhook](https://docs.adyen.com/online-payments/capture#capture-notification).

                  You can capture either the full authorised amount or a part of
                  the authorised amount. By default, any unclaimed amount after
                  a partial capture gets cancelled. This does not apply if you
                  enabled multiple partial captures on your account and the
                  payment method supports multiple partial captures. 


                  [Automatic
                  capture](https://docs.adyen.com/online-payments/capture#automatic-capture)
                  is the default setting for most payment methods. In these
                  cases, you don't need to make capture requests. However,
                  making capture requests for payments that are captured
                  automatically does not result in double charges.


                  For more information, refer to
                  [Capture](https://docs.adyen.com/online-payments/capture).
            /payments/{paymentPspReference}/refunds:
              post:
                tags:
                  - Refunds
                  - Captured
                  - Payments
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                  - Refunds
                summary: Refund a captured payment
                description: >-
                  Refunds a payment that has been
                  [captured](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/captures),
                  and returns a unique reference for this request. You get the
                  outcome of the request asynchronously, in a [**REFUND**
                  webhook](https://docs.adyen.com/online-payments/refund#refund-webhook).


                  You can refund either the full captured amount or a part of
                  the captured amount. You can also perform multiple partial
                  refunds, as long as their sum doesn't exceed the captured
                  amount.


                  > Some payment methods do not support partial refunds. To
                  learn if a payment method supports partial refunds, refer to
                  the payment method page such as
                  [cards](https://docs.adyen.com/payment-methods/cards#supported-cards),
                  [iDEAL](https://docs.adyen.com/payment-methods/ideal), or
                  [Klarna](https://docs.adyen.com/payment-methods/klarna). 


                  If you want to refund a payment but are not sure whether it
                  has been captured, use the
                  [`/payments/{paymentPspReference}/reversals`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/reversals)
                  endpoint instead.


                  For more information, refer to
                  [Refund](https://docs.adyen.com/online-payments/refund).
            /payments/{paymentPspReference}/reversals:
              post:
                tags:
                  - Refunds
                  - Or
                  - Cancel
                  - Payments
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                  - Refunds
                  - Reversals
                summary: Refund or cancel a payment
                description: >-
                  [Refunds](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/refunds)
                  a payment if it has already been captured, and
                  [cancels](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/payments/{paymentPspReference}/cancels)
                  a payment if it has not yet been captured. Returns a unique
                  reference for this request. You get the outcome of the request
                  asynchronously, in a [**CANCEL_OR_REFUND**
                  webhook](https://docs.adyen.com/online-payments/reverse#cancel-or-refund-webhook).


                  The reversed amount is always the full payment amount.

                  > Do not use this request for payments that involve multiple
                  partial captures.


                  For more information, refer to
                  [Reversal](https://docs.adyen.com/online-payments/reversal).
            /sessions:
              post:
                tags:
                  - Create
                  - Payments
                  - Sessions
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                  - Refunds
                  - Reversals
                summary: Create a payment session
                description: >-
                  Creates a payment session for [Web
                  Drop-in](https://docs.adyen.com/online-payments/web-drop-in)
                  and [Web
                  Components](https://docs.adyen.com/online-payments/web-components)
                  integrations.


                  The response contains encrypted payment session data. The
                  front end then uses the session data to make any required
                  server-side calls for the payment flow.


                  You get the payment outcome asynchronously, in an
                  [AUTHORISATION](https://docs.adyen.com/api-explorer/#/Webhooks/latest/post/AUTHORISATION)
                  webhook.
            /sessions/{sessionId}:
              get:
                tags:
                  - Get
                  - The
                  - Results
                  - Of
                  - Payments
                  - Sessions
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                  - Refunds
                  - Reversals
                summary: Get the result of a payment session
                description: >-
                  Returns the status of the payment session with the `sessionId`
                  and `sessionResult` specified in the path.
            /storedPaymentMethods:
              get:
                tags:
                  - Get
                  - Tokens
                  - For
                  - Stored
                  - Payments
                  - Details
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                  - Refunds
                  - Reversals
                  - Payments
                summary: Get tokens for stored payment details
                description: >+
                  Lists the tokens for stored payment details for the shopper
                  identified in the path, if there are any available. The token
                  ID can be used with payment requests for the shopper's
                  payment. A summary of the stored details is included.

            /storedPaymentMethods/{storedPaymentMethodId}:
              delete:
                tags:
                  - Delete
                  - Tokens
                  - For
                  - Stored
                  - Payments
                  - Details
                  - Pay
                  - Sessions
                  - Cancels
                  - Details
                  - Donations
                  - Orders
                  - Cancel
                  - Keys
                  - Links
                  - Link
                  - Identifiers
                  - Methods
                  - Balance
                  - Sessions
                  - Payments
                  - Results
                  - Psp
                  - References
                  - Amount
                  - Updates
                  - Captures
                  - Refunds
                  - Reversals
                  - Payments
                  - Stored
                  - Methods
                summary: Delete a token for stored payment details
                description: Deletes the token identified in the path. The token can no lo
    overlays:
      - type: APIs.io Search
        url: overlays/checkout-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/checkout-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-checkout-api
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
  - name: Adyen Terminal API
    description: >-
      The Adyen Terminal API lets you make payments, issue refunds, collect
      shopper information, and perform other shopper-terminal interactions using
      a payment terminal supplied by Adyen.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/point-of-sale/design-your-integration/terminal-api/terminal-api-reference/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/point-of-sale/design-your-integration/terminal-api/terminal-api-reference/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Adyen Terminal API
          paths:
            /login:
              post:
                description: >-
                  It conveys Information related to the session (period between
                  a Login and the following Logout) to process. Content of the
                  Login Request message.
                summary: Login Request
                tags:
                  - Login
                  - Request
                  - Login
            /logout:
              post:
                description: Empty. Content of the Logout Request message.
                summary: Logout Request
                tags:
                  - Logout
                  - Request
                  - Login
                  - Logout
            /enableservice:
              post:
                description: >-
                  It conveys the services that will be enabled for the  POI
                  Terminal without the request of the Sale System, and a
                  possible invitation for the Customer to start the services.
                  Content of the Enable Service Request message.
                summary: EnableService Request
                tags:
                  - Enable
                  - Services
                  - Request
                  - Login
                  - Logout
                  - Enable Service
            /admin:
              post:
                description: Empty. Content of the Custom Admin Request message.
                summary: Admin Request
                tags:
                  - Administrative
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
            /payment:
              post:
                description: >-
                  Request sent to terminal to initiate payment.  It conveys
                  Information related to the Payment transaction to process.
                  Content of the Payment Request message.
                summary: Payment Request
                tags:
                  - Payments
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
            /cardacquisition:
              post:
                description: >-
                  It conveys Information related to the payment and loyalty
                  cards to read and analyse. This message pair is usually
                  followed by a message pair (e.g. payment or loyalty) which
                  refers to this Card Acquisition message pair. Content of the
                  Card Acquisition Request message.
                summary: CardAcquisition Request
                tags:
                  - Cards
                  - Acquisition
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
            /loyalty:
              post:
                description: >-
                  It conveys Information related to the Loyalty transaction to
                  process. Content of the Loyalty Request message.
                summary: Loyalty Request
                tags:
                  - Loyalty
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
            /storedvalue:
              post:
                description: >-
                  It conveys Information related to the Stored Value transaction
                  to process. Content of the Stored Value Request message.
                summary: StoredValue Request
                tags:
                  - Stored
                  - Value
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
            /reversal:
              post:
                description: >-
                  It conveys Information related to the reversal of a previous
                  payment or a loyalty transaction. Content of the Reversal
                  Request message.
                summary: Reversal Request
                tags:
                  - Reversals
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
            /reconciliation:
              post:
                description: >-
                  It conveys Information related to the Reconciliation requested
                  by the Sale System. Content of the Reconciliation Request
                  message.
                summary: Reconciliation Request
                tags:
                  - Reconciliation
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
            /gettotals:
              post:
                description: >-
                  It conveys information from the Sale System related to the
                  scope and the format of the totals to be computed by the POI
                  System. Content of the Get Totals Request message.
                summary: GetTotals Request
                tags:
                  - Get
                  - Totals
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
            /balanceinquiry:
              post:
                description: >-
                  It conveys Information related to the account for which a
                  Balance Inquiry is requested. Content of the Balance Inquiry
                  Request message.
                summary: BalanceInquiry Request
                tags:
                  - Balance
                  - Inquiries
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
            /transactionstatus:
              post:
                description: >-
                  It conveys Information requested for status of the last or
                  current Payment, Loyalty or Reversal transaction. Content of
                  the TransactionStatus Request message.
                summary: TransactionStatus Request
                tags:
                  - Transactions
                  - Status
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
            /diagnosis:
              post:
                description: >-
                  It conveys Information related to the target POI for which the
                  diagnosis is requested. Content of the Diagnosis Request
                  message.
                summary: Diagnosis Request
                tags:
                  - Diagnosis
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
            /display:
              post:
                description: >-
                  It conveys the data to display and the way to process the
                  display. It contains the complete content to display. It might
                  contain an operation (the DisplayOutput element) per Display
                  Device type. Content of the Display Request message.
                summary: Display Request
                tags:
                  - Display
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
            /input:
              post:
                description: >-
                  It conveys data to display and the way to process the display,
                  and contains the complete content to display. In addition to
                  the display on the Input Device, it might contain an operation
                  (the DisplayOutput element) per Display Device type. Content
                  of the Input Request message.
                summary: Input Request
                tags:
                  - Inputs
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
            /print:
              post:
                description: >-
                  It conveys the data to print and the way to process the print.
                  It contains the complete content to print. Content of the
                  Print Request message.
                summary: Print Request
                tags:
                  - Print
                  - Request
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
                  - Print
            /cardreaderapdu:
              post:
                description: >-
                  It contains the APDU request to send to the chip of the card,
                  and a possible invitation message to display on the
                  CashierInterface or the CustomerInterface. Content of the Card
                  Reader APDU Request message.
                summary: CardReaderAPDU Reque
                tags:
                  - Cards
                  - Readers
                  - Reque
                  - Login
                  - Logout
                  - Enable Service
                  - Administrative
                  - Payments
                  - Card Acquisitions
                  - Loyalty
                  - Stored Values
                  - Reversals
                  - Reconciliation
                  - Gettotals
                  - Balance Inquiry
                  - Transaction Status
                  - Diagnosis
                  - Display
                  - Inputs
                  - Print
                  - Card Reader Applications
    overlays:
      - type: APIs.io Search
        url: overlays/terminal-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/terminal-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-terminal-api
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
  - name: FactSet Fundamentals Report Builder API
    description: >-
      Report Builder APIs return data in relational structures and with industry
      handling to provide the most relevant financial data in a
      presentation-ready format.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/factset-fundamentals-report-builder-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-report-builder-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-report-builder-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-report-builder-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-report-builder-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-fundamentals-report-builder-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: FactSet Fundamentals Report Builder
            description: ''
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: Read more about STACH 2.0's row organized schema
            url: https://factset.github.io/stachschema/#/v2/RowOrganized
          tags:
            - name: Financials
          paths:
            /income-statement:
              get:
                tags:
                  - Income
                  - Statement
                  - Income
                  - Statement
                summary: Income Statement
                description: Returns a standardized Income Statement based on industry.
            /balance-sheet:
              get:
                tags:
                  - Balance
                  - Sheet
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                summary: Balance Sheet
                description: Returns a standardized Balance Sheet based on industry.
            /cash-flow:
              get:
                tags:
                  - Cash
                  - Flow
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                summary: Cash Flow
                description: Returns a standardized Cash Fl
    overlays:
      - type: APIs.io Search
        url: overlays/fundamentals-report-builder-openapi-original.yml
      - type: APIs.io Search
        url: overlays/fundamentals-report-builder-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/fundamentals-report-builder-openapi-api-evangelist-ratings.yml
    aid: factset:factset-fundamentals-report-builder-api
  - name: FactSet Estimates Report Builder API
    description: >-
      The FactSet Estimates Report Builder APIs return consensus estimate data
      with fiscal periods and line items structured in a presentation-ready
      format.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/factset-estimates-report-builder-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-estimates-report-builder-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: FactSet Estimates Report Builder
            description: ''
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: Read more about STACH 2.0's row organized schema
            url: https://factset.github.io/stachschema/#/v2/RowOrganized
          tags:
            - name: All Estimates
            - name: Estimate Tables
          paths:
            /income-statement:
              get:
                tags:
                  - Income
                  - Statement
                  - Income
                  - Statement
                summary: Income Statement
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Income Statement line items.
            /balance-sheet:
              get:
                tags:
                  - Balance
                  - Sheet
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                summary: Balance Sheet
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Balance Sheet line items.
            /cash-flow:
              get:
                tags:
                  - Cash
                  - Flow
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                summary: Cash Flow
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Cash Flow line items.
            /per-share:
              get:
                tags:
                  - Per
                  - Share
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                summary: Per Share
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for Per Share line items.
            /industry-metrics:
              get:
                tags:
                  - Industry
                  - Metrics
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                summary: Industry Metrics
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for industry-specific metrics.
            /product-segments:
              get:
                tags:
                  - Product
                  - Segments
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                summary: Product Segments
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for line items broken down by product
                  and business.
            /geographic-segments:
              get:
                tags:
                  - Geographic
                  - Segments
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                  - Geographic
                summary: Geographic Segments
                description: >-
                  Returns historical and future period broker estimate consensus
                  in a statement format for line items broken down
                  geographically.
            /valuation:
              get:
                tags:
                  - Valuation
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                  - Geographic
                  - Valuation
                summary: Valuation
                description: >-
                  Returns valuation ratios in a statement format calculated from
                  historical and future period broker estimate consensus.
            /table:
              get:
                tags:
                  - Interim/
                  - Annual
                  - Estimate
                  - Table
                  - Income
                  - Statement
                  - Balance
                  - Sheet
                  - Cash
                  - Flow
                  - Per
                  - Share
                  - Industry
                  - Metrics
                  - Product
                  - Segments
                  - Geographic
                  - Valuation
                  - Table
                summary: Interim/Annual Estimate Table
                description: Returns a timeseries grid of Interim and Annual data
    overlays:
      - type: APIs.io Search
        url: overlays/estimates-report-builder-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/estimates-report-builder-openapi-api-evangelist-ratings.yml
    aid: factset:factset-estimates-report-builder-api
  - aid: stripe:stripe-balance-api
    name: Stripe Balance API
    description: >-
      This is an object representing your Stripe balance. You can retrieve it to
      see the balance currently on your Stripe account. You can also retrieve
      the balance history, which contains a list of transactions that
      contributed to the balance (charges, payouts, and so forth).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/api/balance
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/api/balance
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Balance API
          paths:
            /v1/balance:
              get:
                description: >-
                  <p>Retrieves the current account balance, based on the
                  authentication that was used to make the request.
                   For a sample request, see <a href="/docs/connect/account-balances#accounting-for-negative-balances">Accounting for negative balances</a>.</p>
                tags:
                  - V1
                  - Balance
            /v1/balance/history:
              get:
                description: >-
                  <p>Returns a list of transactions that have contributed to the
                  Stripe account balance (e.g., charges, transfers, and so
                  forth). The transactions are returned in sorted order, with
                  the most recent transactions appearing first.</p>


                  <p>Note that this endpoint was previously called “Balance
                  history” and used the path
                  <code>/v1/balance/history</code>.</p>
                tags:
                  - V1
                  - Balance
                  - History
            /v1/balance/history/{id}:
              get:
                description: >-
                  <p>Retrieves the balance transaction with the given ID.</p>


                  <p>Note that this endpoint previously used the path
                  <code>/v1/balance/history/:id</code>.</p>
                tags:
                  - V1
                  - Balance
                  - History
                  - Id
            /v1/balance_transactions:
              get:
                description: >-
                  <p>Returns a list of transactions that have contributed to the
                  Stripe account balance (e.g., charges, transfers, and so
                  forth). The transactions are returned in sorted order, with
                  the most recent transactions appearing first.</p>


                  <p>Note that this endpoint was previously called “Balance
                  history” and used the path
                  <code>/v1/balance/history</code>.</p>
                tags:
                  - V1
                  - Balance
                  - History
                  - Id
                  - Balance_transactions
            /v1/balance_transactions/{id}:
              get:
                description: >-
                  <p>Retrieves the balance transaction with the given ID.</p>


                  <p>Note that this endpoint previously used the path
                  <code>/v1/balance/history/:id</
                tags:
                  - V1
                  - Balance
                  - History
                  - Id
                  - Balance_transactio
    overlays:
      - type: APIs.io Search
        url: overlays/balance-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/balance-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---