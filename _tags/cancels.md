---
name: Cancels
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cancels.png
url: https://example.com/apis/cancels.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cancels
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
  - name: FactSet Vermilion API
    description: >-
      The Vermilion API, enables users to programmatically access FactSet's
      Vermilion Reporting Suite (VRS) and seamlessly integrate into customer's
      3rd party applications. The API is referred to as two key product
      initiatives, the REST API and the SCIM API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/vermilion-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/vermilion-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/vermilion-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/vermilion-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/vermilion-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/vermilion-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: VRS API documentation
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/vermilion-api
          tags:
            - name: Datasource
            - name: Entities
            - name: Reports
            - name: Report instance
            - name: SCIM
          paths:
            /v1/{tenant}/data-sources:
              get:
                tags:
                  - Lists
                  - All
                  - Datasources
                  - V1
                  - Tenant
                  - Data
                  - Sources
                summary: Lists all datasources
                description: List all datasources the user has permission to see
            /v1/{tenant}/data-sources/{dataSourceCode}:
              get:
                tags:
                  - Gets
                  - Datasource
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                summary: Gets a datasource
                description: Gets a datasource based on the code passed
            /v1/{tenant}/data-sources/{dataSourceCode}/data:
              get:
                tags:
                  - Gets
                  - The
                  - Data
                  - For
                  - Datasource
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                summary: Gets the data for the datasource
                description: >-
                  Gets the data for the datasource. There are optional query
                  parameters to filter the data
            /v1/{tenant}/entities/{entityCode}/values:
              get:
                tags:
                  - Gets
                  - The
                  - Entity
                  - Values
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                summary: Gets the entity values
                description: Gets the entity values for the specified entity
            /v1/{tenant}/reports:
              get:
                tags:
                  - Gets
                  - All
                  - Report
                  - Definitions
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                summary: Gets all report definitions
                description: Gets all report definitions the user has permissions for
            /v1/{tenant}/reports/{reportDefinitionCode}:
              get:
                tags:
                  - Gets
                  - Report
                  - Definition
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                summary: Gets a report definition
                description: Gets a report defintion based on the code specified
            /v1/report-instances/generate:
              post:
                tags:
                  - Generates
                  - Report
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                summary: Generates a report
                description: >-
                  Generates a report using the specified ID and the JSON in the
                  request body
            /v1/{tenant}/report-instances/{reportInstanceId}:
              delete:
                tags:
                  - Cancels
                  - Report
                  - Generation
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Cancels a report generation
                description: >-
                  Sends a request to cancel a report generation based on the
                  report instance id passed
              get:
                tags:
                  - Gets
                  - Report
                  - Instance
                  - Based
                  - 'On'
                  - The
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Gets a report instance based on the ID
                description: Gets a report instance object based on the ID passed
            /v1/{tenant}/report-instances:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Report
                  - Instances
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                summary: Gets a list of report instances
                description: >-
                  Gets a list of report instances. This can be filtered down
                  further by including query parameters in the URL. For example,
                  a report definition id can be added so the only report
                  instances returned are the ones with a matching id
            /v1/{tenant}/report-instances/{reportInstanceId}/results/{reportFileName}:
              get:
                tags:
                  - Gets
                  - The
                  - Generated
                  - File
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                summary: Gets the generated file
                description: >-
                  Get the generated file for a report instance. Users can fetch
                  the generated report once the genration is finished. The
                  report instance id and the report file name are passed in as
                  path paramters
            /v1/{tenant}/report-instances/{reportInstanceId}/logs:
              get:
                tags:
                  - Gets
                  - List
                  - Of
                  - Logs
                  - For
                  - The
                  - Report
                  - Instance
                  - Generation
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                summary: Gets a list of logs for the report instance generation
                description: >-
                  Gets a list of logs for the generated report instance. Allows
                  the user to sort on log message, type and date. Also allows
                  for retrieving of just the errors & warnings'
            /scim/v2/Users:
              get:
                tags:
                  - Retrieves
                  - List
                  - Of
                  - Users
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                summary: Retrieves a list of VRS users
                description: Retrieves a list of VRS users
              post:
                tags:
                  - Creates
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                summary: Creates a user
                description: Creates a VRS user
            /scim/v2/Users/{userId}:
              get:
                tags:
                  - Retrieves
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Retrieves a VRS User
                description: Retrieves a VRS user based on their ID
              delete:
                tags:
                  - Deletes
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Deletes a VRS user
                description: >-
                  Deletes a VRS user (this marks them as 'Deleted' in the
                  database)
              patch:
                tags:
                  - Add
                  - Or
                  - Remove
                  - User
                  - Attributes
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Add or remove VRS user attributes
                description: >-
                  Adds or removes VRS user attributes based on the JSON
                  properties
              put:
                tags:
                  - Updates
                  - User
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                summary: Updates a VRS user
                description: Updates (replaces) a VRS user with the properties in the JSON
            /scim/v2/Groups:
              get:
                tags:
                  - Retrieves
                  - List
                  - Of
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                summary: Retrieves a list of VRS role
                description: Retrieves a VRS roles
              post:
                tags:
                  - Creates
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                summary: Creates a role
                description: Creates a VRS role
            /scim/v2/Groups/{groupId}:
              get:
                tags:
                  - Retrieves
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Retrieves a VRS role
                description: Retrieves a VRS role based on the ID
              delete:
                tags:
                  - Deletes
                  - Role
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Deletes a VRS role
                description: Deletes a VRS role
              patch:
                tags:
                  - Add
                  - Or
                  - Remove
                  - User
                  - To/from
                  - Group
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Add or remove a user to/from a group
                description: Adds or removes a VRS user to/from a VRS role
              put:
                tags:
                  - Updates
                  - Group
                  - V1
                  - Tenant
                  - Data
                  - Sources
                  - Source
                  - Code
                  - Values
                  - Reports
                  - Definition
                  - Report
                  - Instances
                  - Generate
                  - Instance
                  - Id
                  - Results
                  - File
                  - Name
                  - Logs
                  - Users
                  - User
                  - Groups
                  - Group
                summary: Updates a VRS Group
                description: Updates (replaces) a VRS Group with the pr
    overlays:
      - type: APIs.io Search
        url: overlays/vermilion-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/vermilion-openapi-api-evangelist-ratings.yml
    aid: factset:factset-vermilion-api
  - name: OpenAI Threads API
    description: Create threads that assistants can interact with.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://platform.openai.com/docs/api-reference/threads
    baseURL: https://platform.openai.com/
    tags: []
    properties:
      - type: Documentation
        url: https://platform.openai.com/docs/api-reference
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: ' threads'
            license:
              name: MIT
              url: https://github.com/openai/openai-openapi/blob/master/LICENSE
          tags:
            - name: Assistants
              description: Build Assistants that can call models and use tools.
            - name: Audio
              description: Learn how to turn audio into text or text into audio.
            - name: Chat
              description: >-
                Given a list of messages comprising a conversation, the model
                will return a response.
            - name: Completions
              description: >-
                Given a prompt, the model will return one or more predicted
                completions, and can also return the probabilities of
                alternative tokens at each position.
            - name: Embeddings
              description: >-
                Get a vector representation of a given input that can be easily
                consumed by machine learning models and algorithms.
            - name: Fine-tuning
              description: >-
                Manage fine-tuning jobs to tailor a model to your specific
                training data.
            - name: Files
              description: >-
                Files are used to upload documents that can be used with
                features like Assistants and Fine-tuning.
            - name: Images
              description: >-
                Given a prompt and/or an input image, the model will generate a
                new image.
            - name: Models
              description: List and describe the various models available in the API.
            - name: Moderations
              description: >-
                Given a input text, outputs if the model classifies it as
                violating OpenAI's content policy.
          paths:
            /threads:
              post:
                tags:
                  - Create
                  - Thread.
                  - Threads
                summary: Create a thread.
            /threads/{thread_id}:
              get:
                tags:
                  - Retrieves
                  - Thread.
                  - Threads
                  - Thread_id
                summary: Retrieves a thread.
              post:
                tags:
                  - Modifies
                  - Thread.
                  - Threads
                  - Thread_id
                summary: Modifies a thread.
              delete:
                tags:
                  - Delete
                  - Thread.
                  - Threads
                  - Thread_id
                summary: Delete a thread.
            /threads/{thread_id}/messages:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Messages
                  - For
                  - Given
                  - Thread.
                  - Threads
                  - Thread_id
                  - Messages
                summary: Returns a list of messages for a given thread.
              post:
                tags:
                  - Create
                  - Message.
                  - Threads
                  - Thread_id
                  - Messages
                summary: Create a message.
            /threads/{thread_id}/messages/{message_id}:
              get:
                tags:
                  - Retrieve
                  - Message.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                summary: Retrieve a message.
              post:
                tags:
                  - Modifies
                  - Message.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                summary: Modifies a message.
            /threads/runs:
              post:
                tags:
                  - Create
                  - Thread
                  - And
                  - Run
                  - It
                  - In
                  - One
                  - Request.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                summary: Create a thread and run it in one request.
            /threads/{thread_id}/runs:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Runs
                  - Belonging
                  - To
                  - Thread.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                summary: Returns a list of runs belonging to a thread.
              post:
                tags:
                  - Create
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                summary: Create a run.
            /threads/{thread_id}/runs/{run_id}:
              get:
                tags:
                  - Retrieves
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                summary: Retrieves a run.
              post:
                tags:
                  - Modifies
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                summary: Modifies a run.
            /threads/{thread_id}/runs/{run_id}/submit_tool_outputs:
              post:
                tags:
                  - When
                  - Run
                  - Has
                  - The
                  - '`status:'
                  - '"requires_action"`'
                  - And
                  - '`required_action.type`'
                  - Is
                  - '`submit_tool_outputs`,'
                  - This
                  - Endpoint
                  - Can
                  - Be
                  - Used
                  - To
                  - Submit
                  - Outputs
                  - From
                  - Tool
                  - Calls
                  - Once
                  - They're
                  - All
                  - Completed.
                  - Must
                  - Submitted
                  - In
                  - Single
                  - |
                    Request.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                summary: >
                  When a run has the `status: "requires_action"` and
                  `required_action.type` is `submit_tool_outputs`, this endpoint
                  can be used to submit the outputs from the tool calls once
                  they're all completed. All outputs must be submitted in a
                  single request.
            /threads/{thread_id}/runs/{run_id}/cancel:
              post:
                tags:
                  - Cancels
                  - Run
                  - That
                  - Is
                  - '`in_progress`.'
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                summary: Cancels a run that is `in_progress`.
            /threads/{thread_id}/runs/{run_id}/steps:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Run
                  - Steps
                  - Belonging
                  - To
                  - Run.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                summary: Returns a list of run steps belonging to a run.
            /threads/{thread_id}/runs/{run_id}/steps/{step_id}:
              get:
                tags:
                  - Retrieves
                  - Run
                  - Step.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                  - Step_id
                summary: Retrieves a run step.
            /threads/{thread_id}/messages/{message_id}/files:
              get:
                tags:
                  - Returns
                  - List
                  - Of
                  - Message
                  - Files.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                  - Step_id
                  - Files
                summary: Returns a list of message files.
            /threads/{thread_id}/messages/{message_id}/files/{file_id}:
              get:
                tags:
                  - Retrieves
                  - Message
                  - File.
                  - Threads
                  - Thread_id
                  - Messages
                  - Message_id
                  - Runs
                  - Run_id
                  - Submit_tool_outputs
                  - Cancel
                  - Steps
                  - Step_id
                  - Files
                  - File_id
                summary: Retrieves a message file.
          x-oaiMeta:
            groups:
              - id: audio
                title: Audio
                description: |
                  Learn how to turn audio into text or text into audio.

                  Related guide: [Speech to text](/docs/guides/speech-to-text)
                sections:
                  - type: endpoint
                    key: createSpeech
                    path: createSpeech
                  - type: endpoint
                    key: createTranscription
                    path: createTranscription
                  - type: endpoint
                    key: createTranslation
                    path: createTranslation
              - id: chat
                title: Chat
                description: >
                  Given a list of messages comprising a conversation, the model
                  will return a response.


                  Related guide: [Chat
                  Completions](/docs/guides/text-generation)
                sections:
                  - type: endpoint
                    key: createChatCompletion
                    path: create
                  - type: object
                    key: CreateChatCompletionResponse
                    path: object
                  - type: object
                    key: CreateChatCompletionStreamResponse
                    path: streaming
              - id: embeddings
                title: Embeddings
                description: >
                  Get a vector representation of a given input that can be
                  easily consumed by machine learning models and algorithms.


                  Related guide: [Embeddings](/docs/guides/embeddings)
                sections:
                  - type: endpoint
                    key: createEmbedding
                    path: create
                  - type: object
                    key: Embedding
                    path: object
              - id: fine-tuning
                title: Fine-tuning
                description: >
                  Manage fine-tuning jobs to tailor a model to your specific
                  training data.


                  Related guide: [Fine-tune models](/docs/guides/fine-tuning)
                sections:
                  - type: endpoint
                    key: createFineTuningJob
                    path: create
                  - type: endpoint
                    key: listPaginatedFineTuningJobs
                    path: list
                  - type: endpoint
                    key: listFineTuningEvents
                    path: list-events
                  - type: endpoint
                    key: retrieveFineTuningJob
                    path: retrieve
                  - type: endpoint
                    key: cancelFineTuningJob
                    path: cancel
                  - type: object
                    key: FineTuningJob
                    path: object
                  - type: object
                    key: FineTuningJobEvent
                    path: event-object
              - id: files
                title: Files
                description: >
                  Files are used to upload documents that can be used with
                  features like [Assistants](/docs/api-reference/assistants) and
                  [Fine-tuning](/docs/api-reference/fine-tuning).
                sections:
                  - type: endpoint
                    key: createFile
                    path: create
                  - type: endpoint
                    key: listFiles
                    path: list
                  - type: endpoint
                    key: retrieveFile
                    path: retrieve
                  - type: endpoint
                    key: deleteFile
                    path: delete
                  - type: endpoint
                    key: downloadFile
                    path: retrieve-contents
                  - type: object
                    key: OpenAIFile
                    path: object
              - id: images
                title: Images
                description: >
                  Given a prompt and/or an input image, the model will generate
                  a new image.


                  Related guide: [Image generation](/docs/guides/images)
                sections:
                  - type: endpoint
                    key: createImage
                    path: create
                  - type: endpoint
                    key: createImageEdit
                    path: createEdit
                  - type: endpoint
                    key: createImageVariation
                    path: createVariation
                  - type: object
                    key: Image
                    path: object
              - id: models
                title: Models
                description: >
                  List and describe the various models available in the API. You
                  can refer to the [Models](/docs/models) documentation to
                  understand what models are available and the differences
                  between them.
                sections:
                  - type: endpoint
                    key: listModels
                    path: list
                  - type: endpoint
                    key: retrieveModel
                    path: retrieve
                  - type: endpoint
                    key: deleteModel
                    path: delete
                  - type: object
                    key: Model
                    path: object
              - id: moderations
                title: Moderations
                description: >
                  Given a input text, outputs if the model classifies it as
                  violating OpenAI's content policy.


                  Related guide: [Moderations](/docs/guides/moderation)
                sections:
                  - type: endpoint
                    key: createModeration
                    path: create
                  - type: object
                    key: CreateModerationResponse
                    path: object
              - id: assistants
                title: Assistants
                beta: true
                description: >
                  Build assistants that can call models and use tools to perform
                  tasks.


                  [Get started with the Assistants API](/docs/assistants)
                sections:
                  - type: endpoint
                    key: createAssistant
                    path: createAssistant
                  - type: endpoint
                    key: createAssistantFile
                    path: createAssistantFile
                  - type: endpoint
                    key: listAssistants
                    path: listAssistants
                  - type: endpoint
                    key: listAssistantFiles
                    path: listAssistantFiles
                  - type: endpoint
                    key: getAssistant
                    path: getAssistant
                  - type: endpoint
                    key: getAssistantFile
                    path: getAssistantFile
                  - type: endpoint
                    key: modifyAssistant
                    path: modifyAssistant
                  - type: endpoint
                    key: deleteAssistant
                    path: deleteAssistant
                  - type: endpoint
                    key: deleteAssistantFile
                    path: deleteAssistantFile
                  - type: object
                    key: AssistantObject
                    path: object
                  - type: object
                    key: AssistantFileObject
                    path: file-object
              - id: threads
                title: Threads
                beta: true
                description: |
                  Create threads that assistants can interact with.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createThread
                    path: createThread
                  - type: endpoint
                    key: getThread
                    path: getThread
                  - type: endpoint
                    key: modifyThread
                    path: modifyThread
                  - type: endpoint
                    key: deleteThread
                    path: deleteThread
                  - type: object
                    key: ThreadObject
                    path: object
              - id: messages
                title: Messages
                beta: true
                description: |
                  Create messages within threads

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createMessage
                    path: createMessage
                  - type: endpoint
                    key: listMessages
                    path: listMessages
                  - type: endpoint
                    key: listMessageFiles
                    path: listMessageFiles
                  - type: endpoint
                    key: getMessage
                    path: getMessage
                  - type: endpoint
                    key: getMessageFile
                    path: getMessageFile
                  - type: endpoint
                    key: modifyMessage
                    path: modifyMessage
                  - type: object
                    key: MessageObject
                    path: object
                  - type: object
                    key: MessageFileObject
                    path: file-object
              - id: runs
                title: Runs
                beta: true
                description: |
                  Represents an execution run on a thread.

                  Related guide: [Assistants](/docs/assistants/overview)
                sections:
                  - type: endpoint
                    key: createRun
                    path: createRun
                  - type: endpoint
                    key: createThreadAndRun
                    path: createThreadAndRun
                  - type: endpoint
                    key: listRuns
                    path: listRuns
                  - type: endpoint
                    key: listRunSteps
                    path: listRunSteps
                  - type: endpoint
                    key: getRun
                    path: getRun
                  - type: endpoint
                    key: getRunStep
                    path: getRunStep
                  - type: endpoint
                    key: modifyRun
                    path: modifyRun
                  - type: endpoint
                    key: submitToolOuputsToRun
                    path: submitToolOutputs
                  - type: endpoint
                    key: cancelRun
                    path: cancelRun
                  - type: object
                    key: RunObject
                    path: object
                  - type: object
                    key: RunStepObject
                    path: step-object
              - id: completions
                title: Completions
                legacy: true
                description: >
                  Given a prompt, the model will return one or more predicted
                  completions along with the probabilities of alternative tokens
                  at each position. Most developer should use our [Chat
                  Completions
                  API](/docs/guides/text-generation/text-generation-models) to
                  leverage our best and newest models. Most models that support
                  the legacy Completions endpoint [will be shut off on January
                  4th, 2024](/docs/deprecations/2023-07-06-gpt-and-embeddings).
                sections:
                  - type: endpoint
                    key: createCompletion
                    path: create
                  - type: object
                    key: CreateCompletionResponse
                    path: null
    overlays:
      - type: APIs.io Search
        url: >-
          overlays/https://github.com/apis-json/artisanal/tree/main/apis/openai/threads-openapi-search.yml
      - type: APIs.io Search
        url: overlays/threads-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/threads-openapi-api-evangelist-ratings.yml
    aid: openai:openai-threads-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---