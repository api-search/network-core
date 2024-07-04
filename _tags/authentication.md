---
name: Authentication
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/authentication.png
url: https://example.com/apis/authentication.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Authentication
apis:
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
  - name: amplifybackend
    description: <p>AWS Amplify Admin API</p>
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
            title: amplifybackend
          paths:
            /backend/{appId}/environments/{backendEnvironmentName}/clone:
              POST:
                summary: CloneBackend
                description: <p>This operation clones an existing backend.</p>
                tags:
                  - Clone
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
            /backend:
              POST:
                summary: CreateBackend
                description: >-
                  <p>This operation creates a backend for an Amplify app.
                  Backends are automatically created at the time of app
                  creation.</p>
                tags:
                  - Create
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
            /backend/{appId}/api:
              POST:
                summary: CreateBackendAPI
                description: <p>Creates a new backend API resource.</p>
                tags:
                  - Create
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
            /backend/{appId}/auth:
              POST:
                summary: CreateBackendAuth
                description: <p>Creates a new backend authentication resource.</p>
                tags:
                  - Create
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
            /backend/{appId}/config:
              POST:
                summary: CreateBackendConfig
                description: <p>Creates a config object for a backend.</p>
                tags:
                  - Create
                  - Backends
                  - Configurations
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
            /backend/{appId}/storage:
              POST:
                summary: CreateBackendStorage
                description: <p>Creates a backend storage resource.</p>
                tags:
                  - Create
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
            /backend/{appId}/challenge:
              POST:
                summary: CreateToken
                description: >-
                  <p>Generates a one-time challenge code to authenticate a user
                  into your Amplify Admin UI.</p>
                tags:
                  - Create
                  - Tokens
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
            /backend/{appId}/environments/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackend
                description: >-
                  <p>Removes an existing environment from your Amplify
                  project.</p>
                tags:
                  - Delete
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/api/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackendAPI
                description: <p>Deletes an existing backend API resource.</p>
                tags:
                  - Delete
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/auth/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackendAuth
                description: <p>Deletes an existing backend authentication resource.</p>
                tags:
                  - Delete
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/storage/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackendStorage
                description: <p>Removes the specified backend storage resource.</p>
                tags:
                  - Delete
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/challenge/{sessionId}/remove:
              POST:
                summary: DeleteToken
                description: >-
                  <p>Deletes the challenge token based on the given appId and
                  sessionId.</p>
                tags:
                  - Delete
                  - Tokens
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
            /backend/{appId}/api/{backendEnvironmentName}/generateModels:
              POST:
                summary: GenerateBackendAPIModels
                description: >-
                  <p>Generates a model schema for an existing backend API
                  resource.</p>
                tags:
                  - Generate
                  - Backends
                  - Models
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
            /backend/{appId}/details:
              POST:
                summary: GetBackend
                description: >-
                  <p>Provides project-level details for your Amplify UI
                  project.</p>
                tags:
                  - Get
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
            /backend/{appId}/api/{backendEnvironmentName}/details:
              POST:
                summary: GetBackendAPI
                description: <p>Gets the details for a backend API.</p>
                tags:
                  - Get
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
            /backend/{appId}/api/{backendEnvironmentName}/getModels:
              POST:
                summary: GetBackendAPIModels
                description: >-
                  <p>Gets a model introspection schema for an existing backend
                  API resource.</p>
                tags:
                  - Get
                  - Backends
                  - Models
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
            /backend/{appId}/auth/{backendEnvironmentName}/details:
              POST:
                summary: GetBackendAuth
                description: <p>Gets a backend auth details.</p>
                tags:
                  - Get
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
            /backend/{appId}/job/{backendEnvironmentName}/{jobId}:
              POST:
                summary: UpdateBackendJob
                description: <p>Updates a specific job.</p>
                tags:
                  - Update
                  - Backends
                  - Jobs
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
            /backend/{appId}/storage/{backendEnvironmentName}/details:
              POST:
                summary: GetBackendStorage
                description: <p>Gets details for a backend storage resource.</p>
                tags:
                  - Get
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
            /backend/{appId}/challenge/{sessionId}:
              GET:
                summary: GetToken
                description: >-
                  <p>Gets the challenge token based on the given appId and
                  sessionId.</p>
                tags:
                  - Get
                  - Tokens
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
            /backend/{appId}/auth/{backendEnvironmentName}/import:
              POST:
                summary: ImportBackendAuth
                description: <p>Imports an existing backend authentication resource.</p>
                tags:
                  - Import
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
            /backend/{appId}/storage/{backendEnvironmentName}/import:
              POST:
                summary: ImportBackendStorage
                description: <p>Imports an existing backend storage resource.</p>
                tags:
                  - Import
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
            /backend/{appId}/job/{backendEnvironmentName}:
              POST:
                summary: ListBackendJobs
                description: <p>Lists the jobs for the backend of an Amplify app.</p>
                tags:
                  - Lists
                  - Backends
                  - Jobs
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
            /s3Buckets:
              POST:
                summary: ListS3Buckets
                description: <p>The list of S3 buckets in your account.</p>
                tags:
                  - Lists
                  - S3
                  - Buckets
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/remove:
              POST:
                summary: RemoveAllBackends
                description: >-
                  <p>Removes all backend environments from your Amplify
                  project.</p>
                tags:
                  - Removes
                  - All
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/config/remove:
              POST:
                summary: RemoveBackendConfig
                description: >-
                  <p>Removes the AWS resources required to access the Amplify
                  Admin UI.</p>
                tags:
                  - Removes
                  - Backends
                  - Configurations
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/api/{backendEnvironmentName}:
              POST:
                summary: UpdateBackendAPI
                description: <p>Updates an existing backend API resource.</p>
                tags:
                  - Update
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/auth/{backendEnvironmentName}:
              POST:
                summary: UpdateBackendAuth
                description: <p>Updates an existing backend authentication resource.</p>
                tags:
                  - Update
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/config/update:
              POST:
                summary: UpdateBackendConfig
                description: >-
                  <p>Updates the AWS resources required to access the Amplify
                  Admin UI.</p>
                tags:
                  - Update
                  - Backends
                  - Configurations
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
                  - Update
            /backend/{appId}/storage/{backendEnvironmentName}:
              POST:
                summary: UpdateBackendStorage
                description: <p>Updates an existing backend storage res
                tags:
                  - Update
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/amplifybackend-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/amplifybackend-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:amplifybackend
  - name: grafana
    description: >-
      <p>Amazon Managed Grafana is a fully managed and secure data visualization
      service that you can use to instantly query, correlate, and visualize
      operational metrics, logs, and traces from multiple sources. Amazon
      Managed Grafana makes it easy to deploy, operate, and scale Grafana, a
      widely deployed data visualization tool that is popular for its extensible
      data support.</p> <p>With Amazon Managed Grafana, you create logically
      isolated Grafana servers called <i>workspaces</i>. In a workspace, you can
      create Grafana dashboards and visualizations to analyze your metrics,
      logs, and traces without having to build, package, or deploy any hardware
      to run Grafana servers. </p>
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
            title: grafana
          paths:
            /workspaces/{workspaceId}/licenses/{licenseType}:
              DELETE:
                summary: DisassociateLicense
                description: >-
                  <p>Removes the Grafana Enterprise license from a
                  workspace.</p>
                tags:
                  - Disassociate
                  - Licenses
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
            /workspaces:
              GET:
                summary: ListWorkspaces
                description: >-
                  <p>Returns a list of Amazon Managed Grafana workspaces in the
                  account, with some information about each workspace. For more
                  complete information about one workspace, use <a
                  href="https://docs.aws.amazon.com/AAMG/latest/APIReference/API_DescribeWorkspace.html">DescribeWorkspace</a>.</p>
                tags:
                  - Lists
                  - Workspaces
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
            /workspaces/{workspaceId}/apikeys:
              POST:
                summary: CreateWorkspaceApiKey
                description: >-
                  <p>Creates a Grafana API key for the workspace. This key can
                  be used to authenticate requests sent to the workspace's HTTP
                  API. See <a
                  href="https://docs.aws.amazon.com/grafana/latest/userguide/Using-Grafana-APIs.html">https://docs.aws.amazon.com/grafana/latest/userguide/Using-Grafana-APIs.html</a>
                  for available APIs and example requests.</p>
                tags:
                  - Create
                  - Workspaces
                  - APIs
                  - Keys
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
            /workspaces/{workspaceId}:
              PUT:
                summary: UpdateWorkspace
                description: >-
                  <p>Modifies an existing Amazon Managed Grafana workspace. If
                  you use this operation and omit any optional parameters, the
                  existing values of those parameters are not changed.</p> <p>To
                  modify the user authentication methods that the workspace
                  uses, such as SAML or IAM Identity Center, use <a
                  href="https://docs.aws.amazon.com/grafana/latest/APIReference/API_UpdateWorkspaceAuthentication.html">UpdateWorkspaceAuthentication</a>.</p>
                  <p>To modify which users in the workspace have the
                  <code>Admin</code> and <code>Editor</code> Grafana roles, use
                  <a
                  href="https://docs.aws.amazon.com/grafana/latest/APIReference/API_UpdatePermissions.html">UpdatePermissions</a>.</p>
                tags:
                  - Update
                  - Workspaces
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
            /workspaces/{workspaceId}/apikeys/{keyName}:
              DELETE:
                summary: DeleteWorkspaceApiKey
                description: <p>Deletes a Grafana API key for the workspace.</p>
                tags:
                  - Delete
                  - Workspaces
                  - APIs
                  - Keys
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
                  - Keys
                  - Names
            /workspaces/{workspaceId}/authentication:
              POST:
                summary: UpdateWorkspaceAuthentication
                description: >-
                  <p>Use this operation to define the identity provider (IdP)
                  that this workspace authenticates users from, using SAML. You
                  can also map SAML assertion attributes to workspace user
                  information and define which groups in the assertion attribute
                  are to have the <code>Admin</code> and <code>Editor</code>
                  roles in the workspace.</p> <note> <p>Changes to the
                  authentication method for a workspace may take a few minutes
                  to take effect.</p> </note>
                tags:
                  - Update
                  - Workspaces
                  - Authentication
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
                  - Keys
                  - Names
                  - Authentication
            /workspaces/{workspaceId}/configuration:
              PUT:
                summary: UpdateWorkspaceConfiguration
                description: >-
                  <p>Updates the configuration string for the given
                  workspace</p>
                tags:
                  - Update
                  - Workspaces
                  - Configurations
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
                  - Keys
                  - Names
                  - Authentication
                  - Configurations
            /workspaces/{workspaceId}/permissions:
              PATCH:
                summary: UpdatePermissions
                description: >-
                  <p>Updates which users in a workspace have the Grafana
                  <code>Admin</code> or <code>Editor</code> roles.</p>
                tags:
                  - Update
                  - Permissions
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
                  - Keys
                  - Names
                  - Authentication
                  - Configurations
                  - Permissions
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>The <code>UntagResource</code> operation removes the
                  association of the tag with the Amazon Managed Grafana
                  resource. </p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
                  - Keys
                  - Names
                  - Authentication
                  - Configurations
                  - Permissions
                  - ARN
            /versions:
              GET:
                summary: ListVersions
                description: >-
                  <p>Lists available versions of Grafana. These are available
                  when calling <code>CreateWorkspace</code>. Optionally, include
                  a workspace to list the versions to which it can be upg
                tags:
                  - Lists
                  - Versions
                  - Identifiers
                  - Licenses
                  - Licenses
                  - Types
                  - Workspaces
                  - API Keys
                  - Keys
                  - Names
                  - Authentication
                  - Configurations
                  - Permissions
                  - ARN
                  - Versions
    overlays:
      - type: APIs.io Search
        url: overlays/grafana-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/grafana-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:grafana
  - name: payment-cryptography-data
    description: >-
      <p>You use the Amazon Web Services Payment Cryptography Data Plane to
      manage how encryption keys are used for payment-related transaction
      processing and associated cryptographic operations. You can encrypt,
      decrypt, generate, verify, and translate payment-related cryptographic
      operations in Amazon Web Services Payment Cryptography. For more
      information, see <a
      href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/data-operations.html">Data
      operations</a> in the <i>Amazon Web Services Payment Cryptography User
      Guide</i>.</p> <p>To manage your encryption keys, you use the <a
      href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/Welcome.html">Amazon
      Web Services Payment Cryptography Control Plane</a>. You can create,
      import, export, share, manage, and delete keys. You can also manage
      Identity and Access Management (IAM) policies for keys. </p>
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
            title: payment-cryptography-data
          paths:
            /keys/{KeyIdentifier}/decrypt:
              POST:
                summary: DecryptData
                description: >-
                  <p>Decrypts ciphertext data to plaintext using symmetric,
                  asymmetric, or DUKPT data encryption key. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/decrypt-data.html">Decrypt
                  data</a> in the <i>Amazon Web Services Payment Cryptography
                  User Guide</i>.</p> <p>You can use an encryption key generated
                  within Amazon Web Services Payment Cryptography, or you can
                  import your own encryption key by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>.
                  For this operation, the key must have
                  <code>KeyModesOfUse</code> set to <code>Decrypt</code>. In
                  asymmetric decryption, Amazon Web Services Payment
                  Cryptography decrypts the ciphertext using the private
                  component of the asymmetric encryption key pair. For data
                  encryption outside of Amazon Web Services Payment
                  Cryptography, you can export the public component of the
                  asymmetric key pair by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_GetPublicKeyCertificate.html">GetPublicCertificate</a>.</p>
                  <p>For symmetric and DUKPT decryption, Amazon Web Services
                  Payment Cryptography supports <code>TDES</code> and
                  <code>AES</code> algorithms. For asymmetric decryption, Amazon
                  Web Services Payment Cryptography supports <code>RSA</code>.
                  When you use DUKPT, for <code>TDES</code> algorithm, the
                  ciphertext data length must be a multiple of 16 bytes. For
                  <code>AES</code> algorithm, the ciphertext data length must be
                  a multiple of 32 bytes.</p> <p>For information about valid
                  keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>EncryptData</a> </p>
                  </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_GetPublicKeyCertificate.html">GetPublicCertificate</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>
                  </p> </li> </ul>
                tags:
                  - Decrypt
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
            /keys/{KeyIdentifier}/encrypt:
              POST:
                summary: EncryptData
                description: >-
                  <p>Encrypts plaintext data to ciphertext using symmetric,
                  asymmetric, or DUKPT data encryption key. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/encrypt-data.html">Encrypt
                  data</a> in the <i>Amazon Web Services Payment Cryptography
                  User Guide</i>.</p> <p>You can generate an encryption key
                  within Amazon Web Services Payment Cryptography by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_CreateKey.html">CreateKey</a>.
                  You can import your own encryption key by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>.
                  For this operation, the key must have
                  <code>KeyModesOfUse</code> set to <code>Encrypt</code>. In
                  asymmetric encryption, plaintext is encrypted using public
                  component. You can import the public component of an
                  asymmetric key pair created outside Amazon Web Services
                  Payment Cryptography by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>).
                  </p> <p>for symmetric and DUKPT encryption, Amazon Web
                  Services Payment Cryptography supports <code>TDES</code> and
                  <code>AES</code> algorithms. For asymmetric encryption, Amazon
                  Web Services Payment Cryptography supports <code>RSA</code>.
                  To encrypt using DUKPT, you must already have a DUKPT key in
                  your account with <code>KeyModesOfUse</code> set to
                  <code>DeriveKey</code>, or you can generate a new DUKPT key by
                  calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_CreateKey.html">CreateKey</a>.</p>
                  <p>For information about valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>.</p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>DecryptData</a> </p>
                  </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_GetPublicKeyCertificate.html">GetPublicCertificate</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>
                  </p> </li> <li> <p> <a>ReEncryptData</a> </p> </li> </ul>
                tags:
                  - Encrypt
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
            /cardvalidationdata/generate:
              POST:
                summary: GenerateCardValidationData
                description: >-
                  <p>Generates card-related validation data using algorithms
                  such as Card Verification Values (CVV/CVV2), Dynamic Card
                  Verification Values (dCVV/dCVV2), or Card Security Codes
                  (CSC). For more information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/generate-card-data.html">Generate
                  card data</a> in the <i>Amazon Web Services Payment
                  Cryptography User Guide</i>.</p> <p>This operation generates a
                  CVV or CSC value that is printed on a payment credit or debit
                  card during card production. The CVV or CSC, PAN (Primary
                  Account Number) and expiration date of the card are required
                  to check its validity during transaction processing. To begin
                  this operation, a CVK (Card Verification Key) encryption key
                  is required. You can use <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_CreateKey.html">CreateKey</a>
                  or <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>
                  to establish a CVK within Amazon Web Services Payment
                  Cryptography. The <code>KeyModesOfUse</code> should be set to
                  <code>Generate</code> and <code>Verify</code> for a CVK
                  encryption key. </p> <p>For information about valid keys for
                  this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>
                  </p> </li> <li> <p> <a>VerifyCardValidationData</a> </p> </li>
                  </ul>
                tags:
                  - Generate
                  - Cards
                  - Validations
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
            /mac/generate:
              POST:
                summary: GenerateMac
                description: >-
                  <p>Generates a Message Authentication Code (MAC) cryptogram
                  within Amazon Web Services Payment Cryptography. </p> <p>You
                  can use this operation when keys won't be shared but mutual
                  data is present on both ends for validation. In this case,
                  known data values are used to generate a MAC on both ends for
                  comparision without sending or receiving data in ciphertext or
                  plaintext. You can use this operation to generate a DUPKT,
                  HMAC or EMV MAC by setting generation attributes and algorithm
                  to the associated values. The MAC generation encryption key
                  must have valid values for <code>KeyUsage</code> such as
                  <code>TR31_M7_HMAC_KEY</code> for HMAC generation, and they
                  key must have <code>KeyModesOfUse</code> set to
                  <code>Generate</code> and <code>Verify</code>.</p> <p>For
                  information about valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>VerifyMac</a> </p> </li>
                  </ul>
                tags:
                  - Generate
                  - Mac
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
            /pindata/generate:
              POST:
                summary: GeneratePinData
                description: >-
                  <p>Generates pin-related data such as PIN, PIN Verification
                  Value (PVV), PIN Block, and PIN Offset during new card
                  issuance or reissuance. For more information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/generate-pin-data.html">Generate
                  PIN data</a> in the <i>Amazon Web Services Payment
                  Cryptography User Guide</i>.</p> <p>PIN data is never
                  transmitted in clear to or from Amazon Web Services Payment
                  Cryptography. This operation generates PIN, PVV, or PIN Offset
                  and then encrypts it using Pin Encryption Key (PEK) to create
                  an <code>EncryptedPinBlock</code> for transmission from Amazon
                  Web Services Payment Cryptography. This operation uses a
                  separate Pin Verification Key (PVK) for VISA PVV generation.
                  </p> <p>For information about valid keys for this operation,
                  see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>.</p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p>
                  <a>GenerateCardValidationData</a> </p> </li> <li> <p>
                  <a>TranslatePinData</a> </p> </li> <li> <p>
                  <a>VerifyPinData</a> </p> </li> </ul>
                tags:
                  - Generate
                  - Pin
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
            /keys/{IncomingKeyIdentifier}/reencrypt:
              POST:
                summary: ReEncryptData
                description: >-
                  <p>Re-encrypt ciphertext using DUKPT, Symmetric and Asymmetric
                  Data Encryption Keys. </p> <p>You can either generate an
                  encryption key within Amazon Web Services Payment Cryptography
                  by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_CreateKey.html">CreateKey</a>
                  or import your own encryption key by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>.
                  The <code>KeyArn</code> for use with this operation must be in
                  a compatible key state with <code>KeyModesOfUse</code> set to
                  <code>Encrypt</code>. In asymmetric encryption, ciphertext is
                  encrypted using public component (imported by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>)
                  of the asymmetric key pair created outside of Amazon Web
                  Services Payment Cryptography. </p> <p>For symmetric and DUKPT
                  encryption, Amazon Web Services Payment Cryptography supports
                  <code>TDES</code> and <code>AES</code> algorithms. For
                  asymmetric encryption, Amazon Web Services Payment
                  Cryptography supports <code>RSA</code>. To encrypt using
                  DUKPT, a DUKPT key must already exist within your account with
                  <code>KeyModesOfUse</code> set to <code>DeriveKey</code> or a
                  new DUKPT can be generated by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_CreateKey.html">CreateKey</a>.</p>
                  <p>For information about valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>DecryptData</a> </p>
                  </li> <li> <p> <a>EncryptData</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_GetPublicKeyCertificate.html">GetPublicCertificate</a>
                  </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>
                  </p> </li> </ul>
                tags:
                  - Re
                  - Encrypt
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
                  - Incoming
                  - Reencrypt
            /pindata/translate:
              POST:
                summary: TranslatePinData
                description: >-
                  <p>Translates encrypted PIN block from and to ISO 9564 formats
                  0,1,3,4. For more information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/translate-pin-data.html">Translate
                  PIN data</a> in the <i>Amazon Web Services Payment
                  Cryptography User Guide</i>.</p> <p>PIN block translation
                  involves changing the encrytion of PIN block from one
                  encryption key to another encryption key and changing PIN
                  block format from one to another without PIN block data
                  leaving Amazon Web Services Payment Cryptography. The
                  encryption key transformation can be from PEK (Pin Encryption
                  Key) to BDK (Base Derivation Key) for DUKPT or from BDK for
                  DUKPT to PEK. Amazon Web Services Payment Cryptography
                  supports <code>TDES</code> and <code>AES</code> key derivation
                  type for DUKPT tranlations. You can use this operation for
                  P2PE (Point to Point Encryption) use cases where the
                  encryption keys should change but the processing system either
                  does not need to, or is not permitted to, decrypt the
                  data.</p> <p>The allowed combinations of PIN block format
                  translations are guided by PCI. It is important to note that
                  not all encrypted PIN block formats (example, format 1)
                  require PAN (Primary Account Number) as input. And as such,
                  PIN block format that requires PAN (example, formats 0,3,4)
                  cannot be translated to a format (format 1) that does not
                  require a PAN for generation. </p> <p>For information about
                  valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>.</p> <note> <p>At
                  this time, Amazon Web Services Payment Cryptography does not
                  support translations to PIN format 4.</p> </note> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>GeneratePinData</a> </p>
                  </li> <li> <p> <a>VerifyPinData</a> </p> </li> </ul>
                tags:
                  - Translations
                  - Pin
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
                  - Incoming
                  - Reencrypt
                  - Translations
            /cryptogram/verify:
              POST:
                summary: VerifyAuthRequestCryptogram
                description: >-
                  <p>Verifies Authorization Request Cryptogram (ARQC) for a EMV
                  chip payment card authorization. For more information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/data-operations.verifyauthrequestcryptogram.html">Verify
                  auth request cryptogram</a> in the <i>Amazon Web Services
                  Payment Cryptography User Guide</i>.</p> <p>ARQC generation is
                  done outside of Amazon Web Services Payment Cryptography and
                  is typically generated on a point of sale terminal for an EMV
                  chip card to obtain payment authorization during transaction
                  time. For ARQC verification, you must first import the ARQC
                  generated outside of Amazon Web Services Payment Cryptography
                  by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_ImportKey.html">ImportKey</a>.
                  This operation uses the imported ARQC and an major encryption
                  key (DUKPT) created by calling <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/APIReference/API_CreateKey.html">CreateKey</a>
                  to either provide a boolean ARQC verification result or
                  provide an APRC (Authorization Response Cryptogram) response
                  using Method 1 or Method 2. The <code>ARPC_METHOD_1</code>
                  uses <code>AuthResponseCode</code> to generate ARPC and
                  <code>ARPC_METHOD_2</code> uses <code>CardStatusUpdate</code>
                  to generate ARPC. </p> <p>For information about valid keys for
                  this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>.</p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p>
                  <a>VerifyCardValidationData</a> </p> </li> <li> <p>
                  <a>VerifyPinData</a> </p> </li> </ul>
                tags:
                  - Verify
                  - Authentication
                  - Request
                  - Cryptogram
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
                  - Incoming
                  - Reencrypt
                  - Translations
                  - Cryptogram
                  - Verify
            /cardvalidationdata/verify:
              POST:
                summary: VerifyCardValidationData
                description: >-
                  <p>Verifies card-related validation data using algorithms such
                  as Card Verification Values (CVV/CVV2), Dynamic Card
                  Verification Values (dCVV/dCVV2) and Card Security Codes
                  (CSC). For more information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/verify-card-data.html">Verify
                  card data</a> in the <i>Amazon Web Services Payment
                  Cryptography User Guide</i>.</p> <p>This operation validates
                  the CVV or CSC codes that is printed on a payment credit or
                  debit card during card payment transaction. The input values
                  are typically provided as part of an inbound transaction to an
                  issuer or supporting platform partner. Amazon Web Services
                  Payment Cryptography uses CVV or CSC, PAN (Primary Account
                  Number) and expiration date of the card to check its validity
                  during transaction processing. In this operation, the CVK
                  (Card Verification Key) encryption key for use with card data
                  verification is same as the one in used for
                  <a>GenerateCardValidationData</a>. </p> <p>For information
                  about valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p>
                  <a>GenerateCardValidationData</a> </p> </li> <li> <p>
                  <a>VerifyAuthRequestCryptogram</a> </p> </li> <li> <p>
                  <a>VerifyPinData</a> </p> </li> </ul>
                tags:
                  - Verify
                  - Cards
                  - Validations
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
                  - Incoming
                  - Reencrypt
                  - Translations
                  - Cryptogram
                  - Verify
            /mac/verify:
              POST:
                summary: VerifyMac
                description: >-
                  <p>Verifies a Message Authentication Code (MAC). </p> <p>You
                  can use this operation when keys won't be shared but mutual
                  data is present on both ends for validation. In this case,
                  known data values are used to generate a MAC on both ends for
                  verification without sending or receiving data in ciphertext
                  or plaintext. You can use this operation to verify a DUPKT,
                  HMAC or EMV MAC by setting generation attributes and algorithm
                  to the associated values. Use the same encryption key for MAC
                  verification as you use for <a>GenerateMac</a>. </p> <p>For
                  information about valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>GenerateMac</a> </p>
                  </li> </ul>
                tags:
                  - Verify
                  - Mac
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
                  - Incoming
                  - Reencrypt
                  - Translations
                  - Cryptogram
                  - Verify
            /pindata/verify:
              POST:
                summary: VerifyPinData
                description: >-
                  <p>Verifies pin-related data such as PIN and PIN Offset using
                  algorithms including VISA PVV and IBM3624. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/verify-pin-data.html">Verify
                  PIN data</a> in the <i>Amazon Web Services Payment
                  Cryptography User Guide</i>.</p> <p>This operation verifies
                  PIN data for user payment card. A card holder PIN data is
                  never transmitted in clear to or from Amazon Web Services
                  Payment Cryptography. This operation uses PIN Verification Key
                  (PVK) for PIN or PIN Offset generation and then encrypts it
                  using PIN Encryption Key (PEK) to create an
                  <code>EncryptedPinBlock</code> for transmission from Amazon
                  Web Services Payment Cryptography. </p> <p>For information
                  about valid keys for this operation, see <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/keys-validattributes.html">Understanding
                  key attributes</a> and <a
                  href="https://docs.aws.amazon.com/payment-cryptography/latest/userguide/crypto-ops-validkeys-ops.html">Key
                  types for specific data operations</a> in the <i>Amazon Web
                  Services Payment Cryptography User Guide</i>. </p> <p>
                  <b>Cross-account use</b>: This operation can't be used across
                  different Amazon Web Services accounts.</p> <p> <b>Related
                  operations:</b> </p> <ul> <li> <p> <a>GeneratePinData</a> </p>
                  </li> <li> <p> <a>TranslatePinData</a> </p> <
                tags:
                  - Verify
                  - Pin
                  - Data
                  - Keys
                  - Identifiers
                  - Decrypt
                  - Encrypt
                  - Card Validation Data
                  - Generate
                  - Mac
                  - Pin Data
                  - Incoming
                  - Reencrypt
                  - Translations
                  - Cryptogram
                  - Veri
    overlays:
      - type: APIs.io Search
        url: overlays/payment-cryptography-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payment-cryptography-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:payment-cryptography-data
  - name: vpc-lattice
    description: >-
      <p>Amazon VPC Lattice is a fully managed application networking service
      that you use to connect, secure, and monitor all of your services across
      multiple accounts and virtual private clouds (VPCs). Amazon VPC Lattice
      interconnects your microservices and legacy services within a logical
      boundary, so that you can discover and manage them more efficiently. For
      more information, see the <a
      href="https://docs.aws.amazon.com/vpc-lattice/latest/ug/">Amazon VPC
      Lattice User Guide</a> </p>
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
            title: vpc-lattice
          paths:
            /services/{serviceIdentifier}/listeners/{listenerIdentifier}/rules:
              GET:
                summary: ListRules
                description: <p>Lists the rules for the listener.</p>
                tags:
                  - Lists
                  - Rules
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
            /accesslogsubscriptions:
              GET:
                summary: ListAccessLogSubscriptions
                description: >-
                  <p>Lists all access log subscriptions for the specified
                  service network or service.</p>
                tags:
                  - Lists
                  - Access
                  - Logs
                  - Subscriptions
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
            /services/{serviceIdentifier}/listeners:
              GET:
                summary: ListListeners
                description: <p>Lists the listeners for the specified service.</p>
                tags:
                  - Lists
                  - Listeners
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
            /services:
              GET:
                summary: ListServices
                description: >-
                  <p>Lists the services owned by the caller account or shared
                  with the caller account.</p>
                tags:
                  - Lists
                  - Services
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
            /servicenetworks:
              GET:
                summary: ListServiceNetworks
                description: >-
                  <p>Lists the service networks owned by the caller account or
                  shared with the caller account. Also includes the account ID
                  in the ARN to show which account owns the service network.</p>
                tags:
                  - Lists
                  - Services
                  - Networks
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
            /servicenetworkserviceassociations:
              GET:
                summary: ListServiceNetworkServiceAssociations
                description: >-
                  <p>Lists the associations between the service network and the
                  service. You can filter the list either by service or service
                  network. You must provide either the service network
                  identifier or the service identifier.</p> <p>Every association
                  in Amazon VPC Lattice is given a unique Amazon Resource Name
                  (ARN), such as when a service network is associated with a VPC
                  or when a service is associated with a service network. If the
                  association is for a resource that is shared with another
                  account, the association will include the local account ID as
                  the prefix in the ARN for each account the resource is shared
                  with.</p>
                tags:
                  - Lists
                  - Services
                  - Networks
                  - Associations
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
            /servicenetworkvpcassociations:
              GET:
                summary: ListServiceNetworkVpcAssociations
                description: >-
                  <p>Lists the service network and VPC associations. You can
                  filter the list either by VPC or service network. You must
                  provide either the service network identifier or the VPC
                  identifier.</p>
                tags:
                  - Lists
                  - Services
                  - Networks
                  - VPC
                  - Associations
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
            /targetgroups:
              GET:
                summary: ListTargetGroups
                description: >-
                  <p>Lists your target groups. You can narrow your search by
                  using the filters below in your request.</p>
                tags:
                  - Lists
                  - Target
                  - Groups
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
            /accesslogsubscriptions/{accessLogSubscriptionIdentifier}:
              PATCH:
                summary: UpdateAccessLogSubscription
                description: <p>Updates the specified access log subscription.</p>
                tags:
                  - Update
                  - Access
                  - Logs
                  - Subscriptions
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
            /authpolicy/{resourceIdentifier}:
              PUT:
                summary: PutAuthPolicy
                description: <p>Creates or updates the auth policy.</p>
                tags:
                  - Put
                  - Authentication
                  - Policies
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
            /services/{serviceIdentifier}/listeners/{listenerIdentifier}:
              PATCH:
                summary: UpdateListener
                description: >-
                  <p>Updates the specified listener for the specified
                  service.</p>
                tags:
                  - Update
                  - Listeners
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
            /resourcepolicy/{resourceArn}:
              PUT:
                summary: PutResourcePolicy
                description: >-
                  <p>Attaches a resource-based permission policy to a service or
                  service network. The policy must contain the same actions and
                  condition statements as the Amazon Web Services Resource
                  Access Manager permission for sharing services and service
                  networks.</p>
                tags:
                  - Put
                  - Resources
                  - Policies
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
            /services/{serviceIdentifier}/listeners/{listenerIdentifier}/rules/{ruleIdentifier}:
              PATCH:
                summary: UpdateRule
                description: >-
                  <p>Updates a rule for the listener. You can't modify a default
                  listener rule. To modify a default listener rule, use
                  <code>UpdateListener</code>.</p>
                tags:
                  - Update
                  - Rules
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
            /services/{serviceIdentifier}:
              PATCH:
                summary: UpdateService
                description: <p>Updates the specified service.</p>
                tags:
                  - Update
                  - Services
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
            /servicenetworks/{serviceNetworkIdentifier}:
              PATCH:
                summary: UpdateServiceNetwork
                description: <p>Updates the specified service network.</p>
                tags:
                  - Update
                  - Services
                  - Networks
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
            /servicenetworkserviceassociations/{serviceNetworkServiceAssociationIdentifier}:
              GET:
                summary: GetServiceNetworkServiceAssociation
                description: >-
                  <p>Retrieves information about the specified association
                  between a service network and a service.</p>
                tags:
                  - Get
                  - Services
                  - Networks
                  - Association
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
            /servicenetworkvpcassociations/{serviceNetworkVpcAssociationIdentifier}:
              PATCH:
                summary: UpdateServiceNetworkVpcAssociation
                description: >-
                  <p>Updates the service network and VPC association. Once you
                  add a security group, it cannot be removed.</p>
                tags:
                  - Update
                  - Services
                  - Networks
                  - VPC
                  - Association
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
                  - VPC
            /targetgroups/{targetGroupIdentifier}:
              PATCH:
                summary: UpdateTargetGroup
                description: <p>Updates the specified target group.</p>
                tags:
                  - Update
                  - Target
                  - Group
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
                  - VPC
                  - Group
            /targetgroups/{targetGroupIdentifier}/deregistertargets:
              POST:
                summary: DeregisterTargets
                description: >-
                  <p>Deregisters the specified targets from the specified target
                  group.</p>
                tags:
                  - Deregister
                  - Targets
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
                  - VPC
                  - Group
                  - Deregister Targets
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes the specified tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
                  - VPC
                  - Group
                  - Deregister Targets
            /targetgroups/{targetGroupIdentifier}/listtargets:
              POST:
                summary: ListTargets
                description: >-
                  <p>Lists the targets for the target group. By default, all
                  targets are included. You can use this API to check the health
                  status of targets. You can also ﬁlter the results by target.
                  </p>
                tags:
                  - Lists
                  - Targets
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
                  - VPC
                  - Group
                  - Deregister Targets
                  - Targets
            /targetgroups/{targetGroupIdentifier}/registertargets:
              POST:
                summary: RegisterTargets
                description: >-
                  <p>Registers the targets with the target group. If it's a
                  Lambda target, you can only have one target in a target 
                tags:
                  - Register
                  - Targets
                  - Identifiers
                  - Listeners
                  - Listeners
                  - Rules
                  - Access Log Subscriptions
                  - Services
                  - Service Networks
                  - Service Network Service Associations
                  - Service Network VPC Associations
                  - Target Groups
                  - Logs
                  - Subscriptions
                  - ARN
                  - Rules
                  - Networks
                  - Services
                  - Association
                  - VPC
                  - Group
                  - Deregister Targets
                  - Targets
                  - Registertarge
    overlays:
      - type: APIs.io Search
        url: overlays/vpc-lattice-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/vpc-lattice-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:vpc-lattice
  - name: Symphony Authenticator API
    description: >-
      Tailor your portfolio exposures and risks using our hedging and
      optimization tools. Dynamically manage objectives and constraints while
      controlling for cost and tradability to meet your investment goals.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.developers.symphony.com/bots/authentication
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.developers.symphony.com/bots/authentication
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Authenticator API
          paths:
            /v1/authenticate:
              post:
                summary: Authenticate.
                description: >
                  Based on the SSL client certificate presented by the TLS
                  layer, authenticate

                  the API caller and return a session token.
                tags:
                  - Authenticate.
                  - V1
                  - Authenticate
            /v1/app/pod/certificate:
              get:
                summary: >
                  Retrieve the certificate that can be use to validate the JWT
                  token obtain

                  through the extension application authentication flow.
                tags:
                  - Retrieve
                  - The
                  - Certificate
                  - That
                  - Can
                  - Be
                  - Use
                  - To
                  - Validate
                  - Token
                  - |-
                    Obtain
                    through
                  - Extension
                  - Application
                  - Authentication
                  - |
                    Flow.
                  - V1
                  - Authenticate
                  - App
                  - Pod
                  - Certificate
            /v1/logout:
              post:
                summary: Logout.
                description: |
                  Logout a users session.
                tags:
                  - Logout.
                  - V1
                  - Authenticate
                  - App
                  - Pod
                  - Certificate
                  - Logout
          definitions:
            Error:
              type: object
              properties:
                code:
                  type: integer
                  format: int32
                message:
                  type: string
            Token:
              type: object
              properties:
                name:
                  description: >
                    The name of the header in which the token should be
                    presented on subsequent API calls.
                  type: string
                token:
                  type: string
                  description: >
                    Authentication token that should be passed as header in each
                    API rest calls.

                    This should be considered opaque data by the client. It is
                    not intended to contain any data interpretable by the

                    client. The format is secret and subject to change without
                    notice.
                authorizationToken:
                  type: string
                  description: >
                    (Beta) Short lived access token built from a user session.
                    This field is still on Beta, please continue using 

                    the returned "token" instead.
            PodCertificate:
              type: object
              properties:
                certificate:
                  description: Certificate in PEM format
                  type: string
            SuccessResponse:
              type: object
              properties:
                message:
                  type: null
    aid: symphony:symphony-authenticator-api
    overlays:
      - type: APIs.io Search
        url: overlays/authenticator-openapi-search.yml
  - name: Symphony Login API
    description: >-
      Programmatically manage your portfolio lifecycle from creation and update
      to scheduling reports with full control over visibility and sharing.
      Automate your portfolio workflow using our APIs — leaving you to focus on
      the alpha driving decisions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://symphony-1.gitbook.io/restapi
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://symphony-1.gitbook.io/restapi
      - type: OpenAPI
        data:
          swagger: '2.0'
          info:
            title: Login API
          paths:
            /pubkey/authenticate:
              post:
                summary: Authenticate with public key
                description: >
                  Based on an authentication request token signed by the
                  caller's RSA private key,

                  authenticate the API caller and return a session token.


                  A HTTP 401 Unauthorized error is returned on errors during
                  authentication (e.g. invalid user,

                  malformed authentication token, user's public key not imported
                  in the pod, invalid token signature etc.).
                tags:
                  - Authenticate
                  - With
                  - Public
                  - Key
                  - Pubkey
                  - Authenticate
            /v1/pubkey/app/authenticate/extensionApp:
              post:
                summary: Authenticate extension app with public key
                description: >
                  Based on an authentication request token signed by the
                  caller's RSA private key,

                  authenticate the API caller and return a session token.


                  A HTTP 401 Unauthorized error is returned on errors during
                  authentication (e.g. invalid user,

                  malformed authentication token, user's public key not imported
                  in the pod, invalid token signature etc.).
                tags:
                  - Authenticate
                  - Extension
                  - App
                  - With
                  - Public
                  - Key
                  - Pubkey
                  - Authenticate
                  - App
            /pubkey/app/authenticate:
              post:
                summary: Authenticate an App with public key
                description: >
                  Based on an authentication request token signed by the
                  application's RSA private key,

                  authenticate the API caller and return a session token.


                  A HTTP 401 Unauthorized error is returned on errors during
                  authentication (e.g. invalid app,

                  malformed authentication token, app's public key not imported
                  in the pod, invalid token signature etc.).
                tags:
                  - Authenticate
                  - An
                  - App
                  - With
                  - Public
                  - Key
                  - Pubkey
                  - Authenticate
                  - App
            /pubkey/app/username/{username}/authenticate:
              post:
                summary: >-
                  Authenticate an application in a delegated context to act on
                  behalf of a user
                tags:
                  - Authenticate
                  - An
                  - Application
                  - In
                  - Delegated
                  - Context
                  - To
                  - Act
                  - 'On'
                  - Behalf
                  - Of
                  - User
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
            /pubkey/app/user/{userId}/authenticate:
              post:
                summary: >-
                  Authenticate an application in a delegated context to act on
                  behalf of a user
                tags:
                  - Authenticate
                  - An
                  - Application
                  - In
                  - Delegated
                  - Context
                  - To
                  - Act
                  - 'On'
                  - Behalf
                  - Of
                  - User
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
                  - Id
            /idm/tokens:
              post:
                summary: >-
                  Returns a valid OAuth2 access token from a given session token
                  to be used for authentication
                tags:
                  - Returns
                  - Valid
                  - Auth2
                  - Access
                  - Token
                  - From
                  - Given
                  - Session
                  - To
                  - Be
                  - Used
                  - For
                  - Authentication
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
                  - Id
                  - Idm
                  - Tokens
            /idm/keys:
              get:
                summary: Returns the Common Access Token (JWT) public keys as a JWKS.
                description: >-
                  This is a public endpoint, no authentication is required. The
                  JWKS can be used to verify JWT issued by the idm/tokens
                  endpoint. Since SBE 20.14.
                tags:
                  - Returns
                  - The
                  - Common
                  - Access
                  - Token
                  - T)
                  - Public
                  - Keys
                  - As
                  - S.
                  - Pubkey
                  - Authenticate
                  - App
                  - Username
                  - Id
                  - Idm
                  - Tokens
                  - Keys
          definitions:
            Error:
              type: object
              properties:
                code:
                  type: integer
                  format: int32
                message:
                  type: string
            Token:
              type: object
              properties:
                name:
                  description: >
                    The name of the header in which the token should be
                    presented on subsequent API calls.
                  type: string
                token:
                  type: string
                  description: >
                    Authentication token that should be passed as header in each
                    API rest calls.

                    This should be considered opaque data by the client. It is
                    not intended to contain any data interpretable by the

                    client. The format is secret and subject to change without
                    notice.
                authorizationToken:
                  type: string
                  description: >
                    (Beta) Short lived access token built from a user session.
                    This field is still on Beta, please continue using 

                    the returned "token" instead.
            AuthenticateRequest:
              type: object
              description: Request body for pubkey authentication
              properties:
                token:
                  type: string
                  description: >-
                    a JWT containing the caller's username or application
                    appGroupId and an expiration date, signed by the caller's
                    private key.
            AuthenticateExtensionAppRequest:
              type: object
              description: Request body for extension app authentication
              properties:
                appToken:
                  type: string
                  description: application generated token
                authToken:
                  type: string
                  description: >-
                    a JWT containing the caller's username and an expiration
                    date, signed by the caller's private key.
            ExtensionAppTokens:
              type: object
              properties:
                appId:
                  description: Application ID
                  type: string
                appToken:
                  description: >
                    This token generated by the application when calling
                    authentication endpoint
                  type: string
                symphonyToken:
                  type: string
                  description: >
                    This token generated by Symphony and should be used by the
                    application to verify that it's talking to Symphony.
                expireAt:
                  type: integer
                  format: int64
                  description: unix timestamp when the token expired
            JwtToken:
              type: object
              properties:
                token_type:
                  type: string
                  description: Type of token, string "Bearer"
                expires_in:
                  type: integer
                  format: int64
                  description: Duration of time the access token is granted for in seconds
                access_token:
                  type: string
                  description: >
                    A JWT containing the caller's username or application, an
                    expiration date and a set of entitlements related to the

                    specified scope, signed by the caller's private key.
            Jwks:
              type: object
              properties:
                keys:
                  type: array
                  items:
                    $ref: '#/definitions/JwksEntry'
            JwksEntry:
              type: object
              description: >-
                A JWK object as defined in
                https://datatracker.ietf.org/doc/html/rfc7517#section-4.
              additionalProperties:
                type: null
    aid: symphony:symphony-login-api
    overlays:
      - type: APIs.io Search
        url: overlays/login-openapi-search.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---