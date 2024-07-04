---
name: Capture
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/capture.png
url: https://example.com/apis/capture.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Capture
apis:
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
  - name: Adyen Payments API
    description: >-
      A set of API endpoints that allow you to initiate, settle, and modify
      payments on the Adyen payments platform. You can use the API to accept
      card payments (including One-Click and 3D Secure), bank transfers,
      ewallets, and many other payment methods.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/online-payments/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/online-payments/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Payment API
          tags:
            - name: Payments
            - name: Modifications
          paths:
            /adjustAuthorisation:
              post:
                tags:
                  - Change
                  - The
                  - Authorised
                  - Amount
                  - Authorization
                summary: Change the authorised amount
                description: >-
                  Allows you to increase or decrease the authorised amount after
                  the initial authorisation has taken place. This functionality
                  enables for example tipping, improving the chances your
                  authorisation will be valid, or charging the shopper when they
                  have already left the merchant premises.


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).

                  > If you have a [newer
                  integration](https://docs.adyen.com/online-payments), and are
                  doing:

                  > * [Asynchronous
                  adjustments](https://docs.adyen.com/online-payments/adjust-authorisation#asynchronous-or-synchronous-adjustment),
                  use the
                  [`/payments/{paymentPspReference}/amountUpdates`](https://docs.adyen.com/api-explorer/#/CheckoutService/v67/post/payments/{paymentPspReference}/amountUpdates)
                  endpoint on Checkout API.

                  > * [Synchronous
                  adjustments](https://docs.adyen.com/online-payments/adjust-authorisation#asynchronous-or-synchronous-adjustment),
                  use this endpoint.
            /authorise:
              post:
                tags:
                  - Create
                  - null
                  - Authorization
                  - Authorization
                  - Authorization
                summary: Create an authorisation
                description: >-
                  Creates a payment with a unique reference (`pspReference`) and
                  attempts to obtain an authorisation hold. For cards, this
                  amount can be captured or cancelled later. Non-card payment
                  methods typically don't support this and will automatically
                  capture as part of the authorisation.

                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments`](https://docs.adyen.com/api-explorer/#/CheckoutService/payments)
                  endpoint under Checkout API instead.
            /authorise3d:
              post:
                tags:
                  - Complete
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                summary: Complete a 3DS authorisation
                description: >-
                  For an authenticated 3D Secure session, completes the payment
                  authorisation. This endpoint must receive the `md` and
                  `paResponse` parameters that you get from the card issuer
                  after a shopper pays via 3D Secure.


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce/3d-secure).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments/details`](https://docs.adyen.com/api-explorer/#/CheckoutService/payments/details)
                  endpoint under Checkout API instead.
            /authorise3ds2:
              post:
                tags:
                  - Complete
                  - S2
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                summary: Complete a 3DS2 authorisation
                description: >-
                  For an authenticated 3D Secure 2 session, completes the
                  payment authorisation. This endpoint must receive the
                  `threeDS2Token` and `threeDS2Result` parameters.


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce/3d-secure).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments/details`](https://docs.adyen.com/api-explorer/#/CheckoutService/payments/details)
                  endpoint under Checkout API instead.
            /cancel:
              post:
                tags:
                  - Cancel
                  - null
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                summary: Cancel an authorisation
                description: >-
                  Cancels the authorisation hold on a payment, returning a
                  unique reference for this request. You can cancel payments
                  after authorisation only for payment methods that support
                  distinct authorisations and captures.


                  For more information, refer to
                  [Cancel](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/cancel).


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments/{paymentPspReference}/cancels`](https://docs.adyen.com/api-explorer/#/CheckoutService/payments/{paymentPspReference}/cancels)
                  endpoint under Checkout API instead.
            /cancelOrRefund:
              post:
                tags:
                  - Cancel
                  - Or
                  - Refunds
                  - Payments
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                summary: Cancel or refund a payment
                description: >-
                  Cancels a payment if it has not been captured yet, or refunds
                  it if it has already been captured. This is useful when it is
                  not certain if the payment has been captured or not (for
                  example, when using auto-capture).


                  Do not use this endpoint for payments that involve:
                   * [Multiple partial captures](https://docs.adyen.com/online-payments/capture).
                   * [Split data](https://docs.adyen.com/marketplaces-and-platforms/processing-payments#providing-split-information) either at time of payment or capture for Adyen for Platforms.

                   Instead, check if the payment has been captured and make a corresponding [`/refund`](https://docs.adyen.com/api-explorer/#/Payment/refund) or [`/cancel`](https://docs.adyen.com/api-explorer/#/Payment/cancel) call.

                  For more information, refer to [Cancel or
                  refund](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/cancel-or-refund).


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments/{paymentPspReference}/reversals`](https://docs.adyen.com/api-explorer/#/CheckoutService/payments/{paymentPspReference}/reversals)
                  endpoint under Checkout API instead.
            /capture:
              post:
                tags:
                  - Capture
                  - null
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                summary: Capture an authorisation
                description: >+
                  Captures the authorisation hold on a payment, returning a
                  unique reference for this request. Usually the full
                  authorisation amount is captured, however it's also possible
                  to capture a smaller amount, which results in cancelling the
                  remaining authorisation balance.


                  Payment methods that are captured automatically after
                  authorisation don't need to be captured. However, submitting a
                  capture request on these transactions will not result in
                  double charges. If immediate or delayed auto-capture is
                  enabled, calling the capture method is not neccessary.


                  For more information refer to
                  [Capture](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/capture).


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments/{paymentPspReference}/captures`](https://docs.adyen.com/api-explorer/#/CheckoutService/v67/post/payments/{paymentPspReference}/captures)
                  endpoint on Checkout API instead.

            /donate:
              post:
                tags:
                  - Create
                  - Donations
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                  - Donate
                summary: Create a donation
                description: >-
                  Schedules a new payment to be created (including a new
                  authorisation request) for the specified donation using the
                  payment details of the original payment.


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/donations`](https://docs.adyen.com/api-explorer/#/CheckoutService/latest/post/donations)
                  endpoint under Checkout API instead.
            /getAuthenticationResult:
              post:
                tags:
                  - Get
                  - The
                  - Authentication
                  - Results
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                  - Donate
                  - Authentication
                  - Results
                summary: Get the 3DS authentication result
                description: >-
                  Return the authentication result after doing a 3D Secure
                  authentication only.
            /refund:
              post:
                tags:
                  - Refunds
                  - Captured
                  - Payments
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                  - Donate
                  - Authentication
                  - Results
                summary: Refund a captured payment
                description: >-
                  Refunds a payment that has previously been captured, returning
                  a unique reference for this request. Refunding can be done on
                  the full captured amount or a partial amount. Multiple
                  (partial) refunds will be accepted as long as their sum
                  doesn't exceed the captured amount. Payments which have been
                  authorised, but not captured, cannot be refunded, use the
                  /cancel method instead.


                  Some payment methods/gateways do not support partial/multiple
                  refunds.

                  A margin above the captured limit can be configured to cover
                  shipping/handling costs.


                  For more information, refer to
                  [Refund](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/refund).


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/payments/{paymentPspReference}/refunds`](https://docs.adyen.com/api-explorer/#/CheckoutService/payments/{paymentPspReference}/refunds)
                  endpoint under Checkout API instead.
            /retrieve3ds2Result:
              post:
                tags:
                  - Get
                  - The
                  - S2
                  - Authentication
                  - Results
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                  - Donate
                  - Authentication
                  - Results
                summary: Get the 3DS2 authentication result
                description: >-
                  Retrieves the `threeDS2Result` after doing a 3D Secure 2
                  authentication only.
            /technicalCancel:
              post:
                tags:
                  - Cancel
                  - null
                  - Authorization
                  - Using
                  - Your
                  - References
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                  - Donate
                  - Authentication
                  - Results
                summary: Cancel an authorisation using your reference
                description: >-
                  This endpoint allows you to cancel a payment if you do not
                  have the PSP reference of the original payment request
                  available.


                  In your call, refer to the original payment by using the
                  `reference` that you specified in your payment request.


                  For more information, see [Technical
                  cancel](https://docs.adyen.com/online-payments/classic-integrations/modify-payments/cancel#technical-cancel). 


                  > This endpoint is part of our [classic API
                  integration](https://docs.adyen.com/online-payments/classic-integrations/api-integration-ecommerce).
                  If using a [newer
                  integration](https://docs.adyen.com/online-payments), use the
                  [`/cancels`](https://docs.adyen.com/api-explorer/#/CheckoutService/cancels)
                  endpoint under Checkout API instead.
            /voidPendingRefund:
              post:
                tags:
                  - Cancel
                  - null
                  - In-person
                  - Refunds
                  - Authorization
                  - Authorization
                  - Authorization
                  - Authorization
                  - Cancel
                  - Or
                  - Refunds
                  - Capture
                  - Donate
                  - Authentication
                  - Results
                  - Pending
                summary: Cancel an in-person refund
                description: >-
                  This endpoint allows you to cancel an unreferenced refund
                  request before it has been completed.


                  In your call, you can refer to the original refund request
                  either by using the `tenderReference`, or the `pspReference`.
                  We recommend implementing based on the `tenderReference`, as
                  this is generated for both offline and online transactions.


                  For more information, refer to [Cancel an unreferenced
                  refund](https://docs.adyen.com/point-of-sale/re
    overlays:
      - type: APIs.io Search
        url: overlays/payments-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payments-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-payments-api
  - name: chime
    description: >-
      <important> <p> <b>Most of these APIs are no longer supported and will not
      be updated.</b> We recommend using the latest versions in the <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/welcome.html">Amazon
      Chime SDK API reference</a>, in the Amazon Chime SDK.</p> <p>Using the
      latest versions requires migrating to dedicated namespaces. For more
      information, refer to <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
      from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK Developer
      Guide</i>.</p> </important> <p>The Amazon Chime application programming
      interface (API) is designed so administrators can perform key tasks, such
      as creating and managing Amazon Chime accounts, users, and Voice
      Connectors. This guide provides detailed information about the Amazon
      Chime API, including operations, types, inputs and outputs, and error
      codes.</p> <p>You can use an AWS SDK, the AWS Command Line Interface (AWS
      CLI), or the REST API to make API calls for Amazon Chime. We recommend
      using an AWS SDK or the AWS CLI. The page for each API action contains a
      <i>See Also</i> section that includes links to information about using the
      action with a language-specific AWS SDK or the AWS CLI.</p> <dl> <dt>Using
      an AWS SDK</dt> <dd> <p> You don't need to write code to calculate a
      signature for request authentication. The SDK clients authenticate your
      requests by using access keys that you provide. For more information about
      AWS SDKs, see the <a href="http://aws.amazon.com/developer/">AWS Developer
      Center</a>. </p> </dd> <dt>Using the AWS CLI</dt> <dd> <p>Use your access
      keys with the AWS CLI to make API calls. For information about setting up
      the AWS CLI, see <a
      href="https://docs.aws.amazon.com/cli/latest/userguide/installing.html">Installing
      the AWS Command Line Interface</a> in the <i>AWS Command Line Interface
      User Guide</i>. For a list of available Amazon Chime commands, see the <a
      href="https://docs.aws.amazon.com/cli/latest/reference/chime/index.html">Amazon
      Chime commands</a> in the <i>AWS CLI Command Reference</i>. </p> </dd>
      <dt>Using REST APIs</dt> <dd> <p>If you use REST to make API calls, you
      must authenticate your request by providing a signature. Amazon Chime
      supports Signature Version 4. For more information, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Signature
      Version 4 Signing Process</a> in the <i>Amazon Web Services General
      Reference</i>.</p> <p>When making REST API calls, use the service name
      <code>chime</code> and REST endpoint
      <code>https://service.chime.aws.amazon.com</code>.</p> </dd> </dl>
      <p>Administrative permissions are controlled using AWS Identity and Access
      Management (IAM). For more information, see <a
      href="https://docs.aws.amazon.com/chime/latest/ag/security-iam.html">Identity
      and Access Management for Amazon Chime</a> in the <i>Amazon Chime
      Administration Guide</i>.</p>
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
            title: chime
          paths:
            /accounts/{accountId}/users/{userId}?operation=associate-phone-number:
              POST:
                summary: AssociatePhoneNumberWithUser
                description: >-
                  <p>Associates a phone number with the specified Amazon Chime
                  user.</p>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
            /voice-connectors/{voiceConnectorId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnector
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_AssociatePhoneNumbersWithVoiceConnector.html">AssociatePhoneNumbersWithVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
            /voice-connector-groups/{voiceConnectorGroupId}?operation=associate-phone-numbers:
              POST:
                summary: AssociatePhoneNumbersWithVoiceConnectorGroup
                description: >-
                  <p>Associates phone numbers with the specified Amazon Chime
                  Voice Connector group.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_AssociatePhoneNumbersWithVoiceConnectorGroup.html">AssociatePhoneNumbersWithVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Associate
                  - Phone
                  - Numbers
                  - With
                  - Voice
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
            /accounts/{accountId}?operation=associate-signin-delegate-groups:
              POST:
                summary: AssociateSigninDelegateGroupsWithAccount
                description: >-
                  <p>Associates the specified sign-in delegate groups with the
                  specified Amazon Chime account.</p>
                tags:
                  - Associate
                  - Sign In
                  - Delegate
                  - Groups
                  - With
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
            /meetings/{meetingId}/attendees?operation=batch-create:
              POST:
                summary: BatchCreateAttendee
                description: >-
                  <p>Creates up to 100 new attendees for an active Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_BatchCreateAttendee.html">BatchCreateAttendee</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p>For more information
                  about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p>
                tags:
                  - Batches
                  - Create
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
            /channels/{channelArn}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateChannelMembership
                description: >-
                  <p>Adds a specified number of users to a channel.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_BatchCreateChannelMembership.html">BatchCreateChannelMembership</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Batches
                  - Create
                  - Channels
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
            /accounts/{accountId}/rooms/{roomId}/memberships?operation=batch-create:
              POST:
                summary: BatchCreateRoomMembership
                description: >-
                  <p>Adds up to 50 members to a chat room in an Amazon Chime
                  Enterprise account. Members can be users or bots. The member
                  role designates whether the member is a chat room
                  administrator or a general chat room member.</p>
                tags:
                  - Batches
                  - Create
                  - Rooms
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
            /phone-numbers?operation=batch-delete:
              POST:
                summary: BatchDeletePhoneNumber
                description: >-
                  <p> Moves phone numbers into the <b>Deletion queue</b>. Phone
                  numbers must be disassociated from any users or Amazon Chime
                  Voice Connectors before they can be deleted. </p> <p> Phone
                  numbers remain in the <b>Deletion queue</b> for 7 days before
                  they are deleted permanently. </p>
                tags:
                  - Batches
                  - Delete
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
            /accounts/{accountId}/users?operation=suspend:
              POST:
                summary: BatchSuspendUser
                description: >-
                  <p>Suspends up to 50 users from a <code>Team</code> or
                  <code>EnterpriseLWA</code> Amazon Chime account. For more
                  information about different account types, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/manage-chime-account.html">Managing
                  Your Amazon Chime Accounts</a> in the <i>Amazon Chime
                  Administration Guide</i>.</p> <p>Users suspended from a
                  <code>Team</code> account are disassociated from the
                  account,but they can continue to use Amazon Chime as free
                  users. To remove the suspension from suspended
                  <code>Team</code> account users, invite them to the
                  <code>Team</code> account again. You can use the
                  <a>InviteUsers</a> action to do so.</p> <p>Users suspended
                  from an <code>EnterpriseLWA</code> account are immediately
                  signed out of Amazon Chime and can no longer sign in. To
                  remove the suspension from suspended
                  <code>EnterpriseLWA</code> account users, use the
                  <a>BatchUnsuspendUser</a> action.</p> <p> To sign out users
                  without suspending them, use the <a>LogoutUser</a> action.</p>
                tags:
                  - Batches
                  - Suspend
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
            /accounts/{accountId}/users?operation=unsuspend:
              POST:
                summary: BatchUnsuspendUser
                description: >-
                  <p>Removes the suspension from up to 50 previously suspended
                  users for the specified Amazon Chime
                  <code>EnterpriseLWA</code> account. Only users on
                  <code>EnterpriseLWA</code> accounts can be unsuspended using
                  this action. For more information about different account
                  types, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/manage-chime-account.html">
                  Managing Your Amazon Chime Accounts </a> in the account types,
                  in the <i>Amazon Chime Administration Guide</i>. </p>
                  <p>Previously suspended users who are unsuspended using this
                  action are returned to <code>Registered</code> status. Users
                  who are not previously suspended are ignored.</p>
                tags:
                  - Batches
                  - Unsuspend
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
            /phone-numbers?operation=batch-update:
              POST:
                summary: BatchUpdatePhoneNumber
                description: >-
                  <p>Updates phone number product types or calling names. You
                  can update one attribute at a time for each
                  <code>UpdatePhoneNumberRequestItem</code>. For example, you
                  can update the product type or the calling name.</p> <p>For
                  toll-free numbers, you cannot use the Amazon Chime Business
                  Calling product type. For numbers outside the U.S., you must
                  use the Amazon Chime SIP Media Application Dial-In product
                  type.</p> <p>Updates to outbound calling names can take up to
                  72 hours to complete. Pending updates to outbound calling
                  names must be complete before you can request another
                  update.</p>
                tags:
                  - Batches
                  - Update
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
            /accounts/{accountId}/users:
              GET:
                summary: ListUsers
                description: >-
                  <p>Lists the users that belong to the specified Amazon Chime
                  account. You can specify an email address to list only the
                  user that the email address belongs to.</p>
                tags:
                  - Lists
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
            /accounts:
              GET:
                summary: ListAccounts
                description: >-
                  <p>Lists the Amazon Chime accounts under the administrator's
                  AWS account. You can filter accounts by account name prefix.
                  To find out which Amazon Chime account a user belongs to, you
                  can filter by the user's email address, which returns one
                  account result.</p>
                tags:
                  - Lists
                  - Accounts
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
            /app-instances:
              GET:
                summary: ListAppInstances
                description: >-
                  <p>Lists all Amazon Chime <code>AppInstance</code>s created
                  under a single AWS account.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstances.html">ListAppInstances</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
            /app-instances/{appInstanceArn}/admins:
              GET:
                summary: ListAppInstanceAdmins
                description: >-
                  <p>Returns a list of the administrators in the
                  <code>AppInstance</code>.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstanceAdmins.html">ListAppInstanceAdmins</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Administrator
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
            /app-instance-users:
              GET:
                summary: ListAppInstanceUsers
                description: >-
                  <p>List all <code>AppInstanceUsers</code> created under a
                  single <code>AppInstance</code>. </p> <important> <p> <b>This
                  API is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_ListAppInstanceUsers.html">ListAppInstanceUsers</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
            /meetings/{meetingId}/attendees:
              GET:
                summary: ListAttendees
                description: >-
                  <p> Lists the attendees for the specified Amazon Chime SDK
                  meeting. For more information about the Amazon Chime SDK, see
                  <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListAttendees.html">ListAttendees</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
            /accounts/{accountId}/bots:
              GET:
                summary: ListBots
                description: >-
                  <p>Lists the bots associated with the administrator's Amazon
                  Chime Enterprise account ID.</p>
                tags:
                  - Lists
                  - Bots
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
            /channels:
              GET:
                summary: ListChannels
                description: >-
                  <p>Lists all Channels created under a single Chime App as a
                  paginated list. You can specify filters to narrow results.</p>
                  <p class="title"> <b>Functionality &amp; restrictions</b> </p>
                  <ul> <li> <p>Use privacy = <code>PUBLIC</code> to retrieve all
                  public channels in the account.</p> </li> <li> <p>Only an
                  <code>AppInstanceAdmin</code> can set privacy =
                  <code>PRIVATE</code> to list the private channels in an
                  account.</p> </li> </ul> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannels.html">ListChannels</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
            /channels/{channelArn}/bans:
              GET:
                summary: ListChannelBans
                description: >-
                  <p>Lists all the users banned from a particular channel.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelBans.html">ListChannelBans</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Bans
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
            /channels/{channelArn}/memberships:
              GET:
                summary: ListChannelMemberships
                description: >-
                  <p>Lists all channel memberships in a channel.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelMemberships.html">ListChannelMemberships</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
            /channels/{channelArn}/moderators:
              GET:
                summary: ListChannelModerators
                description: >-
                  <p>Lists all the moderators for a channel.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelModerators.html">ListChannelModerators</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Moderators
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
            /media-capture-pipelines:
              GET:
                summary: ListMediaCapturePipelines
                description: >-
                  <p>Returns a list of media capture pipelines.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_media-pipelines-chime_ListMediaCapturePipelines.html">ListMediaCapturePipelines</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Media
                  - Capture
                  - Pipelines
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
            /meetings:
              GET:
                summary: ListMeetings
                description: >-
                  <p>Lists up to 100 active Amazon Chime SDK meetings.</p>
                  <important> <p>ListMeetings is not supported in the Amazon
                  Chime SDK Meetings Namespace. Update your application to
                  remove calls to this API.</p> </important> <p>For more
                  information about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
            /meetings/{meetingId}/dial-outs:
              POST:
                summary: CreateMeetingDialOut
                description: >-
                  <p>Uses the join token and call metadata in a meeting request
                  (From number, To number, and so forth) to initiate an outbound
                  call to a public switched telephone network (PSTN) and join
                  them into a Chime meeting. Also ensures that the From number
                  belongs to the customer.</p> <p>To play welcome audio or
                  implement an interactive voice response (IVR), use the
                  <code>CreateSipMediaApplicationCall</code> action with the
                  corresponding SIP media application ID.</p> <important> <p>
                  <b>This API is is not available in a dedicated namespace.</b>
                  </p> </important>
                tags:
                  - Create
                  - Meetings
                  - Dial
                  - Out
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
            /meetings?operation=create-attendees:
              POST:
                summary: CreateMeetingWithAttendees
                description: >-
                  <p> Creates a new Amazon Chime SDK meeting in the specified
                  media Region, with attendees. For more information about
                  specifying media Regions, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/chime-sdk-meetings-regions.html">Amazon
                  Chime SDK Media Regions</a> in the <i>Amazon Chime SDK
                  Developer Guide</i> . For more information about the Amazon
                  Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i> . </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_CreateMeetingWithAttendees.html">CreateMeetingWithAttendees</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Create
                  - Meetings
                  - With
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
            /phone-number-orders:
              GET:
                summary: ListPhoneNumberOrders
                description: >-
                  <p>Lists the phone number orders for the administrator's
                  Amazon Chime account.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Orders
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
            /voice-connectors/{voiceConnectorId}/proxy-sessions:
              GET:
                summary: ListProxySessions
                description: >-
                  <p>Lists the proxy sessions for the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListProxySessions.html">ListProxySessions</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Proxy
                  - Sessions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /accounts/{accountId}/rooms:
              GET:
                summary: ListRooms
                description: >-
                  <p>Lists the room details for the specified Amazon Chime
                  Enterprise account. Optionally, filter the results by a member
                  ID (user ID or bot ID) to see a list of rooms that the member
                  belongs to.</p>
                tags:
                  - Lists
                  - Rooms
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}/memberships:
              GET:
                summary: ListRoomMemberships
                description: >-
                  <p>Lists the membership details for the specified room in an
                  Amazon Chime Enterprise account, such as the members' IDs,
                  email addresses, and names.</p>
                tags:
                  - Lists
                  - Rooms
                  - Memberships
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
            /sip-media-applications:
              GET:
                summary: ListSipMediaApplications
                description: >-
                  <p>Lists the SIP media applications under the administrator's
                  AWS account.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListSipMediaApplications.html">ListSipMediaApplications</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - SIP
                  - Media
                  - Applications
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
            /sip-media-applications/{sipMediaApplicationId}/calls:
              POST:
                summary: CreateSipMediaApplicationCall
                description: >-
                  <p>Creates an outbound call to a phone number from the phone
                  number specified in the request, and it invokes the endpoint
                  of the specified <code>sipMediaApplicationId</code>.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_CreateSipMediaApplicationCall.html">CreateSipMediaApplicationCall</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Create
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
            /sip-rules:
              GET:
                summary: ListSipRules
                description: >-
                  <p>Lists the SIP rules under the administrator's AWS
                  account.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListSipRules.html">ListSipRules</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - SIP
                  - Rules
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
            /accounts/{accountId}/users?operation=create:
              POST:
                summary: CreateUser
                description: >-
                  <p>Creates a user under the specified Amazon Chime
                  account.</p>
                tags:
                  - Create
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
            /voice-connectors:
              GET:
                summary: ListVoiceConnectors
                description: >-
                  <p>Lists the Amazon Chime Voice Connectors for the
                  administrator's AWS account.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectors.html">ListVoiceConnectors</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /voice-connector-groups:
              GET:
                summary: ListVoiceConnectorGroups
                description: >-
                  <p>Lists the Amazon Chime Voice Connector groups for the
                  administrator's AWS account.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectorGroups.html">ListVoiceConnectorGroups</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Groups
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /accounts/{accountId}:
              POST:
                summary: UpdateAccount
                description: >-
                  <p>Updates account details for the specified Amazon Chime
                  account. Currently, only account name and default license
                  updates are supported for this action.</p>
                tags:
                  - Update
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /app-instances/{appInstanceArn}:
              PUT:
                summary: UpdateAppInstance
                description: >-
                  <p>Updates <code>AppInstance</code> metadata.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_UpdateAppInstance.html">UpdateAppInstance</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
            /app-instances/{appInstanceArn}/admins/{appInstanceAdminArn}:
              GET:
                summary: DescribeAppInstanceAdmin
                description: >-
                  <p>Returns the full details of an
                  <code>AppInstanceAdmin</code>.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_DescribeAppInstanceAdmin.html">DescribeAppInstanceAdmin</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Applications
                  - Instances
                  - Administrative
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
            /app-instances/{appInstanceArn}/streaming-configurations:
              PUT:
                summary: PutAppInstanceStreamingConfigurations
                description: >-
                  <p>The data streaming configurations of an
                  <code>AppInstance</code>.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_PutMessagingStreamingConfigurations.html">PutMessagingStreamingConfigurations</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Streaming
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
            /app-instance-users/{appInstanceUserArn}:
              PUT:
                summary: UpdateAppInstanceUser
                description: >-
                  <p>Updates the details of an <code>AppInstanceUser</code>. You
                  can update names and metadata.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_UpdateAppInstanceUser.html">UpdateAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
            /meetings/{meetingId}/attendees/{attendeeId}:
              GET:
                summary: GetAttendee
                description: >-
                  <p> Gets the Amazon Chime SDK attendee details for a specified
                  meeting ID and attendee ID. For more information about the
                  Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i>. </p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_GetAttendee.html">GetAttendee</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
            /channels/{channelArn}:
              PUT:
                summary: UpdateChannel
                description: >-
                  <p>Update a channel's attributes.</p> <p> <b>Restriction</b>:
                  You can't change a channel's privacy. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannel.html">UpdateChannel</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
            /channels/{channelArn}/bans/{memberArn}:
              GET:
                summary: DescribeChannelBan
                description: >-
                  <p>Returns the full details of a channel ban.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelBan.html">DescribeChannelBan</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Ban
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
            /channels/{channelArn}/memberships/{memberArn}:
              GET:
                summary: DescribeChannelMembership
                description: >-
                  <p>Returns the full details of a user's channel
                  membership.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelMembership.html">DescribeChannelMembership</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
            /channels/{channelArn}/messages/{messageId}:
              PUT:
                summary: UpdateChannelMessage
                description: >-
                  <p>Updates the content of a message.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannelMessage.html">UpdateChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
            /channels/{channelArn}/moderators/{channelModeratorArn}:
              GET:
                summary: DescribeChannelModerator
                description: >-
                  <p>Returns the full details of a single ChannelModerator.</p>
                  <note> <p>The <code>x-amz-chime-bearer</code> request header
                  is mandatory. Use the <code>AppInstanceUserArn</code> of the
                  user that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelModerator.html">DescribeChannelModerator</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Moderators
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
            /accounts/{accountId}/bots/{botId}/events-configuration:
              PUT:
                summary: PutEventsConfiguration
                description: >-
                  <p>Creates an events configuration that allows a bot to
                  receive outgoing events sent by Amazon Chime. Choose either an
                  HTTPS endpoint or a Lambda function ARN. For more information,
                  see <a>Bot</a>.</p>
                tags:
                  - Put
                  - Events
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
            /media-capture-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaCapturePipeline
                description: >-
                  <p>Gets an existing media capture pipeline.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_media-pipelines-chime_GetMediaCapturePipeline.html">GetMediaCapturePipeline</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Media
                  - Capture
                  - Pipelines
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /meetings/{meetingId}:
              GET:
                summary: GetMeeting
                description: >-
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_GetMeeting.html">GetMeeting</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p> Gets the Amazon
                  Chime SDK meeting details for the specified meeting ID. For
                  more information about the Amazon Chime SDK, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meetings-sdk.html">Using
                  the Amazon Chime SDK</a> in the <i>Amazon Chime SDK Developer
                  Guide</i> . </p>
                tags:
                  - Get
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /phone-numbers/{phoneNumberId}:
              POST:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates phone number details, such as product type or
                  calling name, for the specified phone number ID. You can
                  update one phone number detail at a time. For example, you can
                  update either the product type or the calling name in one
                  action.</p> <p>For toll-free numbers, you cannot use the
                  Amazon Chime Business Calling product type. For numbers
                  outside the U.S., you must use the Amazon Chime SIP Media
                  Application Dial-In product type.</p> <p>Updates to outbound
                  calling names can take 72 hours to complete. Pending updates
                  to outbound calling names must be complete before you can
                  request another update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
            /voice-connectors/{voiceConnectorId}/proxy-sessions/{proxySessionId}:
              POST:
                summary: UpdateProxySession
                description: >-
                  <p>Updates the specified proxy session details, such as voice
                  or SMS capabilities.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateProxySession.html">UpdateProxySession</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Proxy
                  - Sessions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}:
              POST:
                summary: UpdateRoom
                description: >-
                  <p>Updates room details, such as the room name, for a room in
                  an Amazon Chime Enterprise account.</p>
                tags:
                  - Update
                  - Rooms
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /accounts/{accountId}/rooms/{roomId}/memberships/{memberId}:
              POST:
                summary: UpdateRoomMembership
                description: >-
                  <p>Updates room membership details, such as the member role,
                  for a room in an Amazon Chime Enterprise account. The member
                  role designates whether the member is a chat room
                  administrator or a general chat room member. The member role
                  can be updated only for user IDs.</p>
                tags:
                  - Update
                  - Rooms
                  - Membership
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /sip-media-applications/{sipMediaApplicationId}:
              PUT:
                summary: UpdateSipMediaApplication
                description: >-
                  <p>Updates the details of the specified SIP media
                  application.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipMediaApplication.html">UpdateSipMediaApplication</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
            /sip-rules/{sipRuleId}:
              PUT:
                summary: UpdateSipRule
                description: >-
                  <p>Updates the details of the specified SIP rule.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipRule.html">UpdateSipRule</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Rules
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}:
              PUT:
                summary: UpdateVoiceConnector
                description: >-
                  <p>Updates details for the specified Amazon Chime Voice
                  Connector.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateVoiceConnector.html">UpdateVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
            /voice-connectors/{voiceConnectorId}/emergency-calling-configuration:
              PUT:
                summary: PutVoiceConnectorEmergencyCallingConfiguration
                description: >-
                  <p>Puts emergency calling configuration details to the
                  specified Amazon Chime Voice Connector, such as emergency
                  phone numbers and calling countries. Origination and
                  termination settings must be enabled for the Amazon Chime
                  Voice Connector before emergency calling can be
                  configured.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorEmergencyCallingConfiguration.html">PutVoiceConnectorEmergencyCallingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Emergency
                  - Calling
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
            /voice-connector-groups/{voiceConnectorGroupId}:
              PUT:
                summary: UpdateVoiceConnectorGroup
                description: >-
                  <p>Updates details of the specified Amazon Chime Voice
                  Connector group, such as the name and Amazon Chime Voice
                  Connector priority ranking.</p> <important> <p> <b>This API is
                  is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateVoiceConnectorGroup.html">UpdateVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Voice
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
            /voice-connectors/{voiceConnectorId}/origination:
              PUT:
                summary: PutVoiceConnectorOrigination
                description: >-
                  <p>Adds origination settings for the specified Amazon Chime
                  Voice Connector.</p> <note> <p>If emergency calling is
                  configured for the Amazon Chime Voice Connector, it must be
                  deleted prior to turning off origination settings.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorOrigination.html">PutVoiceConnectorOrigination</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Origination
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
            /voice-connectors/{voiceConnectorId}/programmable-numbers/proxy:
              PUT:
                summary: PutVoiceConnectorProxy
                description: >-
                  <p>Puts the specified proxy configuration to the specified
                  Amazon Chime Voice Connector.</p> <important> <p> <b>This API
                  is is no longer supported and will not be updated.</b> We
                  recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorProxy.html">PutVoiceConnectorProxy</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Proxy
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/streaming-configuration:
              PUT:
                summary: PutVoiceConnectorStreamingConfiguration
                description: >-
                  <p>Adds a streaming configuration for the specified Amazon
                  Chime Voice Connector. The streaming configuration specifies
                  whether media streaming is enabled for sending to Kinesis. It
                  also sets the retention period, in hours, for the Amazon
                  Kinesis data.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorStreamingConfiguration.html">PutVoiceConnectorStreamingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Streaming
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
            /voice-connectors/{voiceConnectorId}/termination:
              PUT:
                summary: PutVoiceConnectorTermination
                description: >-
                  <p>Adds termination settings for the specified Amazon Chime
                  Voice Connector.</p> <note> <p>If emergency calling is
                  configured for the Amazon Chime Voice Connector, it must be
                  deleted prior to turning off termination settings.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorTermination.html">PutVoiceConnectorTermination</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Termination
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=delete:
              POST:
                summary: DeleteVoiceConnectorTerminationCredentials
                description: >-
                  <p>Deletes the specified SIP credentials used by your
                  equipment to authenticate during call termination.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DeleteVoiceConnectorTerminationCredentials.html">DeleteVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Delete
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
            /channels/{channelArn}?scope=app-instance-user-membership:
              GET:
                summary: DescribeChannelMembershipForAppInstanceUser
                description: >-
                  <p> Returns the details of a channel based on the membership
                  of the specified <code>AppInstanceUser</code>.</p> <note>
                  <p>The <code>x-amz-chime-bearer</code> request header is
                  mandatory. Use the <code>AppInstanceUserArn</code> of the user
                  that makes the API call as the value in the header.</p>
                  </note> <important> <p> <b>This API is is no longer supported
                  and will not be updated.</b> We recommend using the latest
                  version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelMembershipForAppInstanceUser.html">DescribeChannelMembershipForAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Membership
                  - For
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
            /channels/{channelArn}?scope=app-instance-user-moderated-channel:
              GET:
                summary: DescribeChannelModeratedByAppInstanceUser
                description: >-
                  <p>Returns the full details of a channel moderated by the
                  specified <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_DescribeChannelModeratedByAppInstanceUser.html">DescribeChannelModeratedByAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Describe
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
            /accounts/{accountId}/users/{userId}?operation=disassociate-phone-number:
              POST:
                summary: DisassociatePhoneNumberFromUser
                description: >-
                  <p>Disassociates the primary provisioned phone number from the
                  specified Amazon Chime user.</p>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /voice-connectors/{voiceConnectorId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnector
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime Voice Connector.</p> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DisassociatePhoneNumbersFromVoiceConnector.html">DisassociatePhoneNumbersFromVoiceConnector</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Voice
                  - Connectors
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /voice-connector-groups/{voiceConnectorGroupId}?operation=disassociate-phone-numbers:
              POST:
                summary: DisassociatePhoneNumbersFromVoiceConnectorGroup
                description: >-
                  <p>Disassociates the specified phone numbers from the
                  specified Amazon Chime Voice Connector group.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_DisassociatePhoneNumbersFromVoiceConnectorGroup.html">DisassociatePhoneNumbersFromVoiceConnectorGroup</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - From
                  - Voice
                  - Connectors
                  - Group
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /accounts/{accountId}?operation=disassociate-signin-delegate-groups:
              POST:
                summary: DisassociateSigninDelegateGroupsFromAccount
                description: >-
                  <p>Disassociates the specified sign-in delegate groups from
                  the specified Amazon Chime account.</p>
                tags:
                  - Disassociate
                  - Sign In
                  - Delegate
                  - Groups
                  - From
                  - Account
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
            /accounts/{accountId}/settings:
              PUT:
                summary: UpdateAccountSettings
                description: >-
                  <p>Updates the settings for the specified Amazon Chime
                  account. You can update settings for remote control of shared
                  screens, or for the dial-out option. For more information
                  about these settings, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/policies.html">Use
                  the Policies Page</a> in the <i>Amazon Chime Administration
                  Guide</i>.</p>
                tags:
                  - Update
                  - Account
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
            /app-instances/{appInstanceArn}/retention-settings:
              PUT:
                summary: PutAppInstanceRetentionSettings
                description: >-
                  <p>Sets the amount of time in days that a given
                  <code>AppInstance</code> retains data.</p> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_identity-chime_PutAppInstanceRetentionSettings.html">PutAppInstanceRetentionSettings</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Applications
                  - Instances
                  - Retention
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /accounts/{accountId}/bots/{botId}:
              POST:
                summary: UpdateBot
                description: >-
                  <p>Updates the status of the specified bot, such as starting
                  or stopping the bot from running in your Amazon Chime
                  Enterprise account.</p>
                tags:
                  - Update
                  - Bot
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /settings:
              PUT:
                summary: UpdateGlobalSettings
                description: >-
                  <p>Updates global settings for the administrator's AWS
                  account, such as Amazon Chime Business Calling and Amazon
                  Chime Voice Connector settings.</p>
                tags:
                  - Update
                  - Global
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
            /endpoints/messaging-session:
              GET:
                summary: GetMessagingSessionEndpoint
                description: >-
                  <p>The details of the endpoint for the messaging session.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_GetMessagingSessionEndpoint.html">GetMessagingSessionEndpoint</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Messaging
                  - Sessions
                  - Endpoints
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
            /phone-number-orders/{phoneNumberOrderId}:
              GET:
                summary: GetPhoneNumberOrder
                description: >-
                  <p>Retrieves details for the specified phone number order,
                  such as the order creation timestamp, phone numbers in E.164
                  format, product type, and order status.</p>
                tags:
                  - Get
                  - Phone
                  - Numbers
                  - Orders
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /settings/phone-number:
              PUT:
                summary: UpdatePhoneNumberSettings
                description: >-
                  <p>Updates the phone number settings for the administrator's
                  AWS account, such as the default outbound calling name. You
                  can update the default outbound calling name once every seven
                  days. Outbound calling names can take up to 72 hours to
                  update.</p>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /accounts/{accountId}/retention-settings:
              PUT:
                summary: PutRetentionSettings
                description: >-
                  <p> Puts retention settings for the specified Amazon Chime
                  Enterprise account. We recommend using AWS CloudTrail to
                  monitor usage of this API for your account. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/cloudtrail.html">Logging
                  Amazon Chime API Calls with AWS CloudTrail</a> in the
                  <i>Amazon Chime Administration Guide</i>.</p> <p> To turn off
                  existing retention settings, remove the number of days from
                  the corresponding <b>RetentionDays</b> field in the
                  <b>RetentionSettings</b> object. For more information about
                  retention settings, see <a
                  href="https://docs.aws.amazon.com/chime/latest/ag/chat-retention.html">Managing
                  Chat Retention Policies</a> in the <i>Amazon Chime
                  Administration Guide</i>.</p>
                tags:
                  - Put
                  - Retention
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
            /sip-media-applications/{sipMediaApplicationId}/logging-configuration:
              PUT:
                summary: PutSipMediaApplicationLoggingConfiguration
                description: >-
                  <p>Updates the logging configuration for the specified SIP
                  media application.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutSipMediaApplicationLoggingConfiguration.html">PutSipMediaApplicationLoggingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - SIP
                  - Media
                  - Applications
                  - Logging
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /accounts/{accountId}/users/{userId}:
              POST:
                summary: UpdateUser
                description: >-
                  <p>Updates user details for a specified user ID. Currently,
                  only <code>LicenseType</code> updates are supported for this
                  action.</p>
                tags:
                  - Update
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /accounts/{accountId}/users/{userId}/settings:
              PUT:
                summary: UpdateUserSettings
                description: >-
                  <p>Updates the settings for the specified user, such as phone
                  number settings.</p>
                tags:
                  - Update
                  - Users
                  - Settings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /voice-connectors/{voiceConnectorId}/logging-configuration:
              PUT:
                summary: PutVoiceConnectorLoggingConfiguration
                description: >-
                  <p>Adds a logging configuration for the specified Amazon Chime
                  Voice Connector. The logging configuration specifies whether
                  SIP message logs are enabled for sending to Amazon CloudWatch
                  Logs.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorLoggingConfiguration.html">PutVoiceConnectorLoggingConfiguration</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Logging
                  - Configurations
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
            /voice-connectors/{voiceConnectorId}/termination/health:
              GET:
                summary: GetVoiceConnectorTerminationHealth
                description: >-
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_GetVoiceConnectorTerminationHealth.html">GetVoiceConnectorTerminationHealth</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important> <p>Retrieves information
                  about the last time a SIP <code>OPTIONS</code> ping was
                  received from your SIP infrastructure for the specified Amazon
                  Chime Voice Connector.</p>
                tags:
                  - Get
                  - Voice
                  - Connectors
                  - Termination
                  - Health
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
            /accounts/{accountId}/users?operation=add:
              POST:
                summary: InviteUsers
                description: >-
                  <p>Sends email to a maximum of 50 users, inviting them to the
                  specified Amazon Chime <code>Team</code> account. Only
                  <code>Team</code> account types are currently supported for
                  this action.</p>
                tags:
                  - Invite
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
            /meetings/{meetingId}/attendees/{attendeeId}/tags:
              GET:
                summary: ListAttendeeTags
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK attendee
                  resource.</p> <important> <p>ListAttendeeTags is not supported
                  in the Amazon Chime SDK Meetings Namespace. Update your
                  application to remove calls to this API.</p> </important>
                tags:
                  - Lists
                  - Attendees
                  - Tags
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
            /channels?scope=app-instance-user-memberships:
              GET:
                summary: ListChannelMembershipsForAppInstanceUser
                description: >-
                  <p> Lists all channels that a particular
                  <code>AppInstanceUser</code> is a part of. Only an
                  <code>AppInstanceAdmin</code> can call the API with a user ARN
                  that is not their own. </p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelMembershipsForAppInstanceUser.html">ListChannelMembershipsForAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Memberships
                  - For
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /channels/{channelArn}/messages:
              POST:
                summary: SendChannelMessage
                description: >-
                  <p>Sends a message to a particular channel that the member is
                  a part of.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> <p>Also,
                  <code>STANDARD</code> messages can contain 4KB of data and the
                  1KB of metadata. <code>CONTROL</code> messages can contain 30
                  bytes of data and no metadata.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_SendChannelMessage.html">SendChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Send
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /channels?scope=app-instance-user-moderated-channels:
              GET:
                summary: ListChannelsModeratedByAppInstanceUser
                description: >-
                  <p>A list of the channels moderated by an
                  <code>AppInstanceUser</code>.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListChannelsModeratedByAppInstanceUser.html">ListChannelsModeratedByAppInstanceUser</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Channels
                  - Moderated
                  - By
                  - Applications
                  - Instances
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /meetings/{meetingId}/tags:
              GET:
                summary: ListMeetingTags
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK meeting
                  resource.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListTagsForResource.html">ListTagsForResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Meetings
                  - Tags
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /phone-numbers:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Lists the phone numbers for the specified Amazon Chime
                  account, Amazon Chime user, Amazon Chime Voice Connector, or
                  Amazon Chime Voice Connector group.</p>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
            /phone-number-countries:
              GET:
                summary: ListSupportedPhoneNumberCountries
                description: <p>Lists supported phone number countries.</p>
                tags:
                  - Lists
                  - Supported
                  - Phone
                  - Numbers
                  - Countries
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
            /tags:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists the tags applied to an Amazon Chime SDK meeting and
                  messaging resources.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the applicable latest version in the Amazon Chime
                  SDK.</p> <ul> <li> <p>For meetings: <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_ListTagsForResource.html">ListTagsForResource</a>.</p>
                  </li> <li> <p>For messaging: <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_ListTagsForResource.html">ListTagsForResource</a>.</p>
                  </li> </ul> <p>Using the latest version requires migrating to
                  a dedicated namespace. For more information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
            /voice-connectors/{voiceConnectorId}/termination/credentials:
              GET:
                summary: ListVoiceConnectorTerminationCredentials
                description: >-
                  <p>Lists the SIP credentials for the specified Amazon Chime
                  Voice Connector.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ListVoiceConnectorTerminationCredentials.html">ListVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Lists
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
            /accounts/{accountId}/users/{userId}?operation=logout:
              POST:
                summary: LogoutUser
                description: >-
                  <p>Logs out the specified user from all of the devices they
                  are currently logged into.</p>
                tags:
                  - Logout
                  - Users
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
            /voice-connectors/{voiceConnectorId}/termination/credentials?operation=put:
              POST:
                summary: PutVoiceConnectorTerminationCredentials
                description: >-
                  <p>Adds termination SIP credentials for the specified Amazon
                  Chime Voice Connector.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_PutVoiceConnectorTerminationCredentials.html">PutVoiceConnectorTerminationCredentials</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Put
                  - Voice
                  - Connectors
                  - Termination
                  - Credentials
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
            /channels/{channelArn}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactChannelMessage
                description: >-
                  <p>Redacts message content, but not metadata. The message
                  exists in the back end, but the action returns null content,
                  and the state shows as redacted.</p> <note> <p>The
                  <code>x-amz-chime-bearer</code> request header is mandatory.
                  Use the <code>AppInstanceUserArn</code> of the user that makes
                  the API call as the value in the header.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_RedactChannelMessage.html">RedactChannelMessage</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Redact
                  - Channels
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
            /accounts/{accountId}/conversations/{conversationId}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactConversationMessage
                description: >-
                  <p>Redacts the specified message from the specified Amazon
                  Chime conversation.</p>
                tags:
                  - Redact
                  - Conversations
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
            /accounts/{accountId}/rooms/{roomId}/messages/{messageId}?operation=redact:
              POST:
                summary: RedactRoomMessage
                description: >-
                  <p>Redacts the specified message from the specified Amazon
                  Chime channel.</p>
                tags:
                  - Redact
                  - Rooms
                  - Messages
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
            /accounts/{accountId}/bots/{botId}?operation=regenerate-security-token:
              POST:
                summary: RegenerateSecurityToken
                description: <p>Regenerates the security token for a bot.</p>
                tags:
                  - Regenerate
                  - Security
                  - Tokens
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
            /accounts/{accountId}/users/{userId}?operation=reset-personal-pin:
              POST:
                summary: ResetPersonalPIN
                description: >-
                  <p>Resets the personal meeting PIN for the specified user on
                  an Amazon Chime account. Returns the <a>User</a> object with
                  the updated personal meeting PIN.</p>
                tags:
                  - Reset
                  - Personal
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
            /phone-numbers/{phoneNumberId}?operation=restore:
              POST:
                summary: RestorePhoneNumber
                description: >-
                  <p>Moves a phone number from the <b>Deletion queue</b> back
                  into the phone number <b>Inventory</b>.</p>
                tags:
                  - Restore
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
            /search?type=phone-numbers:
              GET:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches for phone numbers that can be ordered. For US
                  numbers, provide at least one of the following search filters:
                  <code>AreaCode</code>, <code>City</code>, <code>State</code>,
                  or <code>TollFreePrefix</code>. If you provide
                  <code>City</code>, you must also provide <code>State</code>.
                  Numbers outside the US only support the
                  <code>PhoneNumberType</code> filter, which you must use.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
            /meetings/{meetingId}/transcription?operation=start:
              POST:
                summary: StartMeetingTranscription
                description: >-
                  <p>Starts transcription for the specified
                  <code>meetingId</code>. For more information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/meeting-transcription.html">
                  Using Amazon Chime SDK live transcription </a> in the
                  <i>Amazon Chime SDK Developer Guide</i>.</p> <p>If you specify
                  an invalid configuration, a <code>TranscriptFailed</code>
                  event will be sent with the contents of the
                  <code>BadRequestException</code> generated by Amazon
                  Transcribe. For more information on each parameter and which
                  combinations are valid, refer to the <a
                  href="https://docs.aws.amazon.com/transcribe/latest/APIReference/API_streaming_StartStreamTranscription.html">StartStreamTranscription</a>
                  API in the <i>Amazon Transcribe Developer Guide</i>.</p>
                  <note> <p>Amazon Chime SDK live transcription is powered by
                  Amazon Transcribe. Use of Amazon Transcribe is subject to the
                  <a href="https://aws.amazon.com/service-terms/">AWS Service
                  Terms</a>, including the terms specific to the AWS Machine
                  Learning and Artificial Intelligence Services.</p> </note>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_StartMeetingTranscription.html">StartMeetingTranscription</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Start
                  - Meetings
                  - Transcriptions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
            /meetings/{meetingId}/transcription?operation=stop:
              POST:
                summary: StopMeetingTranscription
                description: >-
                  <p>Stops transcription for the specified
                  <code>meetingId</code>.</p> <important> <p> <b>This API is is
                  no longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_StopMeetingTranscription.html">StopMeetingTranscription</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Stop
                  - Meetings
                  - Transcriptions
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
            /meetings/{meetingId}/attendees/{attendeeId}/tags?operation=add:
              POST:
                summary: TagAttendee
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  attendee.</p> <important> <p>TagAttendee is not supported in
                  the Amazon Chime SDK Meetings Namespace. Update your
                  application to remove calls to this API.</p> </important>
                tags:
                  - Tags
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
            /meetings/{meetingId}/tags?operation=add:
              POST:
                summary: TagMeeting
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_TagResource.html">TagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Tags
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>Applies the specified tags to the specified Amazon Chime
                  SDK meeting resource.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_TagResource.html">TagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Tags
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
            /meetings/{meetingId}/attendees/{attendeeId}/tags?operation=delete:
              POST:
                summary: UntagAttendee
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK attendee.</p> <important> <p>UntagAttendee is not
                  supported in the Amazon Chime SDK Meetings Namespace. Update
                  your application to remove calls to this API.</p> </important>
                tags:
                  - Untag
                  - Attendees
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
            /meetings/{meetingId}/tags?operation=delete:
              POST:
                summary: UntagMeeting
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK meeting.</p> <important> <p> <b>This API is is no longer
                  supported and will not be updated.</b> We recommend using the
                  latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_UntagResource.html">UntagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Untag
                  - Meetings
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: >-
                  <p>Untags the specified tags from the specified Amazon Chime
                  SDK meeting resource.</p> <p>Applies the specified tags to the
                  specified Amazon Chime SDK meeting resource.</p> <important>
                  <p> <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_meeting-chime_UntagResource.html">UntagResource</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
            /channels/{channelArn}/readMarker:
              PUT:
                summary: UpdateChannelReadMarker
                description: >-
                  <p>The details of the time when a user last read messages in a
                  channel.</p> <note> <p>The <code>x-amz-chime-bearer</code>
                  request header is mandatory. Use the
                  <code>AppInstanceUserArn</code> of the user that makes the API
                  call as the value in the header.</p> </note> <important> <p>
                  <b>This API is is no longer supported and will not be
                  updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_messaging-chime_UpdateChannelReadMarker.html">UpdateChannelReadMarker</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - Channels
                  - Read
                  - Marker
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
            /sip-media-applications/{sipMediaApplicationId}/calls/{transactionId}:
              POST:
                summary: UpdateSipMediaApplicationCall
                description: >-
                  <p>Invokes the AWS Lambda function associated with the SIP
                  media application and transaction ID in an update request. The
                  Lambda function can then return a new set of actions.</p>
                  <important> <p> <b>This API is is no longer supported and will
                  not be updated.</b> We recommend using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_UpdateSipMediaApplicationCall.html">UpdateSipMediaApplicationCall</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </important>
                tags:
                  - Update
                  - SIP
                  - Media
                  - Applications
                  - Call
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
                  - Transactions
            /emergency-calling/address:
              POST:
                summary: ValidateE911Address
                description: >-
                  <p>Validates an address to be used for 911 calls made with
                  Amazon Chime Voice Connectors. You can use validated addresses
                  in a Presence Information Data Format Location Object file
                  that you include in SIP requests. That helps ensure that
                  addresses are routed to the appropriate Public Safety
                  Answering Point.</p> <important> <p> <b>This API is is no
                  longer supported and will not be updated.</b> We recommend
                  using the latest version, <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_voice-chime_ValidateE911Address.html">ValidateE911Address</a>,
                  in the Amazon Chime SDK.</p> <p>Using the latest version
                  requires migrating to a dedicated namespace. For more
                  information, refer to <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/migrate-from-chm-namespace.html">Migrating
                  from the Amazon Chime namespace</a> in the <i>Amazon Chime SDK
                  Developer Guide</i>.</p> </
                tags:
                  - Validate
                  - E911
                  - Addresses
                  - Identifiers
                  - Users
                  - Users
                  - '?operation=associate'
                  - Phone
                  - Numbers
                  - Connectors
                  - Numbers
                  - Group
                  - Sign In
                  - Delegate
                  - Groups
                  - Attendees
                  - Create
                  - ARN
                  - Memberships
                  - Rooms
                  - Rooms
                  - Numbers?operation=batch
                  - Delete
                  - Users
                  - Users
                  - Update
                  - Accounts
                  - Applications
                  - Instances
                  - Instances
                  - Administrator
                  - Attendees
                  - Bots
                  - Channels
                  - Bans
                  - Memberships
                  - Moderators
                  - Media
                  - Capture
                  - Pipelines
                  - Meetings
                  - Dial
                  - Outs
                  - Meetings
                  - Orders
                  - Proxy
                  - Sessions
                  - SIP
                  - Applications
                  - Applications
                  - Calls
                  - Rules
                  - Users
                  - Voice
                  - Connectors
                  - Administrative
                  - Streaming
                  - Configurations
                  - Attendees
                  - Members
                  - Messages
                  - Messages
                  - Channels
                  - Moderators
                  - Bot
                  - Events
                  - Configurations
                  - Pipelines
                  - Sessions
                  - Rules
                  - Emergency
                  - Calling
                  - Origination
                  - Programmable
                  - Termination
                  - Credentials
                  - '?scope=app'
                  - Membership
                  - Moderated
                  - '?operation=disassociate'
                  - Settings
                  - Retention
                  - Endpoints
                  - Messaging
                  - Orders
                  - Logging
                  - Health
                  - Users
                  - Tags
                  - Channels
                  - Countries
                  - Credentials
                  - '?operation=logout'
                  - Credentials
                  - '?operation=redact'
                  - Conversations
                  - Conversations
                  - '?operation=regenerate'
                  - Security
                  - Tokens
                  - '?operation=reset'
                  - Personal
                  - Pin
                  - '?operation=restore'
                  - Search
                  - Transcriptions
                  - Transcriptions
                  - Tags
                  - Tags
                  - Resources
                  - Tags
                  - Tags
                  - Read
                  - Marker
                  - Transactions
                  - Addresses''
    overlays:
      - type: APIs.io Search
        url: overlays/chime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime
  - name: chime-sdk-media-pipelines
    description: >-
      <p>The Amazon Chime SDK media pipeline APIs in this section allow software
      developers to create Amazon Chime SDK media pipelines that capture,
      concatenate, or stream your Amazon Chime SDK meetings. For more
      information about media pipelines, see <a
      href="https://docs.aws.amazon.com/chime-sdk/latest/APIReference/API_Operations_Amazon_Chime_SDK_Media_Pipelines.html">Amazon
      Chime SDK media pipelines</a>. </p>
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
            title: chime-sdk-media-pipelines
          paths:
            /sdk-media-capture-pipelines:
              GET:
                summary: ListMediaCapturePipelines
                description: <p>Returns a list of media pipelines.</p>
                tags:
                  - Lists
                  - Media
                  - Capture
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
            /sdk-media-concatenation-pipelines:
              POST:
                summary: CreateMediaConcatenationPipeline
                description: <p>Creates a media concatenation pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Concatenation
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
            /media-insights-pipelines:
              POST:
                summary: CreateMediaInsightsPipeline
                description: <p>Creates a media insights pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Insights
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
            /media-insights-pipeline-configurations:
              GET:
                summary: ListMediaInsightsPipelineConfigurations
                description: >-
                  <p>Lists the available media insights pipeline
                  configurations.</p>
                tags:
                  - Lists
                  - Media
                  - Insights
                  - Pipelines
                  - Configurations
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
            /sdk-media-live-connector-pipelines:
              POST:
                summary: CreateMediaLiveConnectorPipeline
                description: >-
                  <p>Creates a media live connector pipeline in an Amazon Chime
                  SDK meeting.</p>
                tags:
                  - Create
                  - Media
                  - Live
                  - Connectors
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
            /media-pipeline-kinesis-video-stream-pools:
              GET:
                summary: ListMediaPipelineKinesisVideoStreamPools
                description: <p>Lists the video stream pools in the media pipeline.</p>
                tags:
                  - Lists
                  - Media
                  - Pipelines
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
            /sdk-media-stream-pipelines:
              POST:
                summary: CreateMediaStreamPipeline
                description: <p>Creates a streaming media pipeline.</p>
                tags:
                  - Create
                  - Media
                  - Stream
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
            /sdk-media-capture-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaCapturePipeline
                description: <p>Gets an existing media pipeline.</p>
                tags:
                  - Get
                  - Media
                  - Capture
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
            /media-insights-pipeline-configurations/{identifier}:
              PUT:
                summary: UpdateMediaInsightsPipelineConfiguration
                description: >-
                  <p>Updates the media insights pipeline's configuration
                  settings.</p>
                tags:
                  - Update
                  - Media
                  - Insights
                  - Pipelines
                  - Configurations
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /sdk-media-pipelines/{mediaPipelineId}:
              GET:
                summary: GetMediaPipeline
                description: <p>Gets an existing media pipeline.</p>
                tags:
                  - Get
                  - Media
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /media-pipeline-kinesis-video-stream-pools/{identifier}:
              PUT:
                summary: UpdateMediaPipelineKinesisVideoStreamPool
                description: >-
                  <p>Updates an Kinesis video stream pool in a media
                  pipeline.</p>
                tags:
                  - Update
                  - Media
                  - Pipelines
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
            /media-insights-pipelines/{identifier}/speaker-search-tasks/{speakerSearchTaskId}:
              GET:
                summary: GetSpeakerSearchTask
                description: >-
                  <p>Retrieves the details of the specified speaker search
                  task.</p>
                tags:
                  - Get
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks/{voiceToneAnalysisTaskId}:
              GET:
                summary: GetVoiceToneAnalysisTask
                description: <p>Retrieves the details of a voice tone analysis task.</p>
                tags:
                  - Get
                  - Voice
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
            /sdk-media-pipelines:
              GET:
                summary: ListMediaPipelines
                description: <p>Returns a list of media pipelines.</p>
                tags:
                  - Lists
                  - Media
                  - Pipelines
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
            /tags:
              GET:
                summary: ListTagsForResource
                description: <p>Lists the tags available for a media pipeline.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
            /media-insights-pipelines/{identifier}/speaker-search-tasks?operation=start:
              POST:
                summary: StartSpeakerSearchTask
                description: >-
                  <p>Starts a speaker search task.</p> <important> <p>Before
                  starting any speaker search tasks, you must provide all
                  notices and obtain all consents from the speaker as required
                  under applicable privacy and biometrics laws, and as required
                  under the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks?operation=start:
              POST:
                summary: StartVoiceToneAnalysisTask
                description: >-
                  <p>Starts a voice tone analysis task. For more information
                  about voice tone analysis, see <a
                  href="https://docs.aws.amazon.com/chime-sdk/latest/dg/voice-analytics.html">Using
                  Amazon Chime SDK voice analytics</a> in the <i>Amazon Chime
                  SDK Developer Guide</i>.</p> <important> <p>Before starting
                  any voice tone analysis tasks, you must provide all notices
                  and obtain all consents from the speaker as required under
                  applicable privacy and biometrics laws, and as required under
                  the <a href="https://aws.amazon.com/service-terms/">AWS
                  service terms</a> for the Amazon Chime SDK.</p> </important>
                tags:
                  - Start
                  - Voice
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - Voice
            /media-insights-pipelines/{identifier}/speaker-search-tasks/{speakerSearchTaskId}?operation=stop:
              POST:
                summary: StopSpeakerSearchTask
                description: <p>Stops a speaker search task.</p>
                tags:
                  - Stop
                  - Speakers
                  - Search
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - Voice
                  - '?operation=stop'
            /media-insights-pipelines/{identifier}/voice-tone-analysis-tasks/{voiceToneAnalysisTaskId}?operation=stop:
              POST:
                summary: StopVoiceToneAnalysisTask
                description: <p>Stops a voice tone analysis task.</p>
                tags:
                  - Stop
                  - Voice
                  - Tone
                  - Analysis
                  - Tasks
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - Voice
                  - '?operation=stop'
            /tags?operation=tag-resource:
              POST:
                summary: TagResource
                description: >-
                  <p>The ARN of the media pipeline that you want to tag.
                  Consists of the pipeline's endpoint region, resource ID, and
                  pipeline ID.</p>
                tags:
                  - Tags
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - Voice
                  - '?operation=stop'
                  - Tags
                  - Resources
            /tags?operation=untag-resource:
              POST:
                summary: UntagResource
                description: <p>Removes any tags from a media pipeline.</p>
                tags:
                  - Untag
                  - Resources
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - Voice
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
            /media-insights-pipeline-status/{identifier}:
              PUT:
                summary: UpdateMediaInsightsPipelineStatus
                description: <p>Updates the status of a media insights pip
                tags:
                  - Update
                  - Media
                  - Insights
                  - Pipelines
                  - Status
                  - SDKs
                  - Media
                  - Capture
                  - Pipelines
                  - Concatenation
                  - Insights
                  - Pipelines
                  - Configurations
                  - Live
                  - Connectors
                  - Kinesis
                  - Videos
                  - Stream
                  - Pools
                  - Identifiers
                  - Identifiers
                  - Search
                  - Tasks
                  - Tone
                  - Analysis
                  - Tags
                  - Speakers
                  - Tasks
                  - Voice
                  - '?operation=stop'
                  - Tags
                  - Resources
                  - Tags
                  - Stat
    overlays:
      - type: APIs.io Search
        url: overlays/chime-sdk-media-pipelines-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-sdk-media-pipelines-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime-sdk-media-pipelines
  - aid: bigcommerce:orders
    name: Orders
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Orders V3
            version: ''
            license:
              name: ''
          tags:
            - name: Metafields
            - name: Payment Actions
            - name: Transactions
            - name: Order Settings
            - name: Batch metafields
          paths:
            /orders/{order_id}/payment_actions/capture:
              post:
                summary: Capture order payment
                description: >-
                  Capture the payment for an order. When there are no payment
                  method validation issues, the capture process is successful,
                  the `payment_status` updates to `capture pending`, and the
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.

                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Capture
                  - Order
                  - Payment
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/void:
              post:
                summary: Void
                description: >-
                  Void the payment for an order. When there are no payment
                  method validation issues, the void process is successful, the
                  `payment_status` updates to `void pending`, and the void
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Void
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
              parameters:
                - null
                - null
            /orders/{order_id}/transactions:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Transactions
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                description: >-
                  Returns an **orderʼs** transactions.


                  **Usage Notes**

                  * Depending on the payment method, different information will
                  be available (not all payment gateways return full card or
                  fraud detail).



                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`
                summary: Get Transactions
            /orders/{order_id}/payment_actions/refund_quotes:
              post:
                summary: Create a Refund Quote
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Quote
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/refunds:
              post:
                summary: Create a Refund
                description: >-
                  Creates a refund. When there are no payment method validation
                  issues, the refund process is successful and the refund
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              get:
                summary: Get Refunds for Order
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order for the given order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - Refunds
                  - For
                  - Order
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              parameters:
                - null
                - null
            /orders/payment_actions/refunds/{refund_id}:
              parameters:
                - null
                - null
              get:
                summary: Get a Refund
                description: Returns a refund by refund ID.
                tags:
                  - Get
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refunds:
              parameters:
                - null
              get:
                summary: Get All Refunds
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - All
                  - Refunds
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refund_quotes:
              post:
                summary: Create Refund Quotes - BATCH
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  This endpoint will accept a batch of one or more.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Create
                  - Refund
                  - Quotes
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/{order_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Order Metafields
                tags:
                  - Get
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >
                  Gets a `Metafield` object list, by `order_id`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              post:
                summary: Create Metafields
                tags:
                  - Create
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >-
                  Creates an order `Metafield`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
            /orders/{order_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Metafield
                tags:
                  - Get
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Gets a `Metafield`, by `order_id`.
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a `Metafield` object.


                  The maxiumum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              delete:
                summary: Delete a Metafield
                tags:
                  - Delete
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Deletes a `Metafield`.
            /orders/settings:
              get:
                summary: Get Global Order Settings
                description: Returns global order settings.
                tags:
                  - Get
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              put:
                summary: Update Global Order Settings
                description: Updates global order settings.
                tags:
                  - Update
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              parameters:
                - null
            /orders/settings/channels/{channel_id}:
              get:
                summary: Get Channel Order Settings
                description: Returns order settings for a specific channel.
                tags:
                  - Get
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Order Settings
                description: |-
                  Updates order settings for a specific channel.

                   **Note:** You must override both notifications `email_addresses` or neither, i.e. either both notification `email_addresses` are an array of valid email addresses, or both `email_addresses` must be null. You may not have one set to an array of addresses and the other set to `null`.
                tags:
                  - Update
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              parameters:
                - null
                - null
            /orders/metafields:
              get:
                summary: Get All Order Metafields
                tags:
                  - Get
                  - All
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Get all order metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Delete all order
    overlays:
      - type: APIs.io Search
        url: overlays/orders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/orders-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:orders
    name: Orders
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.bigcommerce.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.bigcommerce.com/
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: Orders V3
            version: ''
            license:
              name: ''
          tags:
            - name: Metafields
            - name: Payment Actions
            - name: Transactions
            - name: Order Settings
            - name: Batch metafields
          paths:
            /orders/{order_id}/payment_actions/capture:
              post:
                summary: Capture order payment
                description: >-
                  Capture the payment for an order. When there are no payment
                  method validation issues, the capture process is successful,
                  the `payment_status` updates to `capture pending`, and the
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.

                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Capture
                  - Order
                  - Payment
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/void:
              post:
                summary: Void
                description: >-
                  Void the payment for an order. When there are no payment
                  method validation issues, the void process is successful, the
                  `payment_status` updates to `void pending`, and the void
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Void
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
              parameters:
                - null
                - null
            /orders/{order_id}/transactions:
              parameters:
                - null
                - null
              get:
                tags:
                  - Get
                  - Transactions
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                description: >-
                  Returns an **orderʼs** transactions.


                  **Usage Notes**

                  * Depending on the payment method, different information will
                  be available (not all payment gateways return full card or
                  fraud detail).



                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`
                summary: Get Transactions
            /orders/{order_id}/payment_actions/refund_quotes:
              post:
                summary: Create a Refund Quote
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Quote
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
              parameters:
                - null
                - null
            /orders/{order_id}/payment_actions/refunds:
              post:
                summary: Create a Refund
                description: >-
                  Creates a refund. When there are no payment method validation
                  issues, the refund process is successful and the refund
                  payment request is scheduled. The payment request itself
                  occurs asynchronously.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`


                  **Note:**

                  Order refunds are processed consecutively. Processing
                  synchronous refunds on an order are not yet supported.
                tags:
                  - Create
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              get:
                summary: Get Refunds for Order
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order for the given order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - Refunds
                  - For
                  - Order
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
              parameters:
                - null
                - null
            /orders/payment_actions/refunds/{refund_id}:
              parameters:
                - null
                - null
              get:
                summary: Get a Refund
                description: Returns a refund by refund ID.
                tags:
                  - Get
                  - Refund
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refunds:
              parameters:
                - null
              get:
                summary: Get All Refunds
                description: >-
                  Returns a list of refunds ordered by refund ID in ascending
                  order.


                  Requires at least one of the following scopes:

                  * `store_v2_transactions_read_only`

                  * `store_v2_transactions`

                  * `store_v2_orders_read_only`

                  * `store_v2_orders`
                tags:
                  - Get
                  - All
                  - Refunds
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/payment_actions/refund_quotes:
              post:
                summary: Create Refund Quotes - BATCH
                description: >-
                  Calculate the tax amount, total refund amount and get
                  available payment options for an order refund by providing
                  items and costs or quantities to refund.


                  This endpoint will accept a batch of one or more.


                  Requires at least one of the following scopes:

                  * `store_v2_orders`

                  * `store_v2_transactions`
                tags:
                  - Create
                  - Refund
                  - Quotes
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
            /orders/{order_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Order Metafields
                tags:
                  - Get
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >
                  Gets a `Metafield` object list, by `order_id`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              post:
                summary: Create Metafields
                tags:
                  - Create
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                description: >-
                  Creates an order `Metafield`.


                  The maximum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
            /orders/{order_id}/metafields/{metafield_id}:
              parameters:
                - null
                - null
                - null
              get:
                summary: Get a Metafield
                tags:
                  - Get
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Gets a `Metafield`, by `order_id`.
              put:
                summary: Update a Metafield
                tags:
                  - Update
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: >-
                  Updates a `Metafield` object.


                  The maxiumum number of metafields allowed on each order,
                  product, category, variant, or brand is 250 per client ID.
              delete:
                summary: Delete a Metafield
                tags:
                  - Delete
                  - Metafield
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                description: |
                  Deletes a `Metafield`.
            /orders/settings:
              get:
                summary: Get Global Order Settings
                description: Returns global order settings.
                tags:
                  - Get
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              put:
                summary: Update Global Order Settings
                description: Updates global order settings.
                tags:
                  - Update
                  - Global
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
              parameters:
                - null
            /orders/settings/channels/{channel_id}:
              get:
                summary: Get Channel Order Settings
                description: Returns order settings for a specific channel.
                tags:
                  - Get
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Order Settings
                description: |-
                  Updates order settings for a specific channel.

                   **Note:** You must override both notifications `email_addresses` or neither, i.e. either both notification `email_addresses` are an array of valid email addresses, or both `email_addresses` must be null. You may not have one set to an array of addresses and the other set to `null`.
                tags:
                  - Update
                  - Channel
                  - Order
                  - Settings
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
              parameters:
                - null
                - null
            /orders/metafields:
              get:
                summary: Get All Order Metafields
                tags:
                  - Get
                  - All
                  - Order
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Get all order metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Orders
                  - Order_id
                  - Payment_actions
                  - Capture
                  - Void
                  - Transactions
                  - Refund_quotes
                  - Refunds
                  - Refund_id
                  - Metafields
                  - Metafield_id
                  - Settings
                  - Channels
                  - Channel_id
                description: Delete all order
    overlays:
      - type: APIs.io Search
        url: overlays/orders-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/orders-openapi-api-evangelist-ratings.yml
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
  - aid: stripe:stripe-payment-intents-api
    name: Stripe Payment Intents API
    description: >-
      A PaymentIntent guides you through the process of collecting a payment
      from your customer. We recommend that you create exactly one PaymentIntent
      for each order or customer session in your system. You can reference the
      PaymentIntent later to see the history of payment attempts for a
      particular session.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/api/payment_intents
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/api/payment_intents
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Payment Intents API
          paths:
            /v1/payment_intents:
              get:
                description: <p>Returns a list of PaymentIntents.</p>
                tags:
                  - V1
                  - Payment_intents
              post:
                description: >-
                  <p>Creates a PaymentIntent object.</p>


                  <p>After the PaymentIntent is created, attach a payment method
                  and <a href="/docs/api/payment_intents/confirm">confirm</a>

                  to continue the payment. Learn more about <a
                  href="/docs/payments/payment-intents">the available payment
                  flows

                  with the Payment Intents API</a>.</p>


                  <p>When you use <code>confirm=true</code> during creation,
                  it’s equivalent to creating

                  and confirming the PaymentIntent in the same call. You can use
                  any parameters

                  available in the <a
                  href="/docs/api/payment_intents/confirm">confirm API</a> when
                  you supply

                  <code>confirm=true</code>.</p>
                tags:
                  - V1
                  - Payment_intents
            /v1/payment_intents/search:
              get:
                description: >-
                  <p>Search for PaymentIntents you’ve previously created using
                  Stripe’s <a href="/docs/search#search-query-language">Search
                  Query Language</a>.

                  Don’t use search in read-after-write flows where strict
                  consistency is necessary. Under normal operating

                  conditions, data is searchable in less than a minute.
                  Occasionally, propagation of new or updated data can be up

                  to an hour behind during outages. Search functionality is not
                  available to merchants in India.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
            /v1/payment_intents/{intent}:
              get:
                description: >-
                  <p>Retrieves the details of a PaymentIntent that has
                  previously been created. </p>


                  <p>You can retrieve a PaymentIntent client-side using a
                  publishable key when the <code>client_secret</code> is in the
                  query string. </p>


                  <p>If you retrieve a PaymentIntent with a publishable key, it
                  only returns a subset of properties. Refer to the <a
                  href="#payment_intent_object">payment intent</a> object
                  reference for more details.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
              post:
                description: >-
                  <p>Updates properties on a PaymentIntent object without
                  confirming.</p>


                  <p>Depending on which properties you update, you might need to
                  confirm the

                  PaymentIntent again. For example, updating the
                  <code>payment_method</code>

                  always requires you to confirm the PaymentIntent again. If you
                  prefer to

                  update and confirm at the same time, we recommend updating
                  properties through

                  the <a href="/docs/api/payment_intents/confirm">confirm
                  API</a> instead.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
            /v1/payment_intents/{intent}/apply_customer_balance:
              post:
                description: >-
                  <p>Manually reconcile the remaining amount for a
                  <code>customer_balance</code> PaymentIntent.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
                  - Apply_customer_balance
            /v1/payment_intents/{intent}/cancel:
              post:
                description: >-
                  <p>You can cancel a PaymentIntent object when it’s in one of
                  these statuses: <code>requires_payment_method</code>,
                  <code>requires_capture</code>,
                  <code>requires_confirmation</code>,
                  <code>requires_action</code> or, <a
                  href="/docs/payments/intents">in rare cases</a>,
                  <code>processing</code>. </p>


                  <p>After it’s canceled, no additional charges are made by the
                  PaymentIntent and any operations on the PaymentIntent fail
                  with an error. For PaymentIntents with a <code>status</code>
                  of <code>requires_capture</code>, the remaining
                  <code>amount_capturable</code> is automatically refunded. </p>


                  <p>You can’t cancel the PaymentIntent for a Checkout Session.
                  <a href="/docs/api/checkout/sessions/expire">Expire the
                  Checkout Session</a> instead.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
                  - Apply_customer_balance
                  - Cancel
            /v1/payment_intents/{intent}/capture:
              post:
                description: >-
                  <p>Capture the funds of an existing uncaptured PaymentIntent
                  when its status is <code>requires_capture</code>.</p>


                  <p>Uncaptured PaymentIntents are cancelled a set number of
                  days (7 by default) after their creation.</p>


                  <p>Learn more about <a
                  href="/docs/payments/capture-later">separate authorization and
                  capture</a>.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
                  - Apply_customer_balance
                  - Cancel
                  - Capture
            /v1/payment_intents/{intent}/confirm:
              post:
                description: >-
                  <p>Confirm that your customer intends to pay with current or
                  provided

                  payment method. Upon confirmation, the PaymentIntent will
                  attempt to initiate

                  a payment.

                  If the selected payment method requires additional
                  authentication steps, the

                  PaymentIntent will transition to the
                  <code>requires_action</code> status and

                  suggest additional actions via <code>next_action</code>. If
                  payment fails,

                  the PaymentIntent transitions to the
                  <code>requires_payment_method</code> status or the

                  <code>canceled</code> status if the confirmation limit is
                  reached. If

                  payment succeeds, the PaymentIntent will transition to the
                  <code>succeeded</code>

                  status (or <code>requires_capture</code>, if
                  <code>capture_method</code> is set to <code>manual</code>).

                  If the <code>confirmation_method</code> is
                  <code>automatic</code>, payment may be attempted

                  using our <a
                  href="/docs/stripe-js/reference#stripe-handle-card-payment">client
                  SDKs</a>

                  and the PaymentIntent’s <a
                  href="#payment_intent_object-client_secret">client_secret</a>.

                  After <code>next_action</code>s are handled by the client, no
                  additional

                  confirmation is required to complete the payment.

                  If the <code>confirmation_method</code> is
                  <code>manual</code>, all payment attempts must be

                  initiated using a secret key.

                  If any actions are required for the payment, the PaymentIntent
                  will

                  return to the <code>requires_confirmation</code> state

                  after those actions are completed. Your server needs to then

                  explicitly re-confirm the PaymentIntent to initiate the next
                  payment

                  attempt. Read the <a
                  href="/docs/payments/payment-intents/web-manual">expanded
                  documentation</a>

                  to learn more about manual confirmation.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
                  - Apply_customer_balance
                  - Cancel
                  - Capture
                  - Confirm
            /v1/payment_intents/{intent}/increment_authorization:
              post:
                description: >-
                  <p>Perform an incremental authorization on an eligible

                  <a href="/docs/api/payment_intents/object">PaymentIntent</a>.
                  To be eligible, the

                  PaymentIntent’s status must be <code>requires_capture</code>
                  and

                  <a
                  href="/docs/api/charges/object#charge_object-payment_method_details-card_present-incremental_authorization_supported">incremental_authorization_supported</a>

                  must be <code>true</code>.</p>


                  <p>Incremental authorizations attempt to increase the
                  authorized amount on

                  your customer’s card to the new, higher <code>amount</code>
                  provided. Similar to the

                  initial authorization, incremental authorizations can be
                  declined. A

                  single PaymentIntent can call this endpoint multiple times to
                  further

                  increase the authorized amount.</p>


                  <p>If the incremental authorization succeeds, the
                  PaymentIntent object

                  returns with the updated

                  <a
                  href="/docs/api/payment_intents/object#payment_intent_object-amount">amount</a>.

                  If the incremental authorization fails, a

                  <a href="/docs/error-codes#card-declined">card_declined</a>
                  error returns, and no other

                  fields on the PaymentIntent or Charge update. The
                  PaymentIntent

                  object remains capturable for the previously authorized
                  amount.</p>


                  <p>Each PaymentIntent can have a maximum of 10 incremental
                  authorization attempts, including declines.

                  After it’s captured, a PaymentIntent can no longer be
                  incremented.</p>


                  <p>Learn more about <a
                  href="/docs/terminal/features/incremental-authorizations">incremental
                  authorizations</a>.</p>
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
                  - Apply_customer_balance
                  - Cancel
                  - Capture
                  - Confirm
                  - Increment_authorization
            /v1/payment_intents/{intent}/verify_microdeposits:
              post:
                description: <p>Verifies microdeposits on a PaymentIntent o
                tags:
                  - V1
                  - Payment_intents
                  - Search
                  - Intent
                  - Apply_customer_balance
                  - Cancel
                  - Capture
                  - Confirm
                  - Increment_authorization
                  - Verify_microdeposi
    overlays:
      - type: APIs.io Search
        url: overlays/payment-intents-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payment-intents-openapi-api-evangelist-ratings.yml
  - aid: stripe:stripe-test-helpers-api
    name: Stripe Test Helpers API
    description: >-
      Stripe provides a number of resources for testing your integration. Make
      sure to test the following use cases before launch, and use our Postman
      collection to make the testing process simpler.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/implementation-guides/billing/testing
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/implementation-guides/billing/testing
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Test Helpers API
          paths:
            /v1/test_helpers/customers/{customer}/fund_cash_balance:
              post:
                description: <p>Create an incoming testmode bank transfer</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
            /v1/test_helpers/issuing/authorizations:
              post:
                description: <p>Create a test-mode authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
            /v1/test_helpers/issuing/authorizations/{authorization}/capture:
              post:
                description: <p>Capture a test-mode authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
            /v1/test_helpers/issuing/authorizations/{authorization}/expire:
              post:
                description: <p>Expire a test-mode Authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
            /v1/test_helpers/issuing/authorizations/{authorization}/increment:
              post:
                description: <p>Increment a test-mode Authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
            /v1/test_helpers/issuing/authorizations/{authorization}/reverse:
              post:
                description: <p>Reverse a test-mode Authorization.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
            /v1/test_helpers/issuing/cards/{card}/shipping/deliver:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>delivered</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
            /v1/test_helpers/issuing/cards/{card}/shipping/fail:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>failure</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
            /v1/test_helpers/issuing/cards/{card}/shipping/return:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>returned</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
            /v1/test_helpers/issuing/cards/{card}/shipping/ship:
              post:
                description: >-
                  <p>Updates the shipping status of the specified Issuing
                  <code>Card</code> object to <code>shipped</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
            /v1/test_helpers/issuing/transactions/create_force_capture:
              post:
                description: >-
                  <p>Allows the user to capture an arbitrary amount, also known
                  as a forced capture.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
            /v1/test_helpers/issuing/transactions/create_unlinked_refund:
              post:
                description: >-
                  <p>Allows the user to refund an arbitrary amount, also known
                  as a unlinked refund.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
            /v1/test_helpers/issuing/transactions/{transaction}/refund:
              post:
                description: <p>Refund a test-mode Transaction.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
            /v1/test_helpers/refunds/{refund}/expire:
              post:
                description: >-
                  <p>Expire a refund with a status of
                  <code>requires_action</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
            /v1/test_helpers/terminal/readers/{reader}/present_payment_method:
              post:
                description: >-
                  <p>Presents a payment method on a simulated reader. Can be
                  used to simulate accepting a payment, saving a card or
                  refunding a transaction.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
            /v1/test_helpers/test_clocks:
              get:
                description: <p>Returns a list of your test clocks.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
              post:
                description: >-
                  <p>Creates a new test clock that can be attached to new
                  customers and quotes.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
            /v1/test_helpers/test_clocks/{test_clock}:
              delete:
                description: <p>Deletes a test clock.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
              get:
                description: <p>Retrieves a test clock.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
            /v1/test_helpers/test_clocks/{test_clock}/advance:
              post:
                description: >-
                  <p>Starts advancing a test clock to a specified time in the
                  future. Advancement is done when status changes to
                  <code>Ready</code>.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
            /v1/test_helpers/treasury/inbound_transfers/{id}/fail:
              post:
                description: >-
                  <p>Transitions a test mode created InboundTransfer to the
                  <code>failed</code> status. The InboundTransfer must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
            /v1/test_helpers/treasury/inbound_transfers/{id}/return:
              post:
                description: >-
                  <p>Marks the test mode InboundTransfer object as returned and
                  links the InboundTransfer to a ReceivedDebit. The
                  InboundTransfer must already be in the <code>succeeded</code>
                  state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
            /v1/test_helpers/treasury/inbound_transfers/{id}/succeed:
              post:
                description: >-
                  <p>Transitions a test mode created InboundTransfer to the
                  <code>succeeded</code> status. The InboundTransfer must
                  already be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
            /v1/test_helpers/treasury/outbound_payments/{id}/fail:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundPayment to the
                  <code>failed</code> status. The OutboundPayment must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
            /v1/test_helpers/treasury/outbound_payments/{id}/post:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundPayment to the
                  <code>posted</code> status. The OutboundPayment must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
            /v1/test_helpers/treasury/outbound_payments/{id}/return:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundPayment to the
                  <code>returned</code> status. The OutboundPayment must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
            /v1/test_helpers/treasury/outbound_transfers/{outbound_transfer}/fail:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundTransfer to the
                  <code>failed</code> status. The OutboundTransfer must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
            /v1/test_helpers/treasury/outbound_transfers/{outbound_transfer}/post:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundTransfer to the
                  <code>posted</code> status. The OutboundTransfer must already
                  be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
            /v1/test_helpers/treasury/outbound_transfers/{outbound_transfer}/return:
              post:
                description: >-
                  <p>Transitions a test mode created OutboundTransfer to the
                  <code>returned</code> status. The OutboundTransfer must
                  already be in the <code>processing</code> state.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
            /v1/test_helpers/treasury/received_credits:
              post:
                description: >-
                  <p>Use this endpoint to simulate a test mode ReceivedCredit
                  initiated by a third party. In live mode, you can’t directly
                  create ReceivedCredits initiated by third parties.</p>
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
                  - Received_credits
            /v1/test_helpers/treasury/received_debits:
              post:
                description: >-
                  <p>Use this endpoint to simulate a test mode ReceivedDebit
                  initiated by a third party. In live mode, you can’t directly
                  create ReceivedDebits initiated by third pa
                tags:
                  - V1
                  - Test_helpers
                  - Customers
                  - Customer
                  - Fund_cash_balance
                  - Issuing
                  - Authorizations
                  - Authorization
                  - Capture
                  - Expire
                  - Increment
                  - Reverse
                  - Cards
                  - Card
                  - Shipping
                  - Deliver
                  - Fail
                  - Return
                  - Ship
                  - Transactions
                  - Create_force_capture
                  - Create_unlinked_refund
                  - Transaction
                  - Refund
                  - Refunds
                  - Terminal
                  - Readers
                  - Reader
                  - Present_payment_method
                  - Test_clocks
                  - Test_clock
                  - Advance
                  - Treasury
                  - Inbound_transfers
                  - Id
                  - Succeed
                  - Outbound_payments
                  - Post
                  - Outbound_transfers
                  - Outbound_transfer
                  - Received_credits
                  - Received_debi
    overlays:
      - type: APIs.io Search
        url: overlays/test-helpers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/test-helpers-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---