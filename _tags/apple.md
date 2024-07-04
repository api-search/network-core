---
name: Apple
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/apple.png
url: https://example.com/apis/apple.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Apple
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
            - name: Payment links
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
                  - An
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
  - name: Adyen Management API
    description: >-
      Configure and manage your Adyen company and merchant accounts, stores, and
      payment terminals.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/api-explorer/Management/3/overview
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/api-explorer/Management/3/overview
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Management API
          tags:
            - name: Account - company level
            - name: Account - merchant level
            - name: Account - store level
            - name: Payout settings - merchant level
            - name: Users - company level
            - name: Users - merchant level
            - name: My API credential
            - name: API credentials - company level
            - name: API credentials - merchant level
            - name: API key - company level
            - name: API key - merchant level
            - name: Client key - company level
            - name: Client key - merchant level
            - name: Allowed origins - company level
            - name: Allowed origins - merchant level
            - name: Webhooks - company level
            - name: Webhooks - merchant level
            - name: Payment methods - merchant level
            - name: Terminals - terminal level
            - name: Terminal actions - company level
            - name: Terminal actions - terminal level
            - name: Terminal orders - company level
            - name: Terminal orders - merchant level
            - name: Terminal settings - company level
            - name: Terminal settings - merchant level
            - name: Terminal settings - store level
            - name: Terminal settings - terminal level
            - name: Android files - company level
            - name: Split configuration - merchant level
          paths:
            /companies:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Companies
                  - Accounts
                  - Companies
                summary: Get a list of company accounts
                description: >-
                  Returns the list of company accounts that your API credential
                  has access to. The list is grouped into pages as defined by
                  the query parameters.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):


                  * Management API—Account read
            /companies/{companyId}:
              get:
                tags:
                  - Get
                  - Companies
                  - Account
                  - Companies
                  - Identifiers
                summary: Get a company account
                description: >-
                  Returns the company account specified in the path. Your API
                  credential must have access to the company account. 


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Account read
            /companies/{companyId}/androidApps:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Android
                  - Applications
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                summary: Get a list of Android apps
                description: >-
                  Returns a list of the Android apps that are available for the
                  company identified in the path. 

                  These apps have been uploaded to Adyen and can be installed or
                  uninstalled on Android payment terminals through [terminal
                  actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Android files read

                  * Management API—Android files read and write

                  * Management API—Terminal actions read

                  * Management API—Terminal actions read and write
              post:
                tags:
                  - Uploads
                  - Android
                  - Applications
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                summary: Upload Android App
                description: >-
                  Uploads an Android APK file to Adyen.

                  The maximum APK file size is 200 MB.

                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Android files read and write


                  >By choosing to upload, install, or run any third-party
                  applications on an Adyen payment terminal, you accept full
                  responsibility and liability for any consequences of
                  uploading, installing, or running any such applications.
            /companies/{companyId}/androidApps/{id}:
              get:
                tags:
                  - Get
                  - Android
                  - Applications
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                summary: Get Android app
                description: >-
                  Returns the details of the Android app identified in the
                  path. 

                  These apps have been uploaded to Adyen and can be installed or
                  uninstalled on Android payment terminals through [terminal
                  actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Android files read

                  * Management API—Android files read and write
            /companies/{companyId}/androidCertificates:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Android
                  - Certificates
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                summary: Get a list of Android certificates
                description: >-
                  Returns a list of the Android certificates that are available
                  for the company identified in the path.

                  Typically, these certificates enable running apps on Android
                  payment terminals. The certifcates in the list have been
                  uploaded to Adyen and can be installed or uninstalled on
                  Android terminals through [terminal
                  actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Android files read

                  * Management API—Android files read and write

                  * Management API—Terminal actions read

                  * Management API—Terminal actions read and write
            /companies/{companyId}/apiCredentials:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                summary: Get a list of API credentials
                description: >-
                  Returns the list of [API
                  credentials](https://docs.adyen.com/development-resources/api-credentials)
                  for the company account. The list is grouped into pages as
                  defined by the query parameters.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              post:
                tags:
                  - Create
                  - An
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                summary: Create an API credential.
                description: >-
                  Creates an [API
                  credential](https://docs.adyen.com/development-resources/api-credentials)
                  for the company account identified in the path. In the
                  request, you can specify which merchant accounts the new API
                  credential will have access to, as well as its roles and
                  allowed origins.


                  The response includes several types of authentication details:

                  * [API
                  key](https://docs.adyen.com/development-resources/api-authentication#api-key-authentication):
                  used for API request authentication.

                  * [Client
                  key](https://docs.adyen.com/development-resources/client-side-authentication#how-it-works):
                  public key used for client-side authentication.

                  * [Username and
                  password](https://docs.adyen.com/development-resources/api-authentication#using-basic-authentication):
                  used for basic authentication.


                  > Make sure you store the API key securely in your system. You
                  won't be able to retrieve it later.


                  If your API key is lost or compromised, you need to [generate
                  a new API
                  key](https://docs.adyen.com/api-explorer/#/ManagementService/v1/post/companies/{companyId}/apiCredentials/{apiCredentialId}/generateApiKey).


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /companies/{companyId}/apiCredentials/{apiCredentialId}:
              get:
                tags:
                  - Get
                  - An
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                summary: Get an API credential
                description: >-
                  Returns the [API
                  credential](https://docs.adyen.com/development-resources/api-credentials)
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              patch:
                tags:
                  - Update
                  - An
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                summary: Update an API credential.
                description: >-
                  Changes the API credential's roles, merchant account access,
                  or allowed origins. The request has the new values for the
                  fields you want to change. The response contains the full
                  updated API credential, including the new values from the
                  request. 


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /companies/{companyId}/apiCredentials/{apiCredentialId}/allowedOrigins:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Allowed
                  - Origins
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                summary: Get a list of allowed origins
                description: >-
                  Returns the list of [allowed
                  origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  for the API credential identified in the path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              post:
                tags:
                  - Create
                  - An
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                summary: Create an allowed origin
                description: >-
                  Adds a new [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  to the API credential's list of allowed origins.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /companies/{companyId}/apiCredentials/{apiCredentialId}/allowedOrigins/{originId}:
              delete:
                tags:
                  - Delete
                  - An
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                summary: Delete an allowed origin
                description: >-
                  Removes the [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  identified in the path. As soon as an allowed origin is
                  removed, we no longer accept client-side requests from that
                  domain.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              get:
                tags:
                  - Get
                  - An
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                summary: Get an allowed origin
                description: >-
                  Returns the [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /companies/{companyId}/apiCredentials/{apiCredentialId}/generateApiKey:
              post:
                tags:
                  - Generate
                  - New
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                summary: Generate new API key
                description: >-
                  Returns a new API key for the API credential. You can use the
                  new API key a few minutes after generating it. The old API key
                  stops working 24 hours after generating a new one.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /companies/{companyId}/apiCredentials/{apiCredentialId}/generateClientKey:
              post:
                tags:
                  - Generate
                  - New
                  - Client
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                summary: Generate new client key
                description: >-
                  Returns a new [client
                  key](https://docs.adyen.com/development-resources/client-side-authentication#how-it-works)
                  for the API credential identified in the path. You can use the
                  new client key a few minutes after generating it. The old
                  client key stops working 24 hours after generating a new one.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /companies/{companyId}/billingEntities:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Billing
                  - Entities
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                summary: Get a list of billing entities
                description: >-
                  Returns the billing entities of the company identified in the
                  path and all merchant accounts belonging to the company.

                  A billing entity is a legal entity where we charge orders to.
                  An order for terminal products must contain the ID of a
                  billing entity.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
            /companies/{companyId}/merchants:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Merchants
                  - Accounts
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                summary: Get a list of merchant accounts
                description: >-
                  Returns the list of merchant accounts under the company
                  account specified in the path. The list only includes merchant
                  accounts that your API credential has access to. The list is
                  grouped into pages as defined by the query parameters. 


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Account read
            /companies/{companyId}/shippingLocations:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Shipping
                  - Locations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                summary: Get a list of shipping locations
                description: >-
                  Returns the shipping locations for the company identified in
                  the path and all merchant accounts belonging to the company.

                  A shipping location includes the address where orders can be
                  delivered, and an ID which you need to specify when ordering
                  terminal products.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
              post:
                tags:
                  - Create
                  - Shipping
                  - Locations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                summary: Create a shipping location
                description: >-
                  Creates a shipping location for the company identified in the
                  path. A shipping location defines an address where orders can
                  be delivered.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write
            /companies/{companyId}/terminalActions:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Terminal
                  - Actions
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                summary: Get a list of terminal actions
                description: >-
                  Returns the [terminal
                  actions](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api)
                  that have been scheduled for the company identified in the
                  path.The response doesn't include actions that are scheduled
                  by Adyen.

                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal actions read

                  * Management API—Terminal actions read and write
            /companies/{companyId}/terminalActions/{actionId}:
              get:
                tags:
                  - Get
                  - Terminal
                  - Actions
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                summary: Get terminal action
                description: >-
                  Returns the details of the [terminal
                  action](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api)
                  identified in the path.

                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal actions read

                  * Management API—Terminal actions read and write
            /companies/{companyId}/terminalLogos:
              get:
                tags:
                  - Get
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                summary: Get the terminal logo
                description: >-
                  Returns the logo that is configured for a specific payment
                  terminal model at the company identified in the path. 


                  The logo is returned as a Base64-encoded string. You need to
                  Base64-decode the string to get the actual image file. 

                  This logo applies to all terminals of the specified model
                  under the company, unless a different logo is configured at a
                  lower level (merchant account, store, or individual terminal).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write
              patch:
                tags:
                  - Update
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                summary: Update the terminal logo
                description: >-
                  Updates the logo that is configured for a specific payment
                  terminal model at the company identified in the path. You can
                  update the logo for only one terminal model at a time.

                  This logo applies to all terminals of the specified model
                  under the company, unless a different logo is configured at a
                  lower level (merchant account, store, or individual
                  terminal). 

                  * To change the logo, specify the image file as a
                  Base64-encoded string.

                  * To restore the logo inherited from the Adyen PSP level,
                  specify an empty logo value.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write
            /companies/{companyId}/terminalModels:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Terminal
                  - Models
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                summary: Get a list of terminal models
                description: >-
                  Returns a list of payment terminal models that the company
                  identified in the path has access to.

                  The response includes the terminal model ID, which can be used
                  as a query parameter when getting a list of terminals or a
                  list of products for ordering.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
            /companies/{companyId}/terminalOrders:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                summary: Get a list of orders
                description: >-
                  Returns a lists of terminal products orders for the company
                  identified in the path.

                  To filter the list, use one or more of the query parameters.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
              post:
                tags:
                  - Create
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                summary: Create an order
                description: >-
                  Creates an order for payment terminal products for the company
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write

                  >Requests to the Management API test endpoint do not create
                  actual orders for test terminals. To order test terminals, you
                  need to [submit a sales
                  order](https://docs.adyen.com/point-of-sale/managing-terminals/order-terminals/#sales-order-steps)
                  in your Customer Area.
            /companies/{companyId}/terminalOrders/{orderId}:
              get:
                tags:
                  - Get
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                summary: Get an order
                description: >-
                  Returns the details of the terminal products order identified
                  in the path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
              patch:
                tags:
                  - Update
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                summary: Update an order
                description: >-
                  Updates the terminal products order identified in the path.

                  Updating is only possible while the order has the status
                  **Placed**.


                  The request body only needs to contain what you want to
                  change. 

                  However, to update the products in the `items` array, you must
                  provide the entire array. For example, if the array has three
                  items:
                   To remove one item, the array must include the remaining two items. Or to add one item, the array must include all four items.

                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write
            /companies/{companyId}/terminalOrders/{orderId}/cancel:
              post:
                tags:
                  - Cancel
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                summary: Cancel an order
                description: >-
                  Cancels the terminal products order identified in the path.

                  Cancelling is only possible while the order has the status
                  **Placed**.

                  To cancel an order, make a POST call without a request body.
                  The response returns the full order details, but with the
                  status changed to **Cancelled**.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write
            /companies/{companyId}/terminalProducts:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Terminal
                  - Products
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                summary: Get a list of terminal products
                description: >-
                  Returns a country-specific list of payment terminal packages
                  and parts that the company identified in the path has access
                  to.
                   
                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
            /companies/{companyId}/terminalSettings:
              get:
                tags:
                  - Get
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                summary: Get terminal settings
                description: >-
                  Returns the payment terminal settings that are configured for
                  the company identified in the path. These settings apply to
                  all terminals under the company, unless different values are
                  configured at a lower level (merchant account, store, or
                  individual terminal).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
              patch:
                tags:
                  - Update
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                summary: Update terminal settings
                description: >-
                  Updates payment terminal settings for the company identified
                  in the path. These settings apply to all terminals under the
                  company, unless different values are configured at a lower
                  level (merchant account, store, or individual terminal).


                  * To change a parameter value, include the full object that
                  contains the parameter, even if you don't want to change all
                  parameters in the object.

                  * To restore a parameter value inherited from the Adyen PSP
                  level, include the full object that contains the parameter,
                  and specify an empty value for the parameter or omit the
                  parameter.

                  * Objects that are not included in the request are not
                  updated.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
            /companies/{companyId}/users:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Users
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                summary: Get a list of users
                description: >
                  Returns the list of users for the `companyId` identified in
                  the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
              post:
                tags:
                  - Create
                  - New
                  - Users
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                summary: Create a new user
                description: >
                  Creates the user for the `companyId` identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
            /companies/{companyId}/users/{userId}:
              get:
                tags:
                  - Get
                  - Users
                  - Details
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                summary: Get user details
                description: >
                  Returns user details for the `userId` and the `companyId`
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
              patch:
                tags:
                  - Update
                  - Users
                  - Details
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                summary: Update user details
                description: >
                  Updates user details for the `userId` and the `companyId`
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
            /companies/{companyId}/webhooks:
              get:
                tags:
                  - Lists
                  - All
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                summary: List all webhooks
                description: >-
                  Lists all webhook configurations for the company account.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read

                  * Management API—Webhooks read and write
              post:
                tags:
                  - Sets
                  - Up
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                summary: Set up a webhook
                description: >-
                  Subscribe to receive webhook notifications about events
                  related to your company account. You can add basic
                  authentication to make sure the data is secure.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /companies/{companyId}/webhooks/{webhookId}:
              delete:
                tags:
                  - Removes
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                summary: Remove a webhook
                description: >-
                  Remove the configuration for the webhook identified in the
                  path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
              get:
                tags:
                  - Get
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                summary: Get a webhook
                description: >-
                  Returns the configuration for the webhook identified in the
                  path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read

                  * Management API—Webhooks read and write
              patch:
                tags:
                  - Update
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                summary: Update a webhook
                description: >-
                  Make changes to the configuration of the webhook identified in
                  the path. The request contains the new values you want to have
                  in the webhook configuration. The response contains the full
                  configuration for the webhook, which includes the new values
                  from the request.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /companies/{companyId}/webhooks/{webhookId}/generateHmac:
              post:
                tags:
                  - Generate
                  - An
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                summary: Generate an HMAC key
                description: >-
                  Returns an [HMAC key](https://en.wikipedia.org/wiki/HMAC) for
                  the webhook identified in the path. This key allows you to
                  check the integrity and the origin of the notifications you
                  receive.By creating an HMAC key, you start receiving
                  [HMAC-signed
                  notifications](https://docs.adyen.com/development-resources/webhooks/verify-hmac-signatures#enable-hmac-signatures)
                  from Adyen. Find out more about how to [verify HMAC
                  signatures](https://docs.adyen.com/development-resources/webhooks/verify-hmac-signatures).


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /companies/{companyId}/webhooks/{webhookId}/test:
              post:
                tags:
                  - Tests
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                summary: Test a webhook
                description: >-
                  Sends sample notifications to test if the webhook is set up
                  correctly.


                  We send sample notifications for maximum 20 of the merchant
                  accounts that the webhook is configured for. If the webhook is
                  configured for more than 20 merchant accounts, use the
                  `merchantIds` array to specify a subset of the merchant
                  accounts for which to send test notifications.


                  We send four test notifications for each event code you
                  choose. They cover success and failure scenarios for the
                  hard-coded currencies EUR and GBP, regardless of the
                  currencies configured in the merchant accounts. For custom
                  notifications, we only send the specified custom notification.


                  The response describes the result of the test. The `status`
                  field tells you if the test was successful or not. You can use
                  the other response fields to troubleshoot unsuccessful tests.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /me:
              get:
                tags:
                  - Get
                  - Credentials
                  - Details
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Get API credential details
                description: >-
                  Returns your [API
                  credential](https://docs.adyen.com/development-resources/api-credentials)
                  details based on the API Key you used in the request.


                  You can make this request with any of the Management API
                  roles.
            /me/allowedOrigins:
              get:
                tags:
                  - Get
                  - Allowed
                  - Origins
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Get allowed origins
                description: >-
                  Returns the list of [allowed
                  origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  of your [API
                  credential](https://docs.adyen.com/development-resources/api-credentials)
                  based on the API key you used in the request.


                  You can make this request with any of the Management API
                  roles.
              post:
                tags:
                  - Add
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Add allowed origin
                description: >-
                  Adds an allowed origin to the list of [allowed
                  origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  of your API credential.

                  The API key from the request is used to identify the [API
                  credential](https://docs.adyen.com/development-resources/api-credentials).


                  You can make this request with any of the Management API
                  roles.
            /me/allowedOrigins/{originId}:
              delete:
                tags:
                  - Removes
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Remove allowed origin
                description: >-
                  Removes the [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  specified in the path.

                  The API key from the request is used to identify the [API
                  credential](https://docs.adyen.com/development-resources/api-credentials).


                  You can make this request with any of the Management API
                  roles.
              get:
                tags:
                  - Get
                  - Allowed
                  - Origin
                  - Details
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Get allowed origin details
                description: >-
                  Returns the details of the [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  specified in the path.

                  The API key from the request is used to identify the [API
                  credential](https://docs.adyen.com/development-resources/api-credentials).


                  You can make this request with any of the Management API
                  roles.
            /me/generateClientKey:
              post:
                tags:
                  - Generate
                  - Client
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Generate a client key
                description: >-
                  Generates a new [client
                  key](https://docs.adyen.com/development-resources/client-side-authentication/)
                  used to authenticate requests from your payment environment.

                  You can use the new client key a few minutes after generating
                  it.

                  The old client key stops working 24 hours after generating a
                  new one.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Merchants
                  - Accounts
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Get a list of merchant accounts
                description: >-
                  Returns the list of merchant accounts that your API credential
                  has access to. The list is grouped into pages as defined by
                  the query parameters. 


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Account read
              post:
                tags:
                  - Create
                  - Merchants
                  - Account
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Create a merchant account
                description: >-
                  Creates a merchant account for the company account specified
                  in the request.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Accounts read and write
            /merchants/{merchantId}:
              get:
                tags:
                  - Get
                  - Merchants
                  - Account
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                summary: Get a merchant account
                description: >-
                  Returns the merchant account specified in the path. Your API
                  credential must have access to the merchant account.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Account read
            /merchants/{merchantId}/activate:
              post:
                tags:
                  - Request
                  - To
                  - Activate
                  - Merchants
                  - Account
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Request to activate a merchant account
                description: >-
                  Sends a request to activate the merchant account identified in
                  the path.


                  You get the result of the activation asynchronously through a
                  [`merchant.updated`](https://docs.adyen.com/api-explorer/ManagementNotification/latest/post/merchant.updated)
                  webhook. Once the merchant account is activated, you can start
                  using it to accept payments and payouts.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Accounts read and write
            /merchants/{merchantId}/apiCredentials:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Get a list of API credentials
                description: >-
                  Returns the list of [API
                  credentials](https://docs.adyen.com/development-resources/api-credentials)
                  for the merchant account. The list is grouped into pages as
                  defined by the query parameters.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              post:
                tags:
                  - Create
                  - An
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Create an API credential
                description: >-
                  Creates an [API
                  credential](https://docs.adyen.com/development-resources/api-credentials)
                  for the company account identified in the path. In the
                  request, you can specify the roles and allowed origins for the
                  new API credential.


                  The response includes the:

                  * [API
                  key](https://docs.adyen.com/development-resources/api-authentication#api-key-authentication):
                  used for API request authentication.

                  * [Client
                  key](https://docs.adyen.com/development-resources/client-side-authentication#how-it-works):
                  public key used for client-side authentication.

                  * [Username and
                  password](https://docs.adyen.com/development-resources/api-authentication#using-basic-authentication):
                  used for basic authentication.


                  > Make sure you store the API key securely in your system. You
                  won't be able to retrieve it later.


                  If your API key is lost or compromised, you need to [generate
                  a new API
                  key](https://docs.adyen.com/api-explorer/#/ManagementService/v1/post/merchants/{merchantId}/apiCredentials/{apiCredentialId}/generateApiKey).


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants/{merchantId}/apiCredentials/{apiCredentialId}:
              get:
                tags:
                  - Get
                  - An
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Get an API credential
                description: >-
                  Returns the [API
                  credential](https://docs.adyen.com/development-resources/api-credentials)
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              patch:
                tags:
                  - Update
                  - An
                  - Credentials
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Update an API credential
                description: >-
                  Changes the API credential's roles, or allowed origins. The
                  request has the new values for the fields you want to change.
                  The response contains the full updated API credential,
                  including the new values from the request. 


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants/{merchantId}/apiCredentials/{apiCredentialId}/allowedOrigins:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Allowed
                  - Origins
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Get a list of allowed origins
                description: >-
                  Returns the list of [allowed
                  origins](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  for the API credential identified in the path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              post:
                tags:
                  - Create
                  - An
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Create an allowed origin
                description: >-
                  Adds a new [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  to the API credential's list of allowed origins.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants/{merchantId}/apiCredentials/{apiCredentialId}/allowedOrigins/{originId}:
              delete:
                tags:
                  - Delete
                  - An
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Delete an allowed origin
                description: >-
                  Removes the [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  identified in the path. As soon as an allowed origin is
                  removed, we no longer accept client-side requests from that
                  domain.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
              get:
                tags:
                  - Get
                  - An
                  - Allowed
                  - Origin
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Get an allowed origin
                description: >-
                  Returns the [allowed
                  origin](https://docs.adyen.com/development-resources/client-side-authentication#allowed-origins)
                  identified in the path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants/{merchantId}/apiCredentials/{apiCredentialId}/generateApiKey:
              post:
                tags:
                  - Generate
                  - New
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Generate new API key
                description: >-
                  Returns a new API key for the API credential. You can use the
                  new API key a few minutes after generating it. The old API key
                  stops working 24 hours after generating a new one.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants/{merchantId}/apiCredentials/{apiCredentialId}/generateClientKey:
              post:
                tags:
                  - Generate
                  - New
                  - Client
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Generate new client key
                description: >-
                  Returns a new [client
                  key](https://docs.adyen.com/development-resources/client-side-authentication#how-it-works)
                  for the API credential identified in the path. You can use the
                  new client key a few minutes after generating it. The old
                  client key stops working 24 hours after generating a new one.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—API credentials read and write
            /merchants/{merchantId}/billingEntities:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Billing
                  - Entities
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                summary: Get a list of billing entities
                description: >-
                  Returns the billing entities of the merchant account
                  identified in the path.

                  A billing entity is a legal entity where we charge orders to.
                  An order for terminal products must contain the ID of a
                  billing entity.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
            /merchants/{merchantId}/paymentMethodSettings:
              get:
                tags:
                  - Get
                  - All
                  - Payments
                  - Methods
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                summary: Get all payment methods
                description: >
                  Returns details for all payment methods of the merchant
                  account identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payment methods read
              post:
                tags:
                  - Request
                  - Payments
                  - Methods
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                summary: Request a payment method
                description: >
                  Sends a request to add a new payment method to the merchant
                  account identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payment methods read and write
            /merchants/{merchantId}/paymentMethodSettings/{paymentMethodId}:
              get:
                tags:
                  - Get
                  - Payments
                  - Methods
                  - Details
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                summary: Get payment method details
                description: >
                  Returns details for the merchant account and the payment
                  method identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payment methods read
              patch:
                tags:
                  - Update
                  - Payments
                  - Methods
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                summary: Update a payment method
                description: >
                  Updates payment method details for the merchant account and
                  the payment method identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payment methods read and write
            /merchants/{merchantId}/paymentMethodSettings/{paymentMethodId}/addApplePayDomains:
              post:
                tags:
                  - Add
                  - An
                  - Apple
                  - Pay
                  - Domains
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                summary: Add an Apple Pay domain
                description: >
                  Adds the new domain to the list of Apple Pay domains that are
                  registered with the merchant account and the payment method
                  identified in the path. For more information, see [Apple Pay
                  documentation](https://docs.adyen.com/payment-methods/apple-pay/enable-apple-pay#register-merchant-domain).


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payment methods read and write
            /merchants/{merchantId}/paymentMethodSettings/{paymentMethodId}/getApplePayDomains:
              get:
                tags:
                  - Get
                  - Apple
                  - Pay
                  - Domains
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                summary: Get Apple Pay domains
                description: >
                  Returns all Apple Pay domains that are registered with the
                  merchant account and the payment method identified in the
                  path. For more information, see [Apple Pay
                  documentation](https://docs.adyen.com/payment-methods/apple-pay/enable-apple-pay#register-merchant-domain).


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payment methods read
            /merchants/{merchantId}/payoutSettings:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Payouts
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Get a list of payout settings
                description: >-
                  Returns the list of payout settings for the merchant account
                  identified in the path.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payout account settings read
              post:
                tags:
                  - Add
                  - Payouts
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Add a payout setting
                description: >-
                  Sends a request to add a payout setting for the merchant
                  account specified in the path. A payout setting links the
                  merchant account to the [transfer
                  instrument](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/transferInstruments)
                  that contains the details of the payout bank account. Adyen
                  verifies the bank account before allowing and enabling the
                  payout setting.


                  If you're accepting payments in multiple currencies, you may
                  add multiple payout settings for the merchant account.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):


                  * Management API—Payout account settings read and write
            /merchants/{merchantId}/payoutSettings/{payoutSettingsId}:
              delete:
                tags:
                  - Delete
                  - Payouts
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Delete a payout setting
                description: >-
                  Deletes the payout setting identified in the path.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):


                  * Management API—Payout account settings read and write
              get:
                tags:
                  - Get
                  - Payouts
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Get a payout setting
                description: >-
                  Returns the payout setting identified in the path.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Payout account settings read
              patch:
                tags:
                  - Update
                  - Payouts
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Update a payout setting
                description: >-
                  Updates the payout setting identified in the path. You can
                  enable or disable the payout setting.


                  Use this endpoint if your integration requires it, such as
                  Adyen for Platforms Manage. Your Adyen contact will set up
                  your access.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):


                  * Management API—Payout account settings read and write
            /merchants/{merchantId}/shippingLocations:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Shipping
                  - Locations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Get a list of shipping locations
                description: >-
                  Returns the shipping locations for the merchant account
                  identified in the path.

                  A shipping location includes the address where orders can be
                  delivered, and an ID which you need to specify when ordering
                  terminal products.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
              post:
                tags:
                  - Create
                  - Shipping
                  - Locations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                summary: Create a shipping location
                description: >-
                  Creates a shipping location for the merchant account
                  identified in the path. A shipping location defines an address
                  where orders can be shipped to. 


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write
            /merchants/{merchantId}/splitConfigurations:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Split
                  - Configurations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                summary: Get a list of split configurations
                description: >-
                  Returns the list of split configurations for the merchant
                  account.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
              post:
                tags:
                  - Create
                  - Split
                  - Configurations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                summary: Create a split configuration
                description: >-
                  Creates a split configuration for the merchant account
                  specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
            /merchants/{merchantId}/splitConfigurations/{splitConfigurationId}:
              delete:
                tags:
                  - Delete
                  - Split
                  - Configurations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                summary: Delete a split configuration
                description: >-
                  Deletes the split configuration specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
              get:
                tags:
                  - Get
                  - Split
                  - Configurations
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                summary: Get a split configuration
                description: >-
                  Returns the split configuration specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
              patch:
                tags:
                  - Update
                  - Split
                  - Configurations
                  - Descriptions
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                summary: Update split configuration description
                description: >-
                  Changes the description of the split configuration specified
                  in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
              post:
                tags:
                  - Create
                  - Rules
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                summary: Create a rule
                description: >-
                  Creates a rule in the split configuration specified in the
                  path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
            /merchants/{merchantId}/splitConfigurations/{splitConfigurationId}/rules/{ruleId}:
              delete:
                tags:
                  - Delete
                  - Split
                  - Configurations
                  - Rules
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                summary: Delete a split configuration rule
                description: >-
                  Deletes the split configuration rule specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
              patch:
                tags:
                  - Update
                  - Split
                  - Conditions
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                summary: Update split conditions
                description: >-
                  Changes the conditions of the split configuration rule
                  specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
            /merchants/{merchantId}/splitConfigurations/{splitConfigurationId}/rules/{ruleId}/splitLogic/{splitLogicId}:
              patch:
                tags:
                  - Update
                  - The
                  - Split
                  - Logic
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                summary: Update the split logic
                description: >-
                  Changes the split logic specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API - SplitConfiguration read and write
            /merchants/{merchantId}/stores:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Stores
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                summary: Get a list of stores
                description: >-
                  Returns a list of stores for the merchant account identified
                  in the path. The list is grouped into pages as defined by the
                  query parameters.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read

                  * Management API—Stores read and write
              post:
                tags:
                  - Create
                  - Store
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                summary: Create a store
                description: >-
                  Creates a store for the merchant account identified in the
                  path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read and write
            /merchants/{merchantId}/stores/{reference}/terminalLogos:
              get:
                tags:
                  - Get
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                summary: Get the terminal logo
                description: >-
                  Returns the logo that is configured for a specific payment
                  terminal model at the store identified in the path. 

                  The logo is returned as a Base64-encoded string. You need to
                  Base64-decode the string to get the actual image file. 

                  This logo applies to all terminals of the specified model
                  under the store, unless a different logo is configured for an
                  individual terminal.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write
              patch:
                tags:
                  - Update
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                summary: Update the terminal logo
                description: >-
                  Updates the logo that is configured for a specific payment
                  terminal model at the store identified in the path. You can
                  update the logo for only one terminal model at a time.

                  This logo applies to all terminals of the specified model
                  under the store, unless a different logo is configured for an
                  individual terminal. 


                  * To change the logo, specify the image file as a
                  Base64-encoded string.

                  * To restore the logo inherited from a higher level (merchant
                  or company account), specify an empty logo value.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write
            /merchants/{merchantId}/stores/{reference}/terminalSettings:
              get:
                tags:
                  - Get
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                summary: Get terminal settings
                description: >-
                  Returns the payment terminal settings that are configured for
                  the store identified in the path. These settings apply to all
                  terminals under the store unless different values are
                  configured for an individual terminal.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
              patch:
                tags:
                  - Update
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                summary: Update terminal settings
                description: >-
                  Updates payment terminal settings for the store identified in
                  the path. These settings apply to all terminals under the
                  store, unless different values are configured for an
                  individual terminal.


                  * To change a parameter value, include the full object that
                  contains the parameter, even if you don't want to change all
                  parameters in the object.

                  * To restore a parameter value inherited from a higher level,
                  include the full object that contains the parameter, and
                  specify an empty value for the parameter or omit the
                  parameter.

                  * Objects that are not included in the request are not
                  updated.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
            /merchants/{merchantId}/stores/{storeId}:
              get:
                tags:
                  - Get
                  - Store
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a store
                description: >-
                  Returns the details of the store identified in the path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read

                  * Management API—Stores read and write
              patch:
                tags:
                  - Update
                  - Store
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update a store
                description: >-
                  Updates the store identified in the path. You can only update
                  some store parameters.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read and write
            /merchants/{merchantId}/terminalLogos:
              get:
                tags:
                  - Get
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get the terminal logo
                description: >-
                  Returns the logo that is configured for a specific payment
                  terminal model at the merchant account identified in the
                  path. 

                  The logo is returned as a Base64-encoded string. You need to
                  Base64-decode the string to get the actual image file. 

                  This logo applies to all terminals of the specified model
                  under the merchant account, unless a different logo is
                  configured at a lower level (store or individual terminal).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write
              patch:
                tags:
                  - Update
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update the terminal logo
                description: >-
                  Updates the logo for a specific payment terminal model at the
                  merchant account identified in the path. You can update the
                  logo for only one terminal model at a time. 

                  This logo applies to all terminals of the specified model
                  under the merchant account, unless a different logo is
                  configured at a lower level (store or individual terminal).


                  * To change the logo, specify the image file as a
                  Base64-encoded string.

                  * To restore the logo inherited from the company account,
                  specify an empty logo value.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write
            /merchants/{merchantId}/terminalModels:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Terminal
                  - Models
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a list of terminal models
                description: >-
                  Returns the payment terminal models that merchant account
                  identified in the path has access to. The response includes
                  the terminal model ID, which can be used as a query parameter
                  when getting a list of terminals or a list of products for
                  ordering.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
            /merchants/{merchantId}/terminalOrders:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a list of orders
                description: >-
                  Returns a list of terminal products orders for the merchant
                  account identified in the path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
              post:
                tags:
                  - Create
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Create an order
                description: >-
                  Creates an order for payment terminal products for the
                  merchant account identified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write

                  >Requests to the Management API test endpoint do not create
                  actual orders for test terminals. To order test terminals, you
                  need to [submit a sales
                  order](https://docs.adyen.com/point-of-sale/managing-terminals/order-terminals/#sales-order-steps)
                  in your Customer Area.
            /merchants/{merchantId}/terminalOrders/{orderId}:
              get:
                tags:
                  - Get
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get an order
                description: >-
                  Returns the details of the terminal products order identified
                  in the path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
              patch:
                tags:
                  - Update
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update an order
                description: >-
                  Updates the terminal products order identified in the path.

                  Updating is only possible while the order has the status
                  **Placed**.


                  The request body only needs to contain what you want to
                  change. 

                  However, to update the products in the `items` array, you must
                  provide the entire array. For example, if the array has three
                  items:
                   To remove one item, the array must include the remaining two items. Or to add one item, the array must include all four items.

                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write
            /merchants/{merchantId}/terminalOrders/{orderId}/cancel:
              post:
                tags:
                  - Cancel
                  - An
                  - Orders
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Cancel an order
                description: >-
                  Cancels the terminal products order identified in the path.

                  Cancelling is only possible while the order has the status
                  **Placed**.

                  To cancel an order, make a POST call without a request body.
                  The response returns the full order details, but with the
                  status changed to **Cancelled**.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read and write
            /merchants/{merchantId}/terminalProducts:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Terminal
                  - Products
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a list of terminal products
                description: >-
                  Returns a country-specific list of payment terminal packages
                  and parts that the merchant account identified in the path has
                  access to.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal ordering read

                  * Management API—Terminal ordering read and write
            /merchants/{merchantId}/terminalSettings:
              get:
                tags:
                  - Get
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get terminal settings
                description: >-
                  Returns the payment terminal settings that are configured for
                  the merchant account identified in the path. These settings
                  apply to all terminals under the merchant account unless
                  different values are configured at a lower level (store or
                  individual terminal).


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write
              patch:
                tags:
                  - Update
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update terminal settings
                description: >-
                  Updates payment terminal settings for the merchant account
                  identified in the path.

                  These settings apply to all terminals under the merchant
                  account, unless different values are configured at a lower
                  level (store or individual terminal).


                  * To change a parameter value, include the full object that
                  contains the parameter, even if you don't want to change all
                  parameters in the object.

                  * To restore a parameter value inherited from a higher level,
                  include the full object that contains the parameter, and
                  specify an empty value for the parameter or omit the
                  parameter.

                  * Objects that are not included in the request are not
                  updated.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write
            /merchants/{merchantId}/users:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Users
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a list of users
                description: >
                  Returns a list of users associated with the `merchantId`
                  specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
              post:
                tags:
                  - Create
                  - New
                  - Users
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Create a new user
                description: >
                  Creates a user for the `merchantId` specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
            /merchants/{merchantId}/users/{userId}:
              get:
                tags:
                  - Get
                  - Users
                  - Details
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get user details
                description: >
                  Returns user details for the `userId` and the `merchantId`
                  specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
              patch:
                tags:
                  - Update
                  - Users
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update a user
                description: >
                  Updates user details for the `userId` and the `merchantId`
                  specified in the path.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Users read and write
            /merchants/{merchantId}/webhooks:
              get:
                tags:
                  - Lists
                  - All
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: List all webhooks
                description: >-
                  Lists all webhook configurations for the merchant account.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read

                  * Management API—Webhooks read and write
              post:
                tags:
                  - Sets
                  - Up
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Set up a webhook
                description: >-
                  Subscribe to receive webhook notifications about events
                  related to your merchant account. You can add basic
                  authentication to make sure the data is secure.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /merchants/{merchantId}/webhooks/{webhookId}:
              delete:
                tags:
                  - Removes
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Remove a webhook
                description: >-
                  Remove the configuration for the webhook identified in the
                  path.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
              get:
                tags:
                  - Get
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a webhook
                description: >-
                  Returns the configuration for the webhook identified in the
                  path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read

                  * Management API—Webhooks read and write
              patch:
                tags:
                  - Update
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update a webhook
                description: >-
                  Make changes to the configuration of the webhook identified in
                  the path. The request contains the new values you want to have
                  in the webhook configuration. The response contains the full
                  configuration for the webhook, which includes the new values
                  from the request.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /merchants/{merchantId}/webhooks/{webhookId}/generateHmac:
              post:
                tags:
                  - Generate
                  - An
                  - Keys
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Generate an HMAC key
                description: >-
                  Returns an [HMAC key](https://en.wikipedia.org/wiki/HMAC) for
                  the webhook identified in the path. This key allows you to
                  check the integrity and the origin of the notifications you
                  receive.By creating an HMAC key, you start receiving
                  [HMAC-signed
                  notifications](https://docs.adyen.com/development-resources/webhooks/verify-hmac-signatures#enable-hmac-signatures)
                  from Adyen. Find out more about how to [verify HMAC
                  signatures](https://docs.adyen.com/development-resources/webhooks/verify-hmac-signatures).


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /merchants/{merchantId}/webhooks/{webhookId}/test:
              post:
                tags:
                  - Tests
                  - Webhooks
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Test a webhook
                description: >-
                  Sends sample notifications to test if the webhook is set up
                  correctly.


                  We send four test notifications for each event code you
                  choose. They cover success and failure scenarios for the
                  hard-coded currencies EUR and GBP, regardless of the
                  currencies configured in the merchant accounts. For custom
                  notifications, we only send the specified custom notification.


                  The response describes the result of the test. The `status`
                  field tells you if the test was successful or not. You can use
                  the other fields to troubleshoot unsuccessful tests.


                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Webhooks read and write
            /stores:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Stores
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a list of stores
                description: >-
                  Returns a list of stores. The list is grouped into pages as
                  defined by the query parameters.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read

                  * Management API—Stores read and write
              post:
                tags:
                  - Create
                  - Store
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Create a store
                description: >-
                  Creates a store for the merchant account specified in the
                  request.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read and write
            /stores/{storeId}:
              get:
                tags:
                  - Get
                  - Store
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get a store
                description: >-
                  Returns the details of the store identified in the path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read

                  * Management API—Stores read and write
              patch:
                tags:
                  - Update
                  - Store
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update a store
                description: >-
                  Updates the store identified in the path.

                  You can only update some store parameters.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Stores read and write
            /stores/{storeId}/terminalLogos:
              get:
                tags:
                  - Get
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get the terminal logo
                description: >-
                  Returns the logo that is configured for a specific payment
                  terminal model at the store identified in the path. 

                  The logo is returned as a Base64-encoded string. You need to
                  Base64-decode the string to get the actual image file. 

                  This logo applies to all terminals of that model under the
                  store unless a different logo is configured for an individual
                  terminal.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write
              patch:
                tags:
                  - Update
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update the terminal logo
                description: >-
                  Updates the logo that is configured for a specific payment
                  terminal model at the store identified in the path. You can
                  update the logo for only one terminal model at a time.

                  This logo applies to all terminals of the specified model
                  under the store, unless a different logo is configured for an
                  individual terminal. 


                  * To change the logo, specify the image file as a
                  Base64-encoded string.

                  * To restore the logo inherited from a higher level (merchant
                  or company account), specify an empty logo value.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write
            /stores/{storeId}/terminalSettings:
              get:
                tags:
                  - Get
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Get terminal settings
                description: >-
                  Returns the payment terminal settings that are configured for
                  the store identified in the path. These settings apply to all
                  terminals under the store unless different values are
                  configured for an individual terminal.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
              patch:
                tags:
                  - Update
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                summary: Update terminal settings
                description: >-
                  Updates payment terminal settings for the store identified in
                  the path. These settings apply to all terminals under the
                  store, unless different values are configured for an
                  individual terminal.


                  * To change a parameter value, include the full object that
                  contains the parameter, even if you don't want to change all
                  parameters in the object.

                  * To restore a parameter value inherited from a higher level,
                  include the full object that contains the parameter, and
                  specify an empty value for the parameter or omit the
                  parameter.

                  * Objects that are not included in the request are not
                  updated.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
            /terminals:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Terminals
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                summary: Get a list of terminals
                description: >-
                  Returns the payment terminals that the API credential has
                  access to and that match the query parameters. 

                  To make this request, your API credential must have the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API — Terminal actions read
            /terminals/scheduleActions:
              post:
                tags:
                  - Create
                  - Terminal
                  - Actions
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                summary: Create a terminal action
                description: >-
                  Schedules a [terminal
                  action](https://docs.adyen.com/point-of-sale/automating-terminal-management/terminal-actions-api)
                  by specifying the action and the terminals that the action
                  must be applied to. 


                  The following restrictions apply:

                  * You can schedule only one action at a time. For example, to
                  install a new app version and remove an old app version, you
                  have to make two API requests. 

                  * The maximum number of terminals in a request is **100**. For
                  example, to apply an action to 250 terminals, you have to
                  divide the terminals over three API requests. 

                  * If there is an error with one or more terminal IDs in the
                  request, the action is scheduled for none of the terminals.
                  You need to fix the error and try again. 


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal actions read and write
            /terminals/{terminalId}/reassign:
              post:
                tags:
                  - Reassign
                  - Terminal
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                  - Reassign
                summary: Reassign a terminal
                description: >-
                  Reassigns a payment terminal to a company account, merchant
                  account, merchant account inventory, or a store.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Assign Terminal
            /terminals/{terminalId}/terminalLogos:
              get:
                tags:
                  - Get
                  - The
                  - Terminal
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                  - Reassign
                summary: Get the terminal logo
                description: >-
                  Returns the logo that is configured for the payment terminal
                  identified in the path.

                  The logo is returned as a Base64-encoded string. You need to
                  Base64-decode the string to get the actual image file.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write
              patch:
                tags:
                  - Update
                  - The
                  - Logo
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                  - Reassign
                summary: Update the logo
                description: >-
                  Updates the logo for the payment terminal identified in the
                  path.


                  * To change the logo, specify the image file as a
                  Base64-encoded string.

                  * To restore the logo inherited from a higher level (store,
                  merchant account, or company account), specify an empty logo
                  value.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write
            /terminals/{terminalId}/terminalSettings:
              get:
                tags:
                  - Get
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                  - Reassign
                summary: Get terminal settings
                description: >-
                  Returns the settings that are configured for the payment
                  terminal identified in the path.


                  To make this request, your API credential must have one of the
                  following
                  [roles](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Terminal settings Advanced read and write
              patch:
                tags:
                  - Update
                  - Terminal
                  - Settings
                  - Companies
                  - Identifiers
                  - Android
                  - Applications
                  - Certificates
                  - APIs
                  - Credentials
                  - Credentials
                  - Allowed
                  - Origins
                  - Origin
                  - Generate
                  - Keys
                  - Client
                  - Billing
                  - Entities
                  - Merchants
                  - Shipping
                  - Locations
                  - Terminal
                  - Actions
                  - Actions
                  - Logos
                  - Models
                  - Orders
                  - Orders
                  - Cancel
                  - Products
                  - Settings
                  - Users
                  - Users
                  - Webhooks
                  - Webhooks
                  - HMAC
                  - Tests
                  - Me
                  - Activate
                  - Payments
                  - Methods
                  - Add
                  - Apple
                  - Pay
                  - Domains
                  - Get
                  - Payouts
                  - Split
                  - Configurations
                  - Configurations
                  - Rules
                  - Rules
                  - Logic
                  - Stores
                  - References
                  - Store
                  - Terminals
                  - Reassign
                summary: Update terminal settings
                description: >-
                  Updates the settings that are configured for the payment
                  terminal identified in the path.


                  * To change a parameter value, include the full object that
                  contains the parameter, even if you don't want to change all
                  parameters in the object.

                  * To restore a parameter value inherited from a higher level,
                  include the full object that contains the parameter, and
                  specify an empty value for the parameter or omit the
                  parameter.

                  * Objects that are not included in the request are not
                  updated.


                  To make this request, your API credential must have the
                  following
                  [role](https://docs.adyen.com/development-resources/api-credentials#api-permissions):

                  * Management API—Terminal settings read and write


                  For [sensitive terminal
                  settings](https://docs.adyen.com/point-of-sale/automating-terminal-management/configure-terminals-api#sensitive-terminal-settings),
                  your API credential must have the following role:

                  * Management API—Termina
    overlays:
      - type: APIs.io Search
        url: overlays/management-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/management-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-management-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---