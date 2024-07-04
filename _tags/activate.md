---
name: Activate
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/activate.png
url: https://example.com/apis/activate.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Activate
apis:
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
  - name: connect
    description: >-
      <p>Amazon Connect is a cloud-based contact center solution that you use to
      set up and manage a customer contact center and provide reliable customer
      engagement at any scale.</p> <p>Amazon Connect provides metrics and
      real-time reporting that enable you to optimize contact routing. You can
      also resolve customer issues more efficiently by getting customers in
      touch with the appropriate agents.</p> <p>There are limits to the number
      of Amazon Connect resources that you can create. There are also limits to
      the number of requests that you can make per second. For more information,
      see <a
      href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">Amazon
      Connect Service Quotas</a> in the <i>Amazon Connect Administrator
      Guide</i>.</p> <p>You can connect programmatically to an Amazon Web
      Services service by using an endpoint. For a list of Amazon Connect
      endpoints, see <a
      href="https://docs.aws.amazon.com/general/latest/gr/connect_region.html">Amazon
      Connect Endpoints</a>.</p>
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
            title: connect
          paths:
            /evaluation-forms/{InstanceId}/{EvaluationFormId}/activate:
              POST:
                summary: ActivateEvaluationForm
                description: >-
                  <p>Activates an evaluation form in the specified Amazon
                  Connect instance. After the evaluation form is activated, it
                  is available to start new evaluations based on the form. </p>
                tags:
                  - Activate
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
            /analytics-data/instance/{InstanceId}/association:
              GET:
                summary: ListAnalyticsDataAssociations
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Lists the association status of
                  requested dataset ID for a given Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Analytics
                  - Data
                  - Associations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
            /instance/{InstanceId}/approved-origin:
              DELETE:
                summary: DisassociateApprovedOrigin
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Revokes access to integrated
                  applications from Amazon Connect.</p>
                tags:
                  - Disassociate
                  - Approved
                  - Origin
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
            /instance/{InstanceId}/bot:
              POST:
                summary: DisassociateBot
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Revokes authorization from the
                  specified instance to access the specified Amazon Lex or
                  Amazon Lex V2 bot. </p>
                tags:
                  - Disassociate
                  - Bot
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
            /default-vocabulary/{InstanceId}/{LanguageCode}:
              PUT:
                summary: AssociateDefaultVocabulary
                description: >-
                  <p>Associates an existing vocabulary as the default. Contact
                  Lens for Amazon Connect uses the vocabulary in post-call and
                  real-time analysis sessions for the given language.</p>
                tags:
                  - Associate
                  - Default
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
            /flow-associations/{InstanceId}:
              PUT:
                summary: AssociateFlow
                description: <p>Associates a connect resource to a flow.</p>
                tags:
                  - Associate
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
            /instance/{InstanceId}/storage-config:
              PUT:
                summary: AssociateInstanceStorageConfig
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Associates a storage resource type
                  for the first time. You can only associate one type of storage
                  configuration in a single call. This means, for example, that
                  you can't define an instance with multiple S3 buckets for
                  storing chat transcripts.</p> <p>This API does not create a
                  resource that doesn't exist. It only associates it to the
                  instance. Ensure that the resource being specified in the
                  storage configuration, like an S3 bucket, exists when being
                  used for association.</p>
                tags:
                  - Associate
                  - Instances
                  - Storage
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
            /instance/{InstanceId}/lambda-function:
              DELETE:
                summary: DisassociateLambdaFunction
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Remove the Lambda function from the
                  dropdown options available in the relevant flow blocks.</p>
                tags:
                  - Disassociate
                  - Lambda
                  - Functions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
            /instance/{InstanceId}/lex-bot:
              DELETE:
                summary: DisassociateLexBot
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Revokes authorization from the
                  specified instance to access the specified Amazon Lex bot.</p>
                tags:
                  - Disassociate
                  - Lex
                  - Bot
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
            /phone-number/{PhoneNumberId}/contact-flow:
              DELETE:
                summary: DisassociatePhoneNumberContactFlow
                description: >-
                  <p>Removes the flow association from a phone number claimed to
                  your Amazon Connect instance.</p> <important> <p>If the number
                  is claimed to a traffic distribution group, and you are
                  calling this API using an instance in the Amazon Web Services
                  Region where the traffic distribution group was created, you
                  can use either a full phone number ARN or UUID value for the
                  <code>PhoneNumberId</code> URI request parameter. However, if
                  the number is claimed to a traffic distribution group and you
                  are calling this API using an instance in the alternate Amazon
                  Web Services Region associated with the traffic distribution
                  group, you must provide a full phone number ARN. If a UUID is
                  provided in this scenario, you will receive a
                  <code>ResourceNotFoundException</code>.</p> </important>
                tags:
                  - Disassociate
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
            /queues/{InstanceId}/{QueueId}/associate-quick-connects:
              POST:
                summary: AssociateQueueQuickConnects
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Associates a set of quick connects
                  with a queue.</p>
                tags:
                  - Associate
                  - Queues
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
            /routing-profiles/{InstanceId}/{RoutingProfileId}/associate-queues:
              POST:
                summary: AssociateRoutingProfileQueues
                description: <p>Associates a set of queues with a routing profile.</p>
                tags:
                  - Associate
                  - Routing
                  - Profiles
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
            /instance/{InstanceId}/security-key:
              PUT:
                summary: AssociateSecurityKey
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Associates a security key to the
                  instance.</p>
                tags:
                  - Associate
                  - Security
                  - Keys
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
            /traffic-distribution-group/{TrafficDistributionGroupId}/user:
              GET:
                summary: ListTrafficDistributionGroupUsers
                description: <p>Lists traffic distribution group users.</p>
                tags:
                  - Lists
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
            /users/{InstanceId}/{UserId}/associate-proficiencies:
              POST:
                summary: AssociateUserProficiencies
                description: <p>&gt;Associates a set of proficiencies with a user.</p>
                tags:
                  - Associate
                  - Users
                  - Proficiencies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
            /analytics-data/instance/{InstanceId}/associations:
              POST:
                summary: BatchDisassociateAnalyticsDataSet
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Removes a list of analytics datasets
                  associated with a given Amazon Connect instance. You can
                  disassociate multiple datasets in a single call.</p>
                tags:
                  - Batches
                  - Disassociate
                  - Analytics
                  - Data
                  - Sets
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
            /flow-associations-batch/{InstanceId}:
              POST:
                summary: BatchGetFlowAssociation
                description: <p>Retrieve the flow associations for the given resources.</p>
                tags:
                  - Batches
                  - Get
                  - Flow
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
            /contact/batch/{InstanceId}:
              PUT:
                summary: BatchPutContact
                description: >-
                  <note> <p>Only the Amazon Connect outbound campaigns service
                  principal is allowed to assume a role in your account and call
                  this API.</p> </note> <p>Allows you to create a batch of
                  contacts in Amazon Connect. The outbound campaigns capability
                  ingests dial requests via the <a
                  href="https://docs.aws.amazon.com/connect-outbound/latest/APIReference/API_PutDialRequestBatch.html">PutDialRequestBatch</a>
                  API. It then uses BatchPutContact to create contacts
                  corresponding to those dial requests. If agents are available,
                  the dial requests are dialed out, which results in a voice
                  call. The resulting voice call uses the same contactId that
                  was created by BatchPutContact. </p>
                tags:
                  - Batches
                  - Put
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
            /phone-number/claim:
              POST:
                summary: ClaimPhoneNumber
                description: >-
                  <p>Claims an available phone number to your Amazon Connect
                  instance or traffic distribution group. You can call this API
                  only in the same Amazon Web Services Region where the Amazon
                  Connect instance or traffic distribution group was
                  created.</p> <p>For more information about how to use this
                  operation, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/claim-phone-number.html">Claim
                  a phone number in your country</a> and <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/claim-phone-numbers-traffic-distribution-groups.html">Claim
                  phone numbers to traffic distribution groups</a> in the
                  <i>Amazon Connect Administrator Guide</i>. </p> <important>
                  <p>You can call the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_SearchAvailablePhoneNumbers.html">SearchAvailablePhoneNumbers</a>
                  API for available phone numbers that you can claim. Call the
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribePhoneNumber.html">DescribePhoneNumber</a>
                  API to verify the status of a previous <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ClaimPhoneNumber.html">ClaimPhoneNumber</a>
                  operation.</p> </important> <p>If you plan to claim and
                  release numbers frequently during a 30 day period, contact us
                  for a service quota exception. Otherwise, it is possible you
                  will be blocked from claiming and releasing any more numbers
                  until 30 days past the oldest number released has expired.</p>
                  <p>By default you can claim and release up to 200% of your
                  maximum number of active phone numbers during any 30 day
                  period. If you claim and release phone numbers using the UI or
                  API during a rolling 30 day cycle that exceeds 200% of your
                  phone number service level quota, you will be blocked from
                  claiming any more numbers until 30 days past the oldest number
                  released has expired. </p> <p>For example, if you already have
                  99 claimed numbers and a service level quota of 99 phone
                  numbers, and in any 30 day period you release 99, claim 99,
                  and then release 99, you will have exceeded the 200% limit. At
                  that point you are blocked from claiming any more numbers
                  until you open an Amazon Web Services support ticket.</p>
                tags:
                  - Claim
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /agent-status/{InstanceId}:
              GET:
                summary: ListAgentStatuses
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Lists agent statuses.</p>
                tags:
                  - Lists
                  - Agent
                  - Statuses
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /contact-flows/{InstanceId}:
              PUT:
                summary: CreateContactFlow
                description: >-
                  <p>Creates a flow for the specified Amazon Connect
                  instance.</p> <p>You can also create and update flows using
                  the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Create
                  - Contacts
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /contact-flow-modules/{InstanceId}:
              PUT:
                summary: CreateContactFlowModule
                description: >-
                  <p>Creates a flow module for the specified Amazon Connect
                  instance. </p>
                tags:
                  - Create
                  - Contacts
                  - Flow
                  - Modules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /evaluation-forms/{InstanceId}:
              GET:
                summary: ListEvaluationForms
                description: >-
                  <p>Lists evaluation forms in the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /hours-of-operations/{InstanceId}:
              PUT:
                summary: CreateHoursOfOperation
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Creates hours of operation. </p>
                tags:
                  - Create
                  - Hours
                  - Of
                  - Operation
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /instance:
              GET:
                summary: ListInstances
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Return a list of instances which are
                  in active state, creation-in-progress state, and failed state.
                  Instances that aren't successfully created (they are in a
                  failed state) are returned only for 24 hours after the
                  CreateInstance API was invoked.</p>
                tags:
                  - Lists
                  - Instances
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
            /instance/{InstanceId}/integration-associations:
              GET:
                summary: ListIntegrationAssociations
                description: >-
                  <p>Provides summary information about the Amazon Web Services
                  resource associations for the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Integrations
                  - Associations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
            /contact/create-participant:
              POST:
                summary: CreateParticipant
                description: >-
                  <p>Adds a new participant into an on-going chat contact. For
                  more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-customize-flow.html">Customize
                  chat flow experiences by integrating custom
                  participants</a>.</p>
                tags:
                  - Create
                  - Participants
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
            /contact/persistent-contact-association/{InstanceId}/{InitialContactId}:
              POST:
                summary: CreatePersistentContactAssociation
                description: >-
                  <p>Enables rehydration of chats for the lifespan of a contact.
                  For more information about chat rehydration, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-persistence.html">Enable
                  persistent chat</a> in the <i>Amazon Connect Administrator
                  Guide</i>. </p>
                tags:
                  - Create
                  - Persistent
                  - Contacts
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /predefined-attributes/{InstanceId}:
              GET:
                summary: ListPredefinedAttributes
                description: >-
                  <p>Lists predefined attributes for the specified Amazon
                  Connect instance.</p>
                tags:
                  - Lists
                  - Predefined
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /prompts/{InstanceId}:
              PUT:
                summary: CreatePrompt
                description: >-
                  <p>Creates a prompt. For more information about prompts, such
                  as supported file types and maximum length, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html">Create
                  prompts</a> in the <i>Amazon Connect Administrator's
                  Guide</i>.</p>
                tags:
                  - Create
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /queues/{InstanceId}:
              PUT:
                summary: CreateQueue
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Creates a new queue for the
                  specified Amazon Connect instance.</p> <important> <ul> <li>
                  <p>If the phone number is claimed to a traffic distribution
                  group that was created in the same Region as the Amazon
                  Connect instance where you are calling this API, then you can
                  use a full phone number ARN or a UUID for
                  <code>OutboundCallerIdNumberId</code>. However, if the phone
                  number is claimed to a traffic distribution group that is in
                  one Region, and you are calling this API from an instance in
                  another Amazon Web Services Region that is associated with the
                  traffic distribution group, you must provide a full phone
                  number ARN. If a UUID is provided in this scenario, you will
                  receive a <code>ResourceNotFoundException</code>.</p> </li>
                  <li> <p>Only use the phone number ARN format that doesn't
                  contain <code>instance</code> in the path, for example,
                  <code>arn:aws:connect:us-east-1:1234567890:phone-number/uuid</code>.
                  This is the same ARN format that is returned when you call the
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  API.</p> </li> <li> <p>If you plan to use IAM policies to
                  allow/deny access to this API for phone number resources
                  claimed to a traffic distribution group, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/security_iam_resource-level-policy-examples.html#allow-deny-queue-actions-replica-region">Allow
                  or Deny queue API actions for phone numbers in a replica
                  Region</a>.</p> </li> </ul> </important>
                tags:
                  - Create
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /quick-connects/{InstanceId}:
              GET:
                summary: ListQuickConnects
                description: >-
                  <p>Provides information about the quick connects for the
                  specified Amazon Connect instance. </p>
                tags:
                  - Lists
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /routing-profiles/{InstanceId}:
              PUT:
                summary: CreateRoutingProfile
                description: <p>Creates a new routing profile.</p>
                tags:
                  - Create
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /rules/{InstanceId}:
              GET:
                summary: ListRules
                description: >-
                  <p>List all rules for the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Rules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /security-profiles/{InstanceId}:
              PUT:
                summary: CreateSecurityProfile
                description: <p>Creates a security profile.</p>
                tags:
                  - Create
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
            /instance/{InstanceId}/task/template:
              GET:
                summary: ListTaskTemplates
                description: >-
                  <p>Lists task templates for the specified Amazon Connect
                  instance.</p>
                tags:
                  - Lists
                  - Tasks
                  - Templates
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
            /traffic-distribution-group:
              PUT:
                summary: CreateTrafficDistributionGroup
                description: >-
                  <p>Creates a traffic distribution group given an Amazon
                  Connect instance that has been replicated. </p> <note> <p>The
                  <code>SignInConfig</code> distribution is available only on a
                  default <code>TrafficDistributionGroup</code> (see the
                  <code>IsDefault</code> parameter in the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_TrafficDistributionGroup.html">TrafficDistributionGroup</a>
                  data type). If you call <code>UpdateTrafficDistribution</code>
                  with a modified <code>SignInConfig</code> and a non-default
                  <code>TrafficDistributionGroup</code>, an
                  <code>InvalidRequestException</code> is returned.</p> </note>
                  <p>For more information about creating traffic distribution
                  groups, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/setup-traffic-distribution-groups.html">Set
                  up traffic distribution groups</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p>
                tags:
                  - Create
                  - Traffic
                  - Distributions
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
            /instance/{InstanceId}/integration-associations/{IntegrationAssociationId}/use-cases:
              GET:
                summary: ListUseCases
                description: <p>Lists the use cases for the integration association. </p>
                tags:
                  - Lists
                  - Use
                  - Cases
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /users/{InstanceId}:
              PUT:
                summary: CreateUser
                description: >-
                  <p>Creates a user account for the specified Amazon Connect
                  instance.</p> <important> <p>Certain <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_UserIdentityInfo.html">UserIdentityInfo</a>
                  parameters are required in some situations. For example,
                  <code>Email</code> is required if you are using SAML for
                  identity management. <code>FirstName</code> and
                  <code>LastName</code> are required if you are using Amazon
                  Connect or SAML for identity management.</p> </important>
                  <p>For information about how to create users using the Amazon
                  Connect admin website, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/user-management.html">Add
                  Users</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Create
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /user-hierarchy-groups/{InstanceId}:
              PUT:
                summary: CreateUserHierarchyGroup
                description: <p>Creates a new user hierarchy group.</p>
                tags:
                  - Create
                  - Users
                  - Hierarchy
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /views/{InstanceId}:
              GET:
                summary: ListViews
                description: >-
                  <p>Returns views in the given instance.</p> <p>Results are
                  sorted primarily by type, and secondarily by name.</p>
                tags:
                  - Lists
                  - Views
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
            /views/{InstanceId}/{ViewId}/versions:
              GET:
                summary: ListViewVersions
                description: >-
                  <p>Returns all the available versions for the specified Amazon
                  Connect instance and view identifier.</p> <p>Results will be
                  sorted from highest to lowest.</p>
                tags:
                  - Lists
                  - View
                  - Versions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
            /vocabulary/{InstanceId}:
              POST:
                summary: CreateVocabulary
                description: >-
                  <p>Creates a custom vocabulary associated with your Amazon
                  Connect instance. You can set a custom vocabulary to be your
                  default vocabulary for a given language. Contact Lens for
                  Amazon Connect uses the default vocabulary in post-call and
                  real-time contact analysis sessions for that language.</p>
                tags:
                  - Create
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
            /evaluation-forms/{InstanceId}/{EvaluationFormId}/deactivate:
              POST:
                summary: DeactivateEvaluationForm
                description: >-
                  <p>Deactivates an evaluation form in the specified Amazon
                  Connect instance. After a form is deactivated, it is no longer
                  available for users to start new evaluations based on the
                  form. </p>
                tags:
                  - Deactivate
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
            /contact-evaluations/{InstanceId}/{EvaluationId}:
              POST:
                summary: UpdateContactEvaluation
                description: >-
                  <p>Updates details about a contact evaluation in the specified
                  Amazon Connect instance. A contact evaluation must be in draft
                  state. Answers included in the request are merged with
                  existing answers for the given evaluation. An answer or note
                  can be deleted by passing an empty object (<code>{}</code>) to
                  the question identifier. </p>
                tags:
                  - Update
                  - Contacts
                  - Evaluations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
            /contact-flows/{InstanceId}/{ContactFlowId}:
              GET:
                summary: DescribeContactFlow
                description: >-
                  <p>Describes the specified flow.</p> <p>You can also create
                  and update flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Describe
                  - Contacts
                  - Flow
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
            /contact-flow-modules/{InstanceId}/{ContactFlowModuleId}:
              GET:
                summary: DescribeContactFlowModule
                description: <p>Describes the specified flow module.</p>
                tags:
                  - Describe
                  - Contacts
                  - Flow
                  - Modules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
            /evaluation-forms/{InstanceId}/{EvaluationFormId}:
              PUT:
                summary: UpdateEvaluationForm
                description: >-
                  <p>Updates details about a specific evaluation form version in
                  the specified Amazon Connect instance. Question and section
                  identifiers cannot be duplicated within the same evaluation
                  form.</p> <p>This operation does not support partial updates.
                  Instead it does a full update of evaluation form content.</p>
                tags:
                  - Update
                  - Evaluations
                  - Forms
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
            /hours-of-operations/{InstanceId}/{HoursOfOperationId}:
              POST:
                summary: UpdateHoursOfOperation
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the hours of operation.</p>
                tags:
                  - Update
                  - Hours
                  - Of
                  - Operation
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
            /instance/{InstanceId}:
              GET:
                summary: DescribeInstance
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns the current state of the
                  specified instance identifier. It tracks the instance while it
                  is being created and returns an error status, if applicable.
                  </p> <p>If an instance is not created successfully, the
                  instance status reason field returns details relevant to the
                  reason. The instance in a failed state is returned only for 24
                  hours after the CreateInstance API was invoked.</p>
                tags:
                  - Describe
                  - Instances
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
            /instance/{InstanceId}/integration-associations/{IntegrationAssociationId}:
              DELETE:
                summary: DeleteIntegrationAssociation
                description: >-
                  <p>Deletes an Amazon Web Services resource association from an
                  Amazon Connect instance. The association must not have any use
                  cases associated with it.</p>
                tags:
                  - Delete
                  - Integrations
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
            /predefined-attributes/{InstanceId}/{Name}:
              POST:
                summary: UpdatePredefinedAttribute
                description: >-
                  <p>Updates a predefined attribute for the specified Amazon
                  Connect instance.</p>
                tags:
                  - Update
                  - Predefined
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
            /prompts/{InstanceId}/{PromptId}:
              POST:
                summary: UpdatePrompt
                description: <p>Updates a prompt.</p>
                tags:
                  - Update
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
            /queues/{InstanceId}/{QueueId}:
              GET:
                summary: DescribeQueue
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Describes the specified queue.</p>
                tags:
                  - Describe
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
            /quick-connects/{InstanceId}/{QuickConnectId}:
              GET:
                summary: DescribeQuickConnect
                description: <p>Describes the quick connect.</p>
                tags:
                  - Describe
                  - Quick
                  - Connect
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
            /routing-profiles/{InstanceId}/{RoutingProfileId}:
              GET:
                summary: DescribeRoutingProfile
                description: <p>Describes the specified routing profile.</p>
                tags:
                  - Describe
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
            /rules/{InstanceId}/{RuleId}:
              PUT:
                summary: UpdateRule
                description: >-
                  <p>Updates a rule for the specified Amazon Connect
                  instance.</p> <p>Use the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/connect-rules-language.html">Rules
                  Function language</a> to code conditions for the rule. </p>
                tags:
                  - Update
                  - Rules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /security-profiles/{InstanceId}/{SecurityProfileId}:
              POST:
                summary: UpdateSecurityProfile
                description: <p>Updates a security profile.</p>
                tags:
                  - Update
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /instance/{InstanceId}/task/template/{TaskTemplateId}:
              POST:
                summary: UpdateTaskTemplate
                description: >-
                  <p>Updates details about a specific task template in the
                  specified Amazon Connect instance. This operation does not
                  support partial updates. Instead it does a full update of
                  template content.</p>
                tags:
                  - Update
                  - Tasks
                  - Templates
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /traffic-distribution-group/{TrafficDistributionGroupId}:
              GET:
                summary: DescribeTrafficDistributionGroup
                description: >-
                  <p>Gets details and status of a traffic distribution
                  group.</p>
                tags:
                  - Describe
                  - Traffic
                  - Distributions
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
            /instance/{InstanceId}/integration-associations/{IntegrationAssociationId}/use-cases/{UseCaseId}:
              DELETE:
                summary: DeleteUseCase
                description: <p>Deletes a use case from an integration association.</p>
                tags:
                  - Delete
                  - Use
                  - Case
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
            /users/{InstanceId}/{UserId}:
              GET:
                summary: DescribeUser
                description: >-
                  <p>Describes the specified user. You can <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/find-instance-arn.html">find
                  the instance ID in the Amazon Connect console</a> (it’s the
                  final part of the ARN). The console does not display the user
                  IDs. Instead, list the users and note the IDs provided in the
                  output.</p>
                tags:
                  - Describe
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
            /user-hierarchy-groups/{InstanceId}/{HierarchyGroupId}:
              GET:
                summary: DescribeUserHierarchyGroup
                description: <p>Describes the specified hierarchy group.</p>
                tags:
                  - Describe
                  - Users
                  - Hierarchy
                  - Group
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
            /views/{InstanceId}/{ViewId}:
              POST:
                summary: UpdateViewContent
                description: >-
                  <p>Updates the view content of the given view identifier in
                  the specified Amazon Connect instance.</p> <p>It performs
                  content validation if <code>Status</code> is set to
                  <code>SAVED</code> and performs full content validation if
                  <code>Status</code> is <code>PUBLISHED</code>. Note that the
                  <code>$SAVED</code> alias' content will always be updated, but
                  the <code>$LATEST</code> alias' content will only be updated
                  if <code>Status</code> is <code>PUBLISHED</code>.</p>
                tags:
                  - Update
                  - View
                  - Content
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
            /views/{InstanceId}/{ViewId}/versions/{ViewVersion}:
              DELETE:
                summary: DeleteViewVersion
                description: >-
                  <p>Deletes the particular version specified in
                  <code>ViewVersion</code> identifier.</p>
                tags:
                  - Delete
                  - View
                  - Versions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
            /vocabulary-remove/{InstanceId}/{VocabularyId}:
              POST:
                summary: DeleteVocabulary
                description: <p>Deletes the vocabulary that has the given identifier.</p>
                tags:
                  - Delete
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
            /agent-status/{InstanceId}/{AgentStatusId}:
              POST:
                summary: UpdateAgentStatus
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates agent status.</p>
                tags:
                  - Update
                  - Agent
                  - Status
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
            /contacts/{InstanceId}/{ContactId}:
              POST:
                summary: UpdateContact
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Adds or updates user-defined contact
                  information associated with the specified contact. At least
                  one field to be updated must be present in the request.</p>
                  <important> <p>You can add or update user-defined contact
                  information for both ongoing and completed contacts.</p>
                  </important>
                tags:
                  - Update
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
            /instance/{InstanceId}/attribute/{AttributeType}:
              POST:
                summary: UpdateInstanceAttribute
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the value for the specified
                  attribute type.</p>
                tags:
                  - Update
                  - Instances
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /instance/{InstanceId}/storage-config/{AssociationId}:
              POST:
                summary: UpdateInstanceStorageConfig
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates an existing configuration
                  for a resource type. This API is idempotent.</p>
                tags:
                  - Update
                  - Instances
                  - Storage
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /phone-number/{PhoneNumberId}:
              PUT:
                summary: UpdatePhoneNumber
                description: >-
                  <p>Updates your claimed phone number from its current Amazon
                  Connect instance or traffic distribution group to another
                  Amazon Connect instance or traffic distribution group in the
                  same Amazon Web Services Region.</p> <important> <p>After
                  using this API, you must verify that the phone number is
                  attached to the correct flow in the target instance or traffic
                  distribution group. You need to do this because the API
                  switches only the phone number to a new instance or traffic
                  distribution group. It doesn't migrate the flow configuration
                  of the phone number, too.</p> <p>You can call <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribePhoneNumber.html">DescribePhoneNumber</a>
                  API to verify the status of a previous <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_UpdatePhoneNumber.html">UpdatePhoneNumber</a>
                  operation.</p> </important>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /user-hierarchy-structure/{InstanceId}:
              POST:
                summary: UpdateUserHierarchyStructure
                description: >-
                  <p>Updates the user hierarchy structure: add, remove, and
                  rename user hierarchy levels.</p>
                tags:
                  - Update
                  - Users
                  - Hierarchy
                  - Structures
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /vocabulary/{InstanceId}/{VocabularyId}:
              GET:
                summary: DescribeVocabulary
                description: <p>Describes the specified vocabulary.</p>
                tags:
                  - Describe
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
            /flow-associations/{InstanceId}/{ResourceId}/{ResourceType}:
              GET:
                summary: GetFlowAssociation
                description: <p>Retrieves the flow associated for a given resource.</p>
                tags:
                  - Get
                  - Flow
                  - Association
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
            /queues/{InstanceId}/{QueueId}/disassociate-quick-connects:
              POST:
                summary: DisassociateQueueQuickConnects
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Disassociates a set of quick
                  connects from a queue.</p>
                tags:
                  - Disassociate
                  - Queues
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /routing-profiles/{InstanceId}/{RoutingProfileId}/disassociate-queues:
              POST:
                summary: DisassociateRoutingProfileQueues
                description: <p>Disassociates a set of queues from a routing profile.</p>
                tags:
                  - Disassociate
                  - Routing
                  - Profiles
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /instance/{InstanceId}/security-key/{AssociationId}:
              DELETE:
                summary: DisassociateSecurityKey
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Deletes the specified security
                  key.</p>
                tags:
                  - Disassociate
                  - Security
                  - Keys
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /users/{InstanceId}/{UserId}/disassociate-proficiencies:
              POST:
                summary: DisassociateUserProficiencies
                description: <p>Disassociates a set of proficiencies from a user.</p>
                tags:
                  - Disassociate
                  - Users
                  - Proficiencies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /users/{InstanceId}/{UserId}/contact:
              POST:
                summary: DismissUserContact
                description: >-
                  <p>Dismisses contacts from an agent’s CCP and returns the
                  agent to an available state, which allows the agent to receive
                  a new routed contact. Contacts can only be dismissed if they
                  are in a <code>MISSED</code>, <code>ERROR</code>,
                  <code>ENDED</code>, or <code>REJECTED</code> state in the <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/about-contact-states.html">Agent
                  Event Stream</a>.</p>
                tags:
                  - Dismiss
                  - Users
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /contact/attributes/{InstanceId}/{InitialContactId}:
              GET:
                summary: GetContactAttributes
                description: >-
                  <p>Retrieves the contact attributes for the specified
                  contact.</p>
                tags:
                  - Get
                  - Contacts
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/current/{InstanceId}:
              POST:
                summary: GetCurrentMetricData
                description: >-
                  <p>Gets the real-time metric data from the specified Amazon
                  Connect instance.</p> <p>For a description of each metric, see
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/real-time-metrics-definitions.html">Real-time
                  Metrics Definitions</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Get
                  - Current
                  - Metrics
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/userdata/{InstanceId}:
              POST:
                summary: GetCurrentUserData
                description: >-
                  <p>Gets the real-time active user data from the specified
                  Amazon Connect instance. </p>
                tags:
                  - Get
                  - Current
                  - Users
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /user/federate/{InstanceId}:
              GET:
                summary: GetFederationToken
                description: >-
                  <p>Supports SAML sign-in for Amazon Connect. Retrieves a token
                  for federation. The token is for the Amazon Connect user which
                  corresponds to the IAM credentials that were used to invoke
                  this action. </p> <p>For more information about how SAML
                  sign-in works in Amazon Connect, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/configure-saml.html
                  ">Configure SAML with IAM for Amazon Connect in the <i>Amazon
                  Connect Administrator Guide</i>.</a> </p> <note> <p>This API
                  doesn't support root users. If you try to invoke
                  GetFederationToken with root credentials, an error message
                  similar to the following one appears: </p> <p> <code>Provided
                  identity: Principal: .... User: .... cannot be used for
                  federation with Amazon Connect</code> </p> </note>
                tags:
                  - Get
                  - Federation
                  - Tokens
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/historical/{InstanceId}:
              POST:
                summary: GetMetricData
                description: >-
                  <p>Gets historical metric data from the specified Amazon
                  Connect instance.</p> <p>For a description of each historical
                  metric, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/historical-metrics-definitions.html">Historical
                  Metrics Definitions</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p> <note> <p>We recommend using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_GetMetricDataV2.html">GetMetricDataV2</a>
                  API. It provides more flexibility, features, and the ability
                  to query longer time ranges than <code>GetMetricData</code>.
                  Use it to retrieve historical agent and contact metrics for
                  the last 3 months, at varying intervals. You can also use it
                  to build custom dashboards to measure historical queue and
                  agent performance. For example, you can track the number of
                  incoming contacts for the last 7 days, with data split by day,
                  to see how contact volume changed per day of the week.</p>
                  </note>
                tags:
                  - Get
                  - Metrics
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
            /metrics/data:
              POST:
                summary: GetMetricDataV2
                description: >-
                  <p>Gets metric data from the specified Amazon Connect
                  instance. </p> <p> <code>GetMetricDataV2</code> offers more
                  features than <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_GetMetricData.html">GetMetricData</a>,
                  the previous version of this API. It has new metrics, offers
                  filtering at a metric level, and offers the ability to filter
                  and group data by channels, queues, routing profiles, agents,
                  and agent hierarchy levels. It can retrieve historical data
                  for the last 3 months, at varying intervals. </p> <p>For a
                  description of the historical metrics that are supported by
                  <code>GetMetricDataV2</code> and <code>GetMetricData</code>,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/historical-metrics-definitions.html">Historical
                  metrics definitions</a> in the <i>Amazon Connect
                  Administrator's Guide</i>.</p>
                tags:
                  - Get
                  - Metrics
                  - Data
                  - V2
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
            /prompts/{InstanceId}/{PromptId}/file:
              GET:
                summary: GetPromptFile
                description: <p>Gets the prompt file.</p>
                tags:
                  - Get
                  - Prompts
                  - File
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
            /traffic-distribution/{Id}:
              PUT:
                summary: UpdateTrafficDistribution
                description: >-
                  <p>Updates the traffic distribution for a given traffic
                  distribution group. </p> <note> <p>The
                  <code>SignInConfig</code> distribution is available only on a
                  default <code>TrafficDistributionGroup</code> (see the
                  <code>IsDefault</code> parameter in the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_TrafficDistributionGroup.html">TrafficDistributionGroup</a>
                  data type). If you call <code>UpdateTrafficDistribution</code>
                  with a modified <code>SignInConfig</code> and a non-default
                  <code>TrafficDistributionGroup</code>, an
                  <code>InvalidRequestException</code> is returned.</p> </note>
                  <p>For more information about updating a traffic distribution
                  group, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/update-telephony-traffic-distribution.html">Update
                  telephony traffic distribution across Amazon Web Services
                  Regions </a> in the <i>Amazon Connect Administrator Guide</i>.
                  </p>
                tags:
                  - Update
                  - Traffic
                  - Distributions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
            /phone-number/import:
              POST:
                summary: ImportPhoneNumber
                description: >-
                  <p>Imports a claimed phone number from an external service,
                  such as Amazon Pinpoint, into an Amazon Connect instance. You
                  can call this API only in the same Amazon Web Services Region
                  where the Amazon Connect instance was created.</p>
                tags:
                  - Import
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
            /instance/{InstanceId}/approved-origins:
              GET:
                summary: ListApprovedOrigins
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  approved origins associated with the instance.</p>
                tags:
                  - Lists
                  - Approved
                  - Origins
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
            /instance/{InstanceId}/bots:
              GET:
                summary: ListBots
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>For the specified version of Amazon
                  Lex, returns a paginated list of all the Amazon Lex bots
                  currently associated with the instance. Use this API to
                  returns both Amazon Lex V1 and V2 bots.</p>
                tags:
                  - Lists
                  - Bots
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact-evaluations/{InstanceId}:
              PUT:
                summary: StartContactEvaluation
                description: >-
                  <p>Starts an empty evaluation in the specified Amazon Connect
                  instance, using the given evaluation form for the particular
                  contact. The evaluation form version used for the contact
                  evaluation corresponds to the currently activated version. If
                  no version is activated for the evaluation form, the contact
                  evaluation cannot be started. </p> <note> <p>Evaluations
                  created through the public API do not contain answer values
                  suggested from automation.</p> </note>
                tags:
                  - Start
                  - Contacts
                  - Evaluations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact-flow-modules-summary/{InstanceId}:
              GET:
                summary: ListContactFlowModules
                description: >-
                  <p>Provides information about the flow modules for the
                  specified Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Contacts
                  - Flow
                  - Modules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact-flows-summary/{InstanceId}:
              GET:
                summary: ListContactFlows
                description: >-
                  <p>Provides information about the flows for the specified
                  Amazon Connect instance.</p> <p>You can also create and update
                  flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p> <p>For more information about
                  flows, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/concepts-contact-flows.html">Flows</a>
                  in the <i>Amazon Connect Administrator Guide</i>.</p>
                tags:
                  - Lists
                  - Contacts
                  - Flows
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /contact/references/{InstanceId}/{ContactId}:
              GET:
                summary: ListContactReferences
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>For the specified
                  <code>referenceTypes</code>, returns a list of references
                  associated with the contact. </p>
                tags:
                  - Lists
                  - Contacts
                  - References
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /default-vocabulary-summary/{InstanceId}:
              POST:
                summary: ListDefaultVocabularies
                description: >-
                  <p>Lists the default vocabularies for the specified Amazon
                  Connect instance.</p>
                tags:
                  - Lists
                  - Default
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /evaluation-forms/{InstanceId}/{EvaluationFormId}/versions:
              GET:
                summary: ListEvaluationFormVersions
                description: >-
                  <p>Lists versions of an evaluation form in the specified
                  Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Evaluations
                  - Forms
                  - Versions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /flow-associations-summary/{InstanceId}:
              GET:
                summary: ListFlowAssociations
                description: <p>List the flow association based on the filters.</p>
                tags:
                  - Lists
                  - Flow
                  - Associations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /hours-of-operations-summary/{InstanceId}:
              GET:
                summary: ListHoursOfOperations
                description: >-
                  <p>Provides information about the hours of operation for the
                  specified Amazon Connect instance.</p> <p>For more information
                  about hours of operation, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/set-hours-operation.html">Set
                  the Hours of Operation for a Queue</a> in the <i>Amazon
                  Connect Administrator Guide</i>.</p>
                tags:
                  - Lists
                  - Hours
                  - Of
                  - Operations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
            /instance/{InstanceId}/attributes:
              GET:
                summary: ListInstanceAttributes
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  attribute types for the given instance.</p>
                tags:
                  - Lists
                  - Instances
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
            /instance/{InstanceId}/storage-configs:
              GET:
                summary: ListInstanceStorageConfigs
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of storage
                  configs for the identified instance and resource type.</p>
                tags:
                  - Lists
                  - Instances
                  - Storage
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
            /instance/{InstanceId}/lambda-functions:
              GET:
                summary: ListLambdaFunctions
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  Lambda functions that display in the dropdown options in the
                  relevant flow blocks.</p>
                tags:
                  - Lists
                  - Lambda
                  - Functions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
            /instance/{InstanceId}/lex-bots:
              GET:
                summary: ListLexBots
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all the
                  Amazon Lex V1 bots currently associated with the instance. To
                  return both Amazon Lex V1 and V2 bots, use the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListBots.html">ListBots</a>
                  API. </p>
                tags:
                  - Lists
                  - Lex
                  - Bots
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
            /phone-numbers-summary/{InstanceId}:
              GET:
                summary: ListPhoneNumbers
                description: >-
                  <p>Provides information about the phone numbers for the
                  specified Amazon Connect instance. </p> <p>For more
                  information about phone numbers, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/contact-center-phone-number.html">Set
                  Up Phone Numbers for Your Contact Center</a> in the <i>Amazon
                  Connect Administrator Guide</i>.</p> <important> <ul> <li>
                  <p>We recommend using <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  to return phone number types. ListPhoneNumbers doesn't support
                  number types <code>UIFN</code>, <code>SHARED</code>,
                  <code>THIRD_PARTY_TF</code>, and <code>THIRD_PARTY_DID</code>.
                  While it returns numbers of those types, it incorrectly lists
                  them as <code>TOLL_FREE</code> or <code>DID</code>. </p> </li>
                  <li> <p>The phone number <code>Arn</code> value that is
                  returned from each of the items in the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbers.html#connect-ListPhoneNumbers-response-PhoneNumberSummaryList">PhoneNumberSummaryList</a>
                  cannot be used to tag phone number resources. It will fail
                  with a <code>ResourceNotFoundException</code>. Instead, use
                  the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  API. It returns the new phone number ARN that can be used to
                  tag phone number resources.</p> </li> </ul> </important>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
            /phone-number/list:
              POST:
                summary: ListPhoneNumbersV2
                description: >-
                  <p>Lists phone numbers claimed to your Amazon Connect instance
                  or traffic distribution group. If the provided
                  <code>TargetArn</code> is a traffic distribution group, you
                  can call this API in both Amazon Web Services Regions
                  associated with traffic distribution group.</p> <p>For more
                  information about phone numbers, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/contact-center-phone-number.html">Set
                  Up Phone Numbers for Your Contact Center</a> in the <i>Amazon
                  Connect Administrator Guide</i>.</p> <note> <ul> <li> <p>When
                  given an instance ARN, <code>ListPhoneNumbersV2</code> returns
                  only the phone numbers claimed to the instance.</p> </li> <li>
                  <p>When given a traffic distribution group ARN
                  <code>ListPhoneNumbersV2</code> returns only the phone numbers
                  claimed to the traffic distribution group.</p> </li> </ul>
                  </note>
                tags:
                  - Lists
                  - Phone
                  - Numbers
                  - V2
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /prompts-summary/{InstanceId}:
              GET:
                summary: ListPrompts
                description: >-
                  <p>Provides information about the prompts for the specified
                  Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /queues/{InstanceId}/{QueueId}/quick-connects:
              GET:
                summary: ListQueueQuickConnects
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Lists the quick connects associated
                  with a queue.</p>
                tags:
                  - Lists
                  - Queues
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /queues-summary/{InstanceId}:
              GET:
                summary: ListQueues
                description: >-
                  <p>Provides information about the queues for the specified
                  Amazon Connect instance.</p> <p>If you do not specify a
                  <code>QueueTypes</code> parameter, both standard and agent
                  queues are returned. This might cause an unexpected truncation
                  of results if you have more than 1000 agents and you limit the
                  number of results of the API call in code.</p> <p>For more
                  information about queues, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/concepts-queues-standard-and-agent.html">Queues:
                  Standard and Agent</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /contact/list-real-time-analysis-segments-v2/{InstanceId}/{ContactId}:
              POST:
                summary: ListRealtimeContactAnalysisSegmentsV2
                description: >-
                  <p>Provides a list of analysis segments for a real-time
                  analysis session. </p>
                tags:
                  - Lists
                  - Real Time
                  - Contacts
                  - Analysis
                  - Segments
                  - V2
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /routing-profiles/{InstanceId}/{RoutingProfileId}/queues:
              POST:
                summary: UpdateRoutingProfileQueues
                description: >-
                  <p>Updates the properties associated with a set of queues for
                  a routing profile.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /routing-profiles-summary/{InstanceId}:
              GET:
                summary: ListRoutingProfiles
                description: >-
                  <p>Provides summary information about the routing profiles for
                  the specified Amazon Connect instance.</p> <p>For more
                  information about routing profiles, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/concepts-routing.html">Routing
                  Profiles</a> and <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/routing-profiles.html">Create
                  a Routing Profile</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
            /instance/{InstanceId}/security-keys:
              GET:
                summary: ListSecurityKeys
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Returns a paginated list of all
                  security keys associated with the instance.</p>
                tags:
                  - Lists
                  - Security
                  - Keys
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /security-profiles-applications/{InstanceId}/{SecurityProfileId}:
              GET:
                summary: ListSecurityProfileApplications
                description: >-
                  <p>Returns a list of third-party applications in a specific
                  security profile.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Applications
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /security-profiles-permissions/{InstanceId}/{SecurityProfileId}:
              GET:
                summary: ListSecurityProfilePermissions
                description: <p>Lists the permissions granted to a security profile.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Permissions
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /security-profiles-summary/{InstanceId}:
              GET:
                summary: ListSecurityProfiles
                description: >-
                  <p>Provides summary information about the security profiles
                  for the specified Amazon Connect instance.</p> <p>For more
                  information about security profiles, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/connect-security-profiles.html">Security
                  Profiles</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes the specified tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
            /traffic-distribution-groups:
              GET:
                summary: ListTrafficDistributionGroups
                description: <p>Lists traffic distribution groups.</p>
                tags:
                  - Lists
                  - Traffic
                  - Distributions
                  - Groups
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /user-hierarchy-groups-summary/{InstanceId}:
              GET:
                summary: ListUserHierarchyGroups
                description: >-
                  <p>Provides summary information about the hierarchy groups for
                  the specified Amazon Connect instance.</p> <p>For more
                  information about agent hierarchies, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/agent-hierarchy.html">Set
                  Up Agent Hierarchies</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p>
                tags:
                  - Lists
                  - Users
                  - Hierarchy
                  - Groups
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /users/{InstanceId}/{UserId}/proficiencies:
              POST:
                summary: UpdateUserProficiencies
                description: >-
                  <p>Updates the properties associated with the proficiencies of
                  a user.</p>
                tags:
                  - Update
                  - Users
                  - Proficiencies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /users-summary/{InstanceId}:
              GET:
                summary: ListUsers
                description: >-
                  <p>Provides summary information about the users for the
                  specified Amazon Connect instance.</p>
                tags:
                  - Lists
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
            /contact/monitor:
              POST:
                summary: MonitorContact
                description: >-
                  <p>Initiates silent monitoring of a contact. The Contact
                  Control Panel (CCP) of the user specified by <i>userId</i>
                  will be set to silent monitoring mode on the contact.</p>
                tags:
                  - Monitors
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
            /contact/pause:
              POST:
                summary: PauseContact
                description: <p>Allows pausing an ongoing task contact.</p>
                tags:
                  - Pause
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
            /users/{InstanceId}/{UserId}/status:
              PUT:
                summary: PutUserStatus
                description: >-
                  <p>Changes the current status of a user or agent in Amazon
                  Connect. If the agent is currently handling a contact, this
                  sets the agent's next status.</p> <p>For more information, see
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/metrics-agent-status.html">Agent
                  status</a> and <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/set-next-status.html">Set
                  your next status</a> in the <i>Amazon Connect Administrator
                  Guide</i>.</p>
                tags:
                  - Put
                  - Users
                  - Status
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
            /instance/{InstanceId}/replicate:
              POST:
                summary: ReplicateInstance
                description: >-
                  <p>Replicates an Amazon Connect instance in the specified
                  Amazon Web Services Region and copies configuration
                  information for Amazon Connect resources across Amazon Web
                  Services Regions. </p> <p>For more information about
                  replicating an Amazon Connect instance, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/create-replica-connect-instance.html">Create
                  a replica of your existing Amazon Connect instance</a> in the
                  <i>Amazon Connect Administrator Guide</i>.</p>
                tags:
                  - Replicate
                  - Instances
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
            /contact/resume:
              POST:
                summary: ResumeContact
                description: <p>Allows resuming a task contact in a paused state.</p>
                tags:
                  - Resume
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
            /contact/resume-recording:
              POST:
                summary: ResumeContactRecording
                description: >-
                  <p>When a contact is being recorded, and the recording has
                  been suspended using SuspendContactRecording, this API resumes
                  recording whatever recording is selected in the flow
                  configuration: call, screen, or both. If only call recording
                  or only screen recording is enabled, then it would resume.</p>
                  <p>Voice and screen recordings are supported.</p>
                tags:
                  - Resume
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
            /phone-number/search-available:
              POST:
                summary: SearchAvailablePhoneNumbers
                description: >-
                  <p>Searches for available phone numbers that you can claim to
                  your Amazon Connect instance or traffic distribution group. If
                  the provided <code>TargetArn</code> is a traffic distribution
                  group, you can call this API in both Amazon Web Services
                  Regions associated with the traffic distribution group.</p>
                tags:
                  - Search
                  - Available
                  - Phone
                  - Numbers
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
            /search-contacts:
              POST:
                summary: SearchContacts
                description: <p>Searches contacts in an Amazon Connect instance.</p>
                tags:
                  - Search
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
            /search-hours-of-operations:
              POST:
                summary: SearchHoursOfOperations
                description: >-
                  <p>Searches the hours of operation in an Amazon Connect
                  instance, with optional filtering.</p>
                tags:
                  - Search
                  - Hours
                  - Of
                  - Operations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
            /search-predefined-attributes:
              POST:
                summary: SearchPredefinedAttributes
                description: <p>Predefined attributes that meet certain criteria.</p>
                tags:
                  - Search
                  - Predefined
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
            /search-prompts:
              POST:
                summary: SearchPrompts
                description: >-
                  <p>Searches prompts in an Amazon Connect instance, with
                  optional filtering.</p>
                tags:
                  - Search
                  - Prompts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
            /search-queues:
              POST:
                summary: SearchQueues
                description: >-
                  <p>Searches queues in an Amazon Connect instance, with
                  optional filtering.</p>
                tags:
                  - Search
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
            /search-quick-connects:
              POST:
                summary: SearchQuickConnects
                description: >-
                  <p>Searches quick connects in an Amazon Connect instance, with
                  optional filtering.</p>
                tags:
                  - Search
                  - Quick
                  - Connects
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
            /search-resource-tags:
              POST:
                summary: SearchResourceTags
                description: >-
                  <p>Searches tags used in an Amazon Connect instance using
                  optional search criteria.</p>
                tags:
                  - Search
                  - Resources
                  - Tags
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
            /search-routing-profiles:
              POST:
                summary: SearchRoutingProfiles
                description: >-
                  <p>Searches routing profiles in an Amazon Connect instance,
                  with optional filtering.</p>
                tags:
                  - Search
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
            /search-security-profiles:
              POST:
                summary: SearchSecurityProfiles
                description: >-
                  <p>Searches security profiles in an Amazon Connect instance,
                  with optional filtering.</p>
                tags:
                  - Search
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
            /search-users:
              POST:
                summary: SearchUsers
                description: >-
                  <p>Searches users in an Amazon Connect instance, with optional
                  filtering. </p> <note> <p>
                  <code>AfterContactWorkTimeLimit</code> is returned in
                  milliseconds. </p> </note>
                tags:
                  - Search
                  - Users
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
            /vocabulary-summary/{InstanceId}:
              POST:
                summary: SearchVocabularies
                description: >-
                  <p>Searches for vocabularies within a specific Amazon Connect
                  instance using <code>State</code>,
                  <code>NameStartsWith</code>, and
                  <code>LanguageCode</code>.</p>
                tags:
                  - Search
                  - Vocabularies
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
            /chat-integration-event:
              POST:
                summary: SendChatIntegrationEvent
                description: >-
                  <p>Processes chat integration events from Amazon Web Services
                  or external integrations to Amazon Connect. A chat integration
                  event includes:</p> <ul> <li> <p>SourceId, DestinationId, and
                  Subtype: a set of identifiers, uniquely representing a
                  chat</p> </li> <li> <p> ChatEvent: details of the chat action
                  to perform such as sending a message, event, or disconnecting
                  from a chat</p> </li> </ul> <p>When a chat integration event
                  is sent with chat identifiers that do not map to an active
                  chat contact, a new chat contact is also created before
                  handling chat action. </p> <p>Access to this API is currently
                  restricted to Amazon Pinpoint for supporting SMS integration.
                  </p>
                tags:
                  - Send
                  - Chat
                  - Integrations
                  - Events
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
            /contact/chat:
              PUT:
                summary: StartChatContact
                description: >-
                  <p>Initiates a flow to start a new chat for the customer.
                  Response of this API provides a token required to obtain
                  credentials from the <a
                  href="https://docs.aws.amazon.com/connect-participant/latest/APIReference/API_CreateParticipantConnection.html">CreateParticipantConnection</a>
                  API in the Amazon Connect Participant Service.</p> <p>When a
                  new chat contact is successfully created, clients must
                  subscribe to the participant’s connection for the created chat
                  within 5 minutes. This is achieved by invoking <a
                  href="https://docs.aws.amazon.com/connect-participant/latest/APIReference/API_CreateParticipantConnection.html">CreateParticipantConnection</a>
                  with WEBSOCKET and CONNECTION_CREDENTIALS. </p> <p>A 429 error
                  occurs in the following situations:</p> <ul> <li> <p>API rate
                  limit is exceeded. API TPS throttling returns a
                  <code>TooManyRequests</code> exception.</p> </li> <li> <p>The
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">quota
                  for concurrent active chats</a> is exceeded. Active chat
                  throttling returns a <code>LimitExceededException</code>.</p>
                  </li> </ul> <p>If you use the
                  <code>ChatDurationInMinutes</code> parameter and receive a 400
                  error, your account may not support the ability to configure
                  custom chat durations. For more information, contact Amazon
                  Web Services Support. </p> <p>For more information about chat,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat.html">Chat</a>
                  in the <i>Amazon Connect Administrator Guide</i>.</p>
                tags:
                  - Start
                  - Chat
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
            /contact/start-recording:
              POST:
                summary: StartContactRecording
                description: >-
                  <p>Starts recording the contact: </p> <ul> <li> <p>If the API
                  is called <i>before</i> the agent joins the call, recording
                  starts when the agent joins the call.</p> </li> <li> <p>If the
                  API is called <i>after</i> the agent joins the call, recording
                  starts at the time of the API call.</p> </li> </ul>
                  <p>StartContactRecording is a one-time action. For example, if
                  you use StopContactRecording to stop recording an ongoing
                  call, you can't use StartContactRecording to restart it. For
                  scenarios where the recording has started and you want to
                  suspend and resume it, such as when collecting sensitive
                  information (for example, a credit card number), use
                  SuspendContactRecording and ResumeContactRecording.</p> <p>You
                  can use this API to override the recording behavior configured
                  in the <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/set-recording-behavior.html">Set
                  recording behavior</a> block.</p> <p>Only voice recordings are
                  supported at this time.</p>
                tags:
                  - Start
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
            /contact/start-streaming:
              POST:
                summary: StartContactStreaming
                description: >-
                  <p> Initiates real-time message streaming for a new chat
                  contact.</p> <p> For more information about message streaming,
                  see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/chat-message-streaming.html">Enable
                  real-time chat message streaming</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p>
                tags:
                  - Start
                  - Contacts
                  - Streaming
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
            /contact/outbound-voice:
              PUT:
                summary: StartOutboundVoiceContact
                description: >-
                  <p>Places an outbound call to a contact, and then initiates
                  the flow. It performs the actions in the flow that's specified
                  (in <code>ContactFlowId</code>).</p> <p>Agents do not initiate
                  the outbound API, which means that they do not dial the
                  contact. If the flow places an outbound call to a contact, and
                  then puts the contact in queue, the call is then routed to the
                  agent, like any other inbound case.</p> <p>There is a
                  60-second dialing timeout for this operation. If the call is
                  not connected after 60 seconds, it fails.</p> <note> <p>UK
                  numbers with a 447 prefix are not allowed by default. Before
                  you can dial these UK mobile numbers, you must submit a
                  service quota increase request. For more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">Amazon
                  Connect Service Quotas</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p> </note> <note> <p>Campaign calls
                  are not allowed by default. Before you can make a call with
                  <code>TrafficType</code> = <code>CAMPAIGN</code>, you must
                  submit a service quota increase request to the quota <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html#outbound-communications-quotas">Amazon
                  Connect campaigns</a>. </p> </note>
                tags:
                  - Start
                  - Outbound
                  - Voice
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
            /contact/task:
              PUT:
                summary: StartTaskContact
                description: >-
                  <p>Initiates a flow to start a new task contact. For more
                  information about task contacts, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/tasks.html">Concepts:
                  Tasks in Amazon Connect</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p> <p>When using
                  <code>PreviousContactId</code> and
                  <code>RelatedContactId</code> input parameters, note the
                  following:</p> <ul> <li> <p> <code>PreviousContactId</code>
                  </p> <ul> <li> <p>Any updates to user-defined task contact
                  attributes on any contact linked through the same
                  <code>PreviousContactId</code> will affect every contact in
                  the chain.</p> </li> <li> <p>There can be a maximum of 12
                  linked task contacts in a chain. That is, 12 task contacts can
                  be created that share the same
                  <code>PreviousContactId</code>.</p> </li> </ul> </li> <li> <p>
                  <code>RelatedContactId</code> </p> <ul> <li> <p>Copies contact
                  attributes from the related task contact to the new
                  contact.</p> </li> <li> <p>Any update on attributes in a new
                  task contact does not update attributes on previous
                  contact.</p> </li> <li> <p>There’s no limit on the number of
                  task contacts that can be created that use the same
                  <code>RelatedContactId</code>.</p> </li> </ul> </li> </ul>
                  <p>In addition, when calling StartTaskContact include only one
                  of these parameters: <code>ContactFlowID</code>,
                  <code>QuickConnectID</code>, or <code>TaskTemplateID</code>.
                  Only one parameter is required as long as the task template
                  has a flow configured to run it. If more than one parameter is
                  specified, or only the <code>TaskTemplateID</code> is
                  specified but it does not have a flow configured, the request
                  returns an error because Amazon Connect cannot identify the
                  unique flow to run when the task is created.</p> <p>A
                  <code>ServiceQuotaExceededException</code> occurs when the
                  number of open tasks exceeds the active tasks quota or there
                  are already 12 tasks referencing the same
                  <code>PreviousContactId</code>. For more information about
                  service quotas for task contacts, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html">Amazon
                  Connect service quotas</a> in the <i>Amazon Connect
                  Administrator Guide</i>. </p>
                tags:
                  - Start
                  - Tasks
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
            /contact/webrtc:
              PUT:
                summary: StartWebRTCContact
                description: >-
                  <p>Places an inbound in-app, web, or video call to a contact,
                  and then initiates the flow. It performs the actions in the
                  flow that are specified (in ContactFlowId) and present in the
                  Amazon Connect instance (specified as InstanceId).</p>
                tags:
                  - Start
                  - Web
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
            /contact/stop:
              POST:
                summary: StopContact
                description: >-
                  <p>Ends the specified contact. This call does not work for
                  voice contacts that use the following initiation methods:</p>
                  <ul> <li> <p>DISCONNECT</p> </li> <li> <p>TRANSFER</p> </li>
                  <li> <p>QUEUE_TRANSFER</p> </li> </ul> <p>Chat and task
                  contacts, however, can be terminated in any state, regardless
                  of initiation method.</p>
                tags:
                  - Stop
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
            /contact/stop-recording:
              POST:
                summary: StopContactRecording
                description: >-
                  <p>Stops recording a call when a contact is being recorded.
                  StopContactRecording is a one-time action. If you use
                  StopContactRecording to stop recording an ongoing call, you
                  can't use StartContactRecording to restart it. For scenarios
                  where the recording has started and you want to suspend it for
                  sensitive information (for example, to collect a credit card
                  number), and then restart it, use SuspendContactRecording and
                  ResumeContactRecording.</p> <p>Only voice recordings are
                  supported at this time.</p>
                tags:
                  - Stop
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
            /contact/stop-streaming:
              POST:
                summary: StopContactStreaming
                description: >-
                  <p> Ends message streaming on a specified contact. To restart
                  message streaming on that contact, call the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_StartContactStreaming.html">StartContactStreaming</a>
                  API. </p>
                tags:
                  - Stop
                  - Contacts
                  - Streaming
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
            /contact-evaluations/{InstanceId}/{EvaluationId}/submit:
              POST:
                summary: SubmitContactEvaluation
                description: >-
                  <p>Submits a contact evaluation in the specified Amazon
                  Connect instance. Answers included in the request are merged
                  with existing answers for the given evaluation. If no answers
                  or notes are passed, the evaluation is submitted with the
                  existing answers and notes. You can delete an answer or note
                  by passing an empty object (<code>{}</code>) to the question
                  identifier. </p> <p>If a contact evaluation is already in
                  submitted state, this operation will trigger a
                  resubmission.</p>
                tags:
                  - Submit
                  - Contacts
                  - Evaluations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
            /contact/suspend-recording:
              POST:
                summary: SuspendContactRecording
                description: >-
                  <p>When a contact is being recorded, this API suspends
                  recording whatever is selected in the flow configuration:
                  call, screen, or both. If only call recording or only screen
                  recording is enabled, then it would be suspended. For example,
                  you might suspend the screen recording while collecting
                  sensitive information, such as a credit card number. Then use
                  ResumeContactRecording to restart recording the screen.</p>
                  <p>The period of time that the recording is suspended is
                  filled with silence in the final recording.</p> <p>Voice and
                  screen recordings are supported.</p>
                tags:
                  - Suspend
                  - Contacts
                  - Recording
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
            /contact/tags:
              POST:
                summary: TagContact
                description: >-
                  <p>Adds the specified tags to the contact resource. For more
                  information about this API is used, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/granular-billing.html">Set
                  up granular billing for a detailed view of your Amazon Connect
                  usage</a>. </p>
                tags:
                  - Tags
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
            /contact/transfer:
              POST:
                summary: TransferContact
                description: >-
                  <p>Transfers contacts from one agent or queue to another agent
                  or queue at any point after a contact is created. You can
                  transfer a contact to another queue by providing the flow
                  which orchestrates the contact to the destination queue. This
                  gives you more control over contact handling and helps you
                  adhere to the service level agreement (SLA) guaranteed to your
                  customers.</p> <p>Note the following requirements:</p> <ul>
                  <li> <p>Transfer is supported for only <code>TASK</code>
                  contacts.</p> </li> <li> <p>Do not use both
                  <code>QueueId</code> and <code>UserId</code> in the same
                  call.</p> </li> <li> <p>The following flow types are
                  supported: Inbound flow, Transfer to agent flow, and Transfer
                  to queue flow.</p> </li> <li> <p>The
                  <code>TransferContact</code> API can be called only on active
                  contacts.</p> </li> <li> <p>A contact cannot be transferred
                  more than 11 times.</p> </li> </ul>
                tags:
                  - Transfers
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
            /contact/tags/{InstanceId}/{ContactId}:
              DELETE:
                summary: UntagContact
                description: >-
                  <p>Removes the specified tags from the contact resource. For
                  more information about this API is used, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/granular-billing.html">Set
                  up granular billing for a detailed view of your Amazon Connect
                  usage</a>.</p>
                tags:
                  - Untag
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
            /contact/attributes:
              POST:
                summary: UpdateContactAttributes
                description: >-
                  <p>Creates or updates user-defined contact attributes
                  associated with the specified contact.</p> <p>You can create
                  or update user-defined attributes for both ongoing and
                  completed contacts. For example, while the call is active, you
                  can update the customer's name or the reason the customer
                  called. You can add notes about steps that the agent took
                  during the call that display to the next agent that takes the
                  call. You can also update attributes for a contact using data
                  from your CRM application and save the data with the contact
                  in Amazon Connect. You could also flag calls for additional
                  analysis, such as legal review or to identify abusive
                  callers.</p> <p>Contact attributes are available in Amazon
                  Connect for 24 months, and are then deleted. For information
                  about contact record retention and the maximum size of the
                  contact record attributes section, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/amazon-connect-service-limits.html#feature-limits">Feature
                  specifications</a> in the <i>Amazon Connect Administrator
                  Guide</i>. </p>
                tags:
                  - Update
                  - Contacts
                  - Attributes
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
            /contact-flows/{InstanceId}/{ContactFlowId}/content:
              POST:
                summary: UpdateContactFlowContent
                description: >-
                  <p>Updates the specified flow.</p> <p>You can also create and
                  update flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Content
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
            /contact-flows/{InstanceId}/{ContactFlowId}/metadata:
              POST:
                summary: UpdateContactFlowMetadata
                description: <p>Updates metadata about specified flow.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact-flow-modules/{InstanceId}/{ContactFlowModuleId}/content:
              POST:
                summary: UpdateContactFlowModuleContent
                description: >-
                  <p>Updates specified flow module for the specified Amazon
                  Connect instance. </p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Modules
                  - Content
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact-flow-modules/{InstanceId}/{ContactFlowModuleId}/metadata:
              POST:
                summary: UpdateContactFlowModuleMetadata
                description: <p>Updates metadata about specified flow module.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Modules
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact-flows/{InstanceId}/{ContactFlowId}/name:
              POST:
                summary: UpdateContactFlowName
                description: >-
                  <p>The name of the flow.</p> <p>You can also create and update
                  flows using the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/flow-language.html">Amazon
                  Connect Flow language</a>.</p>
                tags:
                  - Update
                  - Contacts
                  - Flow
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contacts/{InstanceId}/{ContactId}/routing-data:
              POST:
                summary: UpdateContactRoutingData
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates routing priority and age on
                  the contact (<b>QueuePriority</b> and
                  <b>QueueTimeAdjustmentInSeconds</b>). These properties can be
                  used to change a customer's position in the queue. For
                  example, you can move a contact to the back of the queue by
                  setting a lower routing priority relative to other contacts in
                  queue; or you can move a contact to the front of the queue by
                  increasing the routing age which will make the contact look
                  artificially older and therefore higher up in the
                  first-in-first-out routing order. Note that adjusting the
                  routing age of a contact affects only its position in queue,
                  and not its actual queue wait time as reported through
                  metrics. These properties can also be updated by using <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/change-routing-priority.html">the
                  Set routing priority / age flow block</a>.</p>
                tags:
                  - Update
                  - Contacts
                  - Routing
                  - Data
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
            /contact/schedule:
              POST:
                summary: UpdateContactSchedule
                description: >-
                  <p>Updates the scheduled time of a task contact that is
                  already scheduled.</p>
                tags:
                  - Update
                  - Contacts
                  - Schedules
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /contact/participant-role-config/{InstanceId}/{ContactId}:
              PUT:
                summary: UpdateParticipantRoleConfig
                description: >-
                  <p>Updates timeouts for when human chat participants are to be
                  considered idle, and when agents are automatically
                  disconnected from a chat due to idleness. You can set four
                  timers:</p> <ul> <li> <p>Customer idle timeout</p> </li> <li>
                  <p>Customer auto-disconnect timeout</p> </li> <li> <p>Agent
                  idle timeout</p> </li> <li> <p>Agent auto-disconnect
                  timeout</p> </li> </ul> <p>For more information about how chat
                  timeouts work, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/setup-chat-timeouts.html">Set
                  up chat timeouts for human participants</a>. </p>
                tags:
                  - Update
                  - Participants
                  - Roles
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /phone-number/{PhoneNumberId}/metadata:
              PUT:
                summary: UpdatePhoneNumberMetadata
                description: >-
                  <p>Updates a phone number’s metadata.</p> <important> <p>To
                  verify the status of a previous UpdatePhoneNumberMetadata
                  operation, call the <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_DescribePhoneNumber.html">DescribePhoneNumber</a>
                  API.</p> </important>
                tags:
                  - Update
                  - Phone
                  - Numbers
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /queues/{InstanceId}/{QueueId}/hours-of-operation:
              POST:
                summary: UpdateQueueHoursOfOperation
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the hours of operation for
                  the specified queue.</p>
                tags:
                  - Update
                  - Queues
                  - Hours
                  - Of
                  - Operation
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
            /queues/{InstanceId}/{QueueId}/max-contacts:
              POST:
                summary: UpdateQueueMaxContacts
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the maximum number of
                  contacts allowed in a queue before it is considered full.</p>
                tags:
                  - Update
                  - Queues
                  - Maximum
                  - Contacts
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
            /queues/{InstanceId}/{QueueId}/name:
              POST:
                summary: UpdateQueueName
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the name and description of
                  a queue. At least <code>Name</code> or
                  <code>Description</code> must be provided.</p>
                tags:
                  - Update
                  - Queues
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
            /queues/{InstanceId}/{QueueId}/outbound-caller-config:
              POST:
                summary: UpdateQueueOutboundCallerConfig
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the outbound caller ID name,
                  number, and outbound whisper flow for a specified queue.</p>
                  <important> <ul> <li> <p>If the phone number is claimed to a
                  traffic distribution group that was created in the same Region
                  as the Amazon Connect instance where you are calling this API,
                  then you can use a full phone number ARN or a UUID for
                  <code>OutboundCallerIdNumberId</code>. However, if the phone
                  number is claimed to a traffic distribution group that is in
                  one Region, and you are calling this API from an instance in
                  another Amazon Web Services Region that is associated with the
                  traffic distribution group, you must provide a full phone
                  number ARN. If a UUID is provided in this scenario, you will
                  receive a <code>ResourceNotFoundException</code>.</p> </li>
                  <li> <p>Only use the phone number ARN format that doesn't
                  contain <code>instance</code> in the path, for example,
                  <code>arn:aws:connect:us-east-1:1234567890:phone-number/uuid</code>.
                  This is the same ARN format that is returned when you call the
                  <a
                  href="https://docs.aws.amazon.com/connect/latest/APIReference/API_ListPhoneNumbersV2.html">ListPhoneNumbersV2</a>
                  API.</p> </li> <li> <p>If you plan to use IAM policies to
                  allow/deny access to this API for phone number resources
                  claimed to a traffic distribution group, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/security_iam_resource-level-policy-examples.html#allow-deny-queue-actions-replica-region">Allow
                  or Deny queue API actions for phone numbers in a replica
                  Region</a>.</p> </li> </ul> </important>
                tags:
                  - Update
                  - Queues
                  - Outbound
                  - Caller
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /queues/{InstanceId}/{QueueId}/status:
              POST:
                summary: UpdateQueueStatus
                description: >-
                  <p>This API is in preview release for Amazon Connect and is
                  subject to change.</p> <p>Updates the status of the queue.</p>
                tags:
                  - Update
                  - Queues
                  - Status
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /quick-connects/{InstanceId}/{QuickConnectId}/config:
              POST:
                summary: UpdateQuickConnectConfig
                description: >-
                  <p>Updates the configuration settings for the specified quick
                  connect.</p>
                tags:
                  - Update
                  - Quick
                  - Connect
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /quick-connects/{InstanceId}/{QuickConnectId}/name:
              POST:
                summary: UpdateQuickConnectName
                description: >-
                  <p>Updates the name and description of a quick connect. The
                  request accepts the following data in JSON format. At least
                  <code>Name</code> or <code>Description</code> must be
                  provided.</p>
                tags:
                  - Update
                  - Quick
                  - Connect
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
            /routing-profiles/{InstanceId}/{RoutingProfileId}/agent-availability-timer:
              POST:
                summary: UpdateRoutingProfileAgentAvailabilityTimer
                description: >-
                  <p>Whether agents with this routing profile will have their
                  routing order calculated based on <i>time since their last
                  inbound contact</i> or <i>longest idle time</i>. </p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Agent
                  - Availability
                  - Timer
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
            /routing-profiles/{InstanceId}/{RoutingProfileId}/concurrency:
              POST:
                summary: UpdateRoutingProfileConcurrency
                description: >-
                  <p>Updates the channels that agents can handle in the Contact
                  Control Panel (CCP) for a routing profile.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Concurrency
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
            /routing-profiles/{InstanceId}/{RoutingProfileId}/default-outbound-queue:
              POST:
                summary: UpdateRoutingProfileDefaultOutboundQueue
                description: >-
                  <p>Updates the default outbound queue of a routing
                  profile.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Default
                  - Outbound
                  - Queues
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /routing-profiles/{InstanceId}/{RoutingProfileId}/name:
              POST:
                summary: UpdateRoutingProfileName
                description: >-
                  <p>Updates the name and description of a routing profile. The
                  request accepts the following data in JSON format. At least
                  <code>Name</code> or <code>Description</code> must be
                  provided.</p>
                tags:
                  - Update
                  - Routing
                  - Profiles
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /users/{InstanceId}/{UserId}/hierarchy:
              POST:
                summary: UpdateUserHierarchy
                description: >-
                  <p>Assigns the specified hierarchy group to the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Hierarchy
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /user-hierarchy-groups/{InstanceId}/{HierarchyGroupId}/name:
              POST:
                summary: UpdateUserHierarchyGroupName
                description: <p>Updates the name of the user hierarchy group. </p>
                tags:
                  - Update
                  - Users
                  - Hierarchy
                  - Group
                  - Names
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
            /users/{InstanceId}/{UserId}/identity-info:
              POST:
                summary: UpdateUserIdentityInfo
                description: >-
                  <p>Updates the identity information for the specified
                  user.</p> <important> <p>We strongly recommend limiting who
                  has the ability to invoke <code>UpdateUserIdentityInfo</code>.
                  Someone with that ability can change the login credentials of
                  other users by changing their email address. This poses a
                  security risk to your organization. They can change the email
                  address of a user to the attacker's email address, and then
                  reset the password through email. For more information, see <a
                  href="https://docs.aws.amazon.com/connect/latest/adminguide/security-profile-best-practices.html">Best
                  Practices for Security Profiles</a> in the <i>Amazon Connect
                  Administrator Guide</i>.</p> </important>
                tags:
                  - Update
                  - Users
                  - Identity
                  - Info
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /users/{InstanceId}/{UserId}/phone-config:
              POST:
                summary: UpdateUserPhoneConfig
                description: >-
                  <p>Updates the phone configuration settings for the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Phone
                  - Configurations
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /users/{InstanceId}/{UserId}/routing-profile:
              POST:
                summary: UpdateUserRoutingProfile
                description: >-
                  <p>Assigns the specified routing profile to the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Routing
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /users/{InstanceId}/{UserId}/security-profiles:
              POST:
                summary: UpdateUserSecurityProfiles
                description: >-
                  <p>Assigns the specified security profiles to the specified
                  user.</p>
                tags:
                  - Update
                  - Users
                  - Security
                  - Profiles
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - Info
            /views/{InstanceId}/{ViewId}/metadata:
              POST:
                summary: UpdateViewMetadata
                description: >-
                  <p>Updates the view metadata. Note that either
                  <code>Name</code> or <code>Description</code> must be pro
                tags:
                  - Update
                  - View
                  - Metadata
                  - Instances
                  - Identifiers
                  - Evaluations
                  - Forms
                  - Activate
                  - Association
                  - Approved
                  - Origin
                  - Bot
                  - Languages
                  - Code
                  - Storage
                  - Configurations
                  - Lambda
                  - Functions
                  - Lex
                  - Phone
                  - Numbers
                  - Contacts
                  - Flow
                  - Queues
                  - Associate
                  - Quick
                  - Connects
                  - Routing
                  - Profiles
                  - Queues
                  - Security
                  - Keys
                  - Traffic
                  - Distributions
                  - Group
                  - Users
                  - Proficiencies
                  - Associations
                  - Claim
                  - Integrations
                  - Create
                  - Participants
                  - Initial
                  - Tasks
                  - Templates
                  - Use
                  - Cases
                  - View
                  - Versions
                  - Deactivate
                  - Modules
                  - Hours
                  - Of
                  - Operation
                  - Names
                  - Prompts
                  - Connect
                  - Rules
                  - Case
                  - Hierarchy
                  - Versions
                  - Vocabularies
                  - Agent
                  - Status
                  - Attributes
                  - Types
                  - Resources
                  - Disassociate
                  - Metrics
                  - Data
                  - File
                  - Import
                  - Origins
                  - Bots
                  - Attributes
                  - Configurations
                  - Functions
                  - Lists
                  - Keys
                  - ARN
                  - Groups
                  - Monitors
                  - Pause
                  - Replicate
                  - Resume
                  - Recording
                  - Search
                  - Available
                  - Contacts
                  - Operations
                  - Predefined
                  - Prompts
                  - Tags
                  - Profiles
                  - Users
                  - Chat
                  - Events
                  - Start
                  - Streaming
                  - Outbound
                  - Voice
                  - Web RTC
                  - Stop
                  - Submit
                  - Suspend
                  - Transfers
                  - Content
                  - Metadata
                  - Schedules
                  - Maximum
                  - Caller
                  - Availability
                  - Timer
                  - Concurrency
                  - Default
                  - Identity
                  - In
    overlays:
      - type: APIs.io Search
        url: overlays/connect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connect
  - name: lookoutmetrics
    description: >-
      <p>This is the <i>Amazon Lookout for Metrics API Reference</i>. For an
      introduction to the service with tutorials for getting started, visit <a
      href="https://docs.aws.amazon.com/lookoutmetrics/latest/dev">Amazon
      Lookout for Metrics Developer Guide</a>.</p>
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
            title: lookoutmetrics
          paths:
            /ActivateAnomalyDetector:
              POST:
                summary: ActivateAnomalyDetector
                description: <p>Activates an anomaly detector.</p>
                tags:
                  - Activate
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
            /BackTestAnomalyDetector:
              POST:
                summary: BackTestAnomalyDetector
                description: >-
                  <p>Runs a backtest for anomaly detection for the specified
                  resource.</p>
                tags:
                  - Back
                  - Tests
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
            /CreateAlert:
              POST:
                summary: CreateAlert
                description: <p>Creates an alert for an anomaly detector.</p>
                tags:
                  - Create
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
            /CreateAnomalyDetector:
              POST:
                summary: CreateAnomalyDetector
                description: <p>Creates an anomaly detector.</p>
                tags:
                  - Create
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
            /CreateMetricSet:
              POST:
                summary: CreateMetricSet
                description: <p>Creates a dataset.</p>
                tags:
                  - Create
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
            /DeactivateAnomalyDetector:
              POST:
                summary: DeactivateAnomalyDetector
                description: <p>Deactivates an anomaly detector.</p>
                tags:
                  - Deactivate
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
            /DeleteAlert:
              POST:
                summary: DeleteAlert
                description: <p>Deletes an alert.</p>
                tags:
                  - Delete
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
            /DeleteAnomalyDetector:
              POST:
                summary: DeleteAnomalyDetector
                description: >-
                  <p>Deletes a detector. Deleting an anomaly detector will
                  delete all of its corresponding resources including any
                  configured datasets and alerts.</p>
                tags:
                  - Delete
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
            /DescribeAlert:
              POST:
                summary: DescribeAlert
                description: >-
                  <p>Describes an alert.</p> <p>Amazon Lookout for Metrics API
                  actions are eventually consistent. If you do a read operation
                  on a resource immediately after creating or modifying it, use
                  retries to allow time for the write operation to complete.</p>
                tags:
                  - Describe
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
            /DescribeAnomalyDetectionExecutions:
              POST:
                summary: DescribeAnomalyDetectionExecutions
                description: >-
                  <p>Returns information about the status of the specified
                  anomaly detection jobs.</p>
                tags:
                  - Describe
                  - Anomaly
                  - Detections
                  - Executions
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
            /DescribeAnomalyDetector:
              POST:
                summary: DescribeAnomalyDetector
                description: >-
                  <p>Describes a detector.</p> <p>Amazon Lookout for Metrics API
                  actions are eventually consistent. If you do a read operation
                  on a resource immediately after creating or modifying it, use
                  retries to allow time for the write operation to complete.</p>
                tags:
                  - Describe
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
            /DescribeMetricSet:
              POST:
                summary: DescribeMetricSet
                description: >-
                  <p>Describes a dataset.</p> <p>Amazon Lookout for Metrics API
                  actions are eventually consistent. If you do a read operation
                  on a resource immediately after creating or modifying it, use
                  retries to allow time for the write operation to complete.</p>
                tags:
                  - Describe
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
            /DetectMetricSetConfig:
              POST:
                summary: DetectMetricSetConfig
                description: >-
                  <p>Detects an Amazon S3 dataset's file format, interval, and
                  offset.</p>
                tags:
                  - Detect
                  - Metrics
                  - Sets
                  - Configurations
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
            /GetAnomalyGroup:
              POST:
                summary: GetAnomalyGroup
                description: <p>Returns details about a group of anomalous metrics.</p>
                tags:
                  - Get
                  - Anomaly
                  - Group
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
            /GetDataQualityMetrics:
              POST:
                summary: GetDataQualityMetrics
                description: >-
                  <p>Returns details about the requested data quality
                  metrics.</p>
                tags:
                  - Get
                  - Data
                  - Quality
                  - Metrics
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
            /GetFeedback:
              POST:
                summary: GetFeedback
                description: <p>Get feedback for an anomaly group.</p>
                tags:
                  - Get
                  - Feedback
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
            /GetSampleData:
              POST:
                summary: GetSampleData
                description: >-
                  <p>Returns a selection of sample records from an Amazon S3
                  datasource.</p>
                tags:
                  - Get
                  - Samples
                  - Data
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
            /ListAlerts:
              POST:
                summary: ListAlerts
                description: >-
                  <p>Lists the alerts attached to a detector.</p> <p>Amazon
                  Lookout for Metrics API actions are eventually consistent. If
                  you do a read operation on a resource immediately after
                  creating or modifying it, use retries to allow time for the
                  write operation to complete.</p>
                tags:
                  - Lists
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
            /ListAnomalyDetectors:
              POST:
                summary: ListAnomalyDetectors
                description: >-
                  <p>Lists the detectors in the current AWS Region.</p>
                  <p>Amazon Lookout for Metrics API actions are eventually
                  consistent. If you do a read operation on a resource
                  immediately after creating or modifying it, use retries to
                  allow time for the write operation to complete.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
            /ListAnomalyGroupRelatedMetrics:
              POST:
                summary: ListAnomalyGroupRelatedMetrics
                description: >-
                  <p>Returns a list of measures that are potential causes or
                  effects of an anomaly group.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Group
                  - Related
                  - Metrics
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
            /ListAnomalyGroupSummaries:
              POST:
                summary: ListAnomalyGroupSummaries
                description: <p>Returns a list of anomaly groups.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Group
                  - Summaries
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
            /ListAnomalyGroupTimeSeries:
              POST:
                summary: ListAnomalyGroupTimeSeries
                description: >-
                  <p>Gets a list of anomalous metrics for a measure in an
                  anomaly group.</p>
                tags:
                  - Lists
                  - Anomaly
                  - Group
                  - Time
                  - Series
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
            /ListMetricSets:
              POST:
                summary: ListMetricSets
                description: >-
                  <p>Lists the datasets in the current AWS Region.</p> <p>Amazon
                  Lookout for Metrics API actions are eventually consistent. If
                  you do a read operation on a resource immediately after
                  creating or modifying it, use retries to allow time for the
                  write operation to complete.</p>
                tags:
                  - Lists
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes <a
                  href="https://docs.aws.amazon.com/lookoutmetrics/latest/dev/detectors-tags.html">tags</a>
                  from a detector, dataset, or alert.</p>
                tags:
                  - Untag
                  - Resources
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
            /PutFeedback:
              POST:
                summary: PutFeedback
                description: <p>Add feedback for an anomalous metric.</p>
                tags:
                  - Put
                  - Feedback
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
            /UpdateAlert:
              POST:
                summary: UpdateAlert
                description: <p>Make changes to an existing alert.</p>
                tags:
                  - Update
                  - Alerts
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
                  - Update
            /UpdateAnomalyDetector:
              POST:
                summary: UpdateAnomalyDetector
                description: >-
                  <p>Updates a detector. After activation, you can only change a
                  detector's ingestion delay and description.</p>
                tags:
                  - Update
                  - Anomaly
                  - Detectors
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
                  - Update
            /UpdateMetricSet:
              POST:
                summary: UpdateMetricSet
                description: <p>Updates a da
                tags:
                  - Update
                  - Metrics
                  - Sets
                  - Activate
                  - Anomaly
                  - Detectors
                  - Back
                  - Tests
                  - Create
                  - Alerts
                  - Metrics
                  - Sets
                  - Deactivate
                  - Delete
                  - Describe
                  - Detections
                  - Executions
                  - Detect
                  - Configurations
                  - Get
                  - Group
                  - Data
                  - Quality
                  - Metrics
                  - Feedback
                  - Samples
                  - Lists
                  - Alerts
                  - Detectors
                  - Related
                  - Summaries
                  - Time
                  - Series
                  - Sets
                  - ARN
                  - Put
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/lookoutmetrics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lookoutmetrics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lookoutmetrics
  - name: privatenetworks
    description: >-
      <p>Amazon Web Services Private 5G is a managed service that makes it easy
      to deploy, operate, and scale your own private mobile network at your
      on-premises location. Private 5G provides the pre-configured hardware and
      software for mobile networks, helps automate setup, and scales capacity on
      demand to support additional devices as needed.</p>
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
            title: privatenetworks
          paths:
            /v1/orders/acknowledge:
              POST:
                summary: AcknowledgeOrderReceipt
                description: >-
                  <p>Acknowledges that the specified network order was
                  received.</p>
                tags:
                  - Acknowledge
                  - Orders
                  - Receipts
                  - V1
                  - Orders
                  - Acknowledge
            /v1/device-identifiers/activate:
              POST:
                summary: ActivateDeviceIdentifier
                description: <p>Activates the specified device identifier.</p>
                tags:
                  - Activate
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
            /v1/network-sites/activate:
              POST:
                summary: ActivateNetworkSite
                description: <p>Activates the specified network site.</p>
                tags:
                  - Activate
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
            /v1/network-resources/configure:
              POST:
                summary: ConfigureAccessPoint
                description: >-
                  <p>Configures the specified network resource. </p> <p> Use
                  this action to specify the geographic position of the
                  hardware. You must provide Certified Professional Installer
                  (CPI) credentials in the request so that we can obtain
                  spectrum grants. For more information, see <a
                  href="https://docs.aws.amazon.com/private-networks/latest/userguide/radio-units.html">Radio
                  units</a> in the <i>Amazon Web Services Private 5G User
                  Guide</i>. </p>
                tags:
                  - Configure
                  - Access
                  - Points
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
            /v1/networks:
              POST:
                summary: CreateNetwork
                description: <p>Creates a network.</p>
                tags:
                  - Create
                  - Networks
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
            /v1/network-sites:
              POST:
                summary: CreateNetworkSite
                description: <p>Creates a network site.</p>
                tags:
                  - Create
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
            /v1/device-identifiers/deactivate:
              POST:
                summary: DeactivateDeviceIdentifier
                description: <p>Deactivates the specified device identifier.</p>
                tags:
                  - Deactivate
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
            /v1/networks/{networkArn}:
              GET:
                summary: GetNetwork
                description: <p>Gets the specified network.</p>
                tags:
                  - Get
                  - Networks
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
            /v1/network-sites/{networkSiteArn}:
              GET:
                summary: GetNetworkSite
                description: <p>Gets the specified network site.</p>
                tags:
                  - Get
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
            /v1/device-identifiers/{deviceIdentifierArn}:
              GET:
                summary: GetDeviceIdentifier
                description: <p>Gets the specified device identifier.</p>
                tags:
                  - Get
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
            /v1/network-resources/{networkResourceArn}:
              GET:
                summary: GetNetworkResource
                description: <p>Gets the specified network resource.</p>
                tags:
                  - Get
                  - Networks
                  - Resources
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
            /v1/orders/{orderArn}:
              GET:
                summary: GetOrder
                description: <p>Gets the specified order.</p>
                tags:
                  - Get
                  - Orders
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
            /v1/device-identifiers/list:
              POST:
                summary: ListDeviceIdentifiers
                description: >-
                  <p>Lists device identifiers. Add filters to your request to
                  return a more specific list of results. Use filters to match
                  the Amazon Resource Name (ARN) of an order, the status of
                  device identifiers, or the ARN of the traffic group.</p> <p>If
                  you specify multiple filters, filters are joined with an OR,
                  and the request returns results that match all of the
                  specified filters.</p>
                tags:
                  - Lists
                  - Device
                  - Identifiers
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/network-resources:
              POST:
                summary: ListNetworkResources
                description: >-
                  <p>Lists network resources. Add filters to your request to
                  return a more specific list of results. Use filters to match
                  the Amazon Resource Name (ARN) of an order or the status of
                  network resources.</p> <p>If you specify multiple filters,
                  filters are joined with an OR, and the request returns results
                  that match all of the specified filters.</p>
                tags:
                  - Lists
                  - Networks
                  - Resources
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/network-sites/list:
              POST:
                summary: ListNetworkSites
                description: >-
                  <p>Lists network sites. Add filters to your request to return
                  a more specific list of results. Use filters to match the
                  status of the network site.</p>
                tags:
                  - Lists
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/networks/list:
              POST:
                summary: ListNetworks
                description: >-
                  <p>Lists networks. Add filters to your request to return a
                  more specific list of results. Use filters to match the status
                  of the network.</p>
                tags:
                  - Lists
                  - Networks
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /v1/orders/list:
              POST:
                summary: ListOrders
                description: >-
                  <p>Lists orders. Add filters to your request to return a more
                  specific list of results. Use filters to match the Amazon
                  Resource Name (ARN) of the network site or the status of the
                  order.</p> <p>If you specify multiple filters, filters are
                  joined with an OR, and the request returns results that match
                  all of the specified filters.</p>
                tags:
                  - Lists
                  - Orders
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
            /ping:
              GET:
                summary: Ping
                description: <p>Checks the health of the service.</p>
                tags:
                  - Ping
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
            /v1/network-resources/update:
              POST:
                summary: StartNetworkResourceUpdate
                description: >-
                  <p>Use this action to do the following tasks:</p> <ul> <li>
                  <p>Update the duration and renewal status of the commitment
                  period for a radio unit. The update goes into effect
                  immediately.</p> </li> <li> <p>Request a replacement for a
                  network resource.</p> </li> <li> <p>Request that you return a
                  network resource.</p> </li> </ul> <p>After you submit a
                  request to replace or return a network resource, the status of
                  the network resource changes to
                  <code>CREATING_SHIPPING_LABEL</code>. The shipping label is
                  available when the status of the network resource is
                  <code>PENDING_RETURN</code>. After the network resource is
                  successfully returned, its status changes to
                  <code>DELETED</code>. For more information, see <a
                  href="https://docs.aws.amazon.com/private-networks/latest/userguide/radio-units.html#return-radio-unit">Return
                  a radio unit</a>.</p>
                tags:
                  - Start
                  - Networks
                  - Resources
                  - Update
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
                  - Update
            /v1/network-sites/site:
              PUT:
                summary: UpdateNetworkSite
                description: <p>Updates the specified network site.</p>
                tags:
                  - Update
                  - Networks
                  - Sites
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
                  - Update
            /v1/network-sites/plan:
              PUT:
                summary: UpdateNetworkSitePlan
                description: <p>Updates the specified network site
                tags:
                  - Update
                  - Networks
                  - Sites
                  - Plan
                  - V1
                  - Orders
                  - Acknowledge
                  - Device
                  - Identifiers
                  - Activate
                  - Networks
                  - Sites
                  - Resources
                  - Configure
                  - Networks
                  - Deactivate
                  - ARN
                  - Sites
                  - Identifiers
                  - Resources
                  - Lists
                  - Ping
                  - Update
                  - Pl
    overlays:
      - type: APIs.io Search
        url: overlays/privatenetworks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/privatenetworks-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:privatenetworks
  - name: route53
    description: "<p>Amazon Route\_53 is a highly available and scalable Domain Name System (DNS) web service.</p> <p>You can use Route\_53 to:</p> <ul> <li> <p>Register domain names.</p> <p>For more information, see <a href=\"https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-domain-registration.html\">How domain registration works</a>.</p> </li> <li> <p>Route internet traffic to the resources for your domain</p> <p>For more information, see <a href=\"https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-dns-service.html\">How internet traffic is routed to your website or web application</a>.</p> </li> <li> <p>Check the health of your resources.</p> <p>For more information, see <a href=\"https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/welcome-health-checks.html\">How Route\_53 checks the health of your resources</a>.</p> </li> </ul>"
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
            title: route53
          paths:
            /2013-04-01/keysigningkey/{HostedZoneId}/{Name}/activate:
              POST:
                summary: ActivateKeySigningKey
                description: >-
                  <p>Activates a key-signing key (KSK) so that it can be used
                  for signing by DNSSEC. This operation changes the KSK status
                  to <code>ACTIVE</code>.</p>
                tags:
                  - Activate
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
            /2013-04-01/hostedzone/{Id}/associatevpc:
              POST:
                summary: AssociateVPCWithHostedZone
                description: >-
                  <p>Associates an Amazon VPC with a private hosted zone. </p>
                  <important> <p>To perform the association, the VPC and the
                  private hosted zone must already exist. You can't convert a
                  public hosted zone into a private hosted zone.</p>
                  </important> <note> <p>If you want to associate a VPC that was
                  created by using one Amazon Web Services account with a
                  private hosted zone that was created by using a different
                  account, the Amazon Web Services account that created the
                  private hosted zone must first submit a
                  <code>CreateVPCAssociationAuthorization</code> request. Then
                  the account that created the VPC must submit an
                  <code>AssociateVPCWithHostedZone</code> request.</p> </note>
                  <note> <p>When granting access, the hosted zone and the Amazon
                  VPC must belong to the same partition. A partition is a group
                  of Amazon Web Services Regions. Each Amazon Web Services
                  account is scoped to one partition.</p> <p>The following are
                  the supported partitions:</p> <ul> <li> <p> <code>aws</code> -
                  Amazon Web Services Regions</p> </li> <li> <p>
                  <code>aws-cn</code> - China Regions</p> </li> <li> <p>
                  <code>aws-us-gov</code> - Amazon Web Services GovCloud (US)
                  Region</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Access
                  Management</a> in the <i>Amazon Web Services General
                  Reference</i>.</p> </note>
                tags:
                  - Associate
                  - With
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
            /2013-04-01/cidrcollection/{CidrCollectionId}:
              GET:
                summary: ListCidrLocations
                description: >-
                  <p>Returns a paginated list of CIDR locations for the given
                  collection (metadata only, does not include CIDR blocks).</p>
                tags:
                  - Lists
                  - CIDR
                  - Locations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
            /2013-04-01/hostedzone/{Id}/rrset/:
              POST:
                summary: ChangeResourceRecordSets
                description: >-
                  <p>Creates, changes, or deletes a resource record set, which
                  contains authoritative DNS information for a specified domain
                  name or subdomain name. For example, you can use
                  <code>ChangeResourceRecordSets</code> to create a resource
                  record set that routes traffic for test.example.com to a web
                  server that has an IP address of 192.0.2.44.</p> <p>
                  <b>Deleting Resource Record Sets</b> </p> <p>To delete a
                  resource record set, you must specify all the same values that
                  you specified when you created it.</p> <p> <b>Change Batches
                  and Transactional Changes</b> </p> <p>The request body must
                  include a document with a
                  <code>ChangeResourceRecordSetsRequest</code> element. The
                  request body contains a list of change items, known as a
                  change batch. Change batches are considered transactional
                  changes. Route 53 validates the changes in the request and
                  then either makes all or none of the changes in the change
                  batch request. This ensures that DNS routing isn't adversely
                  affected by partial changes to the resource record sets in a
                  hosted zone. </p> <p>For example, suppose a change batch
                  request contains two changes: it deletes the
                  <code>CNAME</code> resource record set for www.example.com and
                  creates an alias resource record set for www.example.com. If
                  validation for both records succeeds, Route 53 deletes the
                  first resource record set and creates the second resource
                  record set in a single operation. If validation for either the
                  <code>DELETE</code> or the <code>CREATE</code> action fails,
                  then the request is canceled, and the original
                  <code>CNAME</code> record continues to exist.</p> <note> <p>If
                  you try to delete the same resource record set more than once
                  in a single change batch, Route 53 returns an
                  <code>InvalidChangeBatch</code> error.</p> </note> <p>
                  <b>Traffic Flow</b> </p> <p>To create resource record sets for
                  complex routing configurations, use either the traffic flow
                  visual editor in the Route 53 console or the API actions for
                  traffic policies and traffic policy instances. Save the
                  configuration as a traffic policy, then associate the traffic
                  policy with one or more domain names (such as example.com) or
                  subdomain names (such as www.example.com), in the same hosted
                  zone or in multiple hosted zones. You can roll back the
                  updates if the new configuration isn't performing as expected.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/traffic-flow.html">Using
                  Traffic Flow to Route DNS Traffic</a> in the <i>Amazon Route
                  53 Developer Guide</i>.</p> <p> <b>Create, Delete, and
                  Upsert</b> </p> <p>Use
                  <code>ChangeResourceRecordsSetsRequest</code> to perform the
                  following actions:</p> <ul> <li> <p> <code>CREATE</code>:
                  Creates a resource record set that has the specified
                  values.</p> </li> <li> <p> <code>DELETE</code>: Deletes an
                  existing resource record set that has the specified
                  values.</p> </li> <li> <p> <code>UPSERT</code>: If a resource
                  set doesn't exist, Route 53 creates it. If a resource set
                  exists Route 53 updates it with the values in the request.
                  </p> </li> </ul> <p> <b>Syntaxes for Creating, Updating, and
                  Deleting Resource Record Sets</b> </p> <p>The syntax for a
                  request depends on the type of resource record set that you
                  want to create, delete, or update, such as weighted, alias, or
                  failover. The XML elements in your request must appear in the
                  order listed in the syntax. </p> <p>For an example for each
                  type of resource record set, see "Examples."</p> <p>Don't
                  refer to the syntax in the "Parameter Syntax" section, which
                  includes all of the elements for every kind of resource record
                  set that you can create, delete, or update by using
                  <code>ChangeResourceRecordSets</code>. </p> <p> <b>Change
                  Propagation to Route 53 DNS Servers</b> </p> <p>When you
                  submit a <code>ChangeResourceRecordSets</code> request, Route
                  53 propagates your changes to all of the Route 53
                  authoritative DNS servers managing the hosted zone. While your
                  changes are propagating, <code>GetChange</code> returns a
                  status of <code>PENDING</code>. When propagation is complete,
                  <code>GetChange</code> returns a status of
                  <code>INSYNC</code>. Changes generally propagate to all Route
                  53 name servers managing the hosted zone within 60 seconds.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_GetChange.html">GetChange</a>.</p>
                  <p> <b>Limits on ChangeResourceRecordSets Requests</b> </p>
                  <p>For information about the limits on a
                  <code>ChangeResourceRecordSets</code> request, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>.</p>
                tags:
                  - Change
                  - Resources
                  - Record
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
            /2013-04-01/tags/{ResourceType}/{ResourceId}:
              GET:
                summary: ListTagsForResource
                description: >-
                  <p>Lists tags for one health check or hosted zone. </p> <p>For
                  information about using tags for cost allocation, see <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Using
                  Cost Allocation Tags</a> in the <i>Billing and Cost Management
                  User Guide</i>.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
            /2013-04-01/cidrcollection:
              GET:
                summary: ListCidrCollections
                description: >-
                  <p>Returns a paginated list of CIDR collections in the Amazon
                  Web Services account (metadata only).</p>
                tags:
                  - Lists
                  - CIDR
                  - Collections
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
            /2013-04-01/healthcheck:
              GET:
                summary: ListHealthChecks
                description: >-
                  <p>Retrieve a list of the health checks that are associated
                  with the current Amazon Web Services account. </p>
                tags:
                  - Lists
                  - Health
                  - Checks
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
            /2013-04-01/hostedzone:
              GET:
                summary: ListHostedZones
                description: >-
                  <p>Retrieves a list of the public and private hosted zones
                  that are associated with the current Amazon Web Services
                  account. The response includes a <code>HostedZones</code>
                  child element for each hosted zone.</p> <p>Amazon Route 53
                  returns a maximum of 100 items in each response. If you have a
                  lot of hosted zones, you can use the <code>maxitems</code>
                  parameter to list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
            /2013-04-01/keysigningkey:
              POST:
                summary: CreateKeySigningKey
                description: >-
                  <p>Creates a new key-signing key (KSK) associated with a
                  hosted zone. You can only have two KSKs per hosted zone.</p>
                tags:
                  - Create
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
            /2013-04-01/queryloggingconfig:
              GET:
                summary: ListQueryLoggingConfigs
                description: >-
                  <p>Lists the configurations for DNS query logging that are
                  associated with the current Amazon Web Services account or the
                  configuration that is associated with a specified hosted
                  zone.</p> <p>For more information about DNS query logs, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateQueryLoggingConfig.html">CreateQueryLoggingConfig</a>.
                  Additional information, including the format of DNS query
                  logs, appears in <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/query-logs.html">Logging
                  DNS Queries</a> in the <i>Amazon Route 53 Developer
                  Guide</i>.</p>
                tags:
                  - Lists
                  - Queries
                  - Logging
                  - Configurations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
            /2013-04-01/delegationset:
              GET:
                summary: ListReusableDelegationSets
                description: >-
                  <p>Retrieves a list of the reusable delegation sets that are
                  associated with the current Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Reusable
                  - Delegation
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
            /2013-04-01/trafficpolicy:
              POST:
                summary: CreateTrafficPolicy
                description: >-
                  <p>Creates a traffic policy, which you use to create multiple
                  DNS resource record sets for one domain name (such as
                  example.com) or one subdomain name (such as
                  www.example.com).</p>
                tags:
                  - Create
                  - Traffic
                  - Policies
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
            /2013-04-01/trafficpolicyinstance:
              POST:
                summary: CreateTrafficPolicyInstance
                description: >-
                  <p>Creates resource record sets in a specified hosted zone
                  based on the settings in a specified traffic policy version.
                  In addition, <code>CreateTrafficPolicyInstance</code>
                  associates the resource record sets with a specified domain
                  name (such as example.com) or subdomain name (such as
                  www.example.com). Amazon Route 53 responds to DNS queries for
                  the domain or subdomain name by using the resource record sets
                  that <code>CreateTrafficPolicyInstance</code> created.</p>
                  <note> <p>After you submit an
                  <code>CreateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. Use
                  <code>GetTrafficPolicyInstance</code> with the <code>id</code>
                  of new traffic policy instance to confirm that the
                  <code>CreateTrafficPolicyInstance</code> request completed
                  successfully. For more information, see the <code>State</code>
                  response element.</p> </note>
                tags:
                  - Create
                  - Traffic
                  - Policies
                  - Instances
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicy/{Id}:
              POST:
                summary: CreateTrafficPolicyVersion
                description: >-
                  <p>Creates a new version of an existing traffic policy. When
                  you create a new version of a traffic policy, you specify the
                  ID of the traffic policy that you want to update and a
                  JSON-formatted document that describes the new version. You
                  use traffic policies to create multiple DNS resource record
                  sets for one domain name (such as example.com) or one
                  subdomain name (such as www.example.com). You can create a
                  maximum of 1000 versions of a traffic policy. If you reach the
                  limit and need to create another version, you'll need to start
                  a new traffic policy.</p>
                tags:
                  - Create
                  - Traffic
                  - Policies
                  - Versions
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/hostedzone/{Id}/authorizevpcassociation:
              GET:
                summary: ListVPCAssociationAuthorizations
                description: >-
                  <p>Gets a list of the VPCs that were created by other accounts
                  and that can be associated with a specified hosted zone
                  because you've submitted one or more
                  <code>CreateVPCAssociationAuthorization</code> requests. </p>
                  <p>The response includes a <code>VPCs</code> element with a
                  <code>VPC</code> child element for each VPC that can be
                  associated with the hosted zone.</p>
                tags:
                  - Lists
                  - Association
                  - Authorization
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
            /2013-04-01/keysigningkey/{HostedZoneId}/{Name}/deactivate:
              POST:
                summary: DeactivateKeySigningKey
                description: >-
                  <p>Deactivates a key-signing key (KSK) so that it will not be
                  used for signing by DNSSEC. This operation changes the KSK
                  status to <code>INACTIVE</code>.</p>
                tags:
                  - Deactivate
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
            /2013-04-01/healthcheck/{HealthCheckId}:
              POST:
                summary: UpdateHealthCheck
                description: >-
                  <p>Updates an existing health check. Note that some values
                  can't be updated. </p> <p>For more information about updating
                  health checks, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/health-checks-creating-deleting.html">Creating,
                  Updating, and Deleting Health Checks</a> in the <i>Amazon
                  Route 53 Developer Guide</i>.</p>
                tags:
                  - Update
                  - Health
                  - Checks
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/hostedzone/{Id}:
              POST:
                summary: UpdateHostedZoneComment
                description: <p>Updates the comment for a specified hosted zone.</p>
                tags:
                  - Update
                  - Hosted
                  - Zones
                  - Comments
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/keysigningkey/{HostedZoneId}/{Name}:
              DELETE:
                summary: DeleteKeySigningKey
                description: >-
                  <p>Deletes a key-signing key (KSK). Before you can delete a
                  KSK, you must deactivate it. The KSK must be deactivated
                  before you can delete it regardless of whether the hosted zone
                  is enabled for DNSSEC signing.</p> <p>You can use <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_DeactivateKeySigningKey.html">DeactivateKeySigningKey</a>
                  to deactivate the key before you delete it.</p> <p>Use <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_GetDNSSEC.html">GetDNSSEC</a>
                  to verify that the KSK is in an <code>INACTIVE</code>
                  status.</p>
                tags:
                  - Delete
                  - Keys
                  - Signing
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/queryloggingconfig/{Id}:
              GET:
                summary: GetQueryLoggingConfig
                description: >-
                  <p>Gets information about a specified configuration for DNS
                  query logging.</p> <p>For more information about DNS query
                  logs, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateQueryLoggingConfig.html">CreateQueryLoggingConfig</a>
                  and <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/query-logs.html">Logging
                  DNS Queries</a>.</p>
                tags:
                  - Get
                  - Queries
                  - Logging
                  - Configurations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/delegationset/{Id}:
              GET:
                summary: GetReusableDelegationSet
                description: >-
                  <p>Retrieves information about a specified reusable delegation
                  set, including the four name servers that are assigned to the
                  delegation set.</p>
                tags:
                  - Get
                  - Reusable
                  - Delegation
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
            /2013-04-01/trafficpolicy/{Id}/{Version}:
              POST:
                summary: UpdateTrafficPolicyComment
                description: >-
                  <p>Updates the comment for a specified traffic policy
                  version.</p>
                tags:
                  - Update
                  - Traffic
                  - Policies
                  - Comments
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
            /2013-04-01/trafficpolicyinstance/{Id}:
              POST:
                summary: UpdateTrafficPolicyInstance
                description: "<note> <p>After you submit a <code>UpdateTrafficPolicyInstance</code> request, there's a brief delay while Route\_53 creates the resource record sets that are specified in the traffic policy definition. Use <code>GetTrafficPolicyInstance</code> with the <code>id</code> of updated traffic policy instance confirm that the <code>UpdateTrafficPolicyInstance</code> request completed successfully. For more information, see the <code>State</code> response element.</p> </note> <p>Updates the resource record sets in a specified hosted zone that were created based on the settings in a specified traffic policy version.</p> <p>When you update a traffic policy instance, Amazon Route 53 continues to respond to DNS queries for the root resource record set name (such as example.com) while it replaces one group of resource record sets with another. Route 53 performs the following operations:</p> <ol> <li> <p>Route 53 creates a new group of resource record sets based on the specified traffic policy. This is true regardless of how significant the differences are between the existing resource record sets and the new resource record sets. </p> </li> <li> <p>When all of the new resource record sets have been created, Route 53 starts to respond to DNS queries for the root resource record set name (such as example.com) by using the new resource record sets.</p> </li> <li> <p>Route 53 deletes the old group of resource record sets that are associated with the root resource record set name.</p> </li> </ol>"
                tags:
                  - Update
                  - Traffic
                  - Policies
                  - Instances
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
            /2013-04-01/hostedzone/{Id}/deauthorizevpcassociation:
              POST:
                summary: DeleteVPCAssociationAuthorization
                description: >-
                  <p>Removes authorization to submit an
                  <code>AssociateVPCWithHostedZone</code> request to associate a
                  specified VPC with a hosted zone that was created by a
                  different account. You must use the account that created the
                  hosted zone to submit a
                  <code>DeleteVPCAssociationAuthorization</code> request.</p>
                  <important> <p>Sending this request only prevents the Amazon
                  Web Services account that created the VPC from associating the
                  VPC with the Amazon Route 53 hosted zone in the future. If the
                  VPC is already associated with the hosted zone,
                  <code>DeleteVPCAssociationAuthorization</code> won't
                  disassociate the VPC from the hosted zone. If you want to
                  delete an existing association, use
                  <code>DisassociateVPCFromHostedZone</code>.</p> </important>
                tags:
                  - Delete
                  - Association
                  - Authorization
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
            /2013-04-01/hostedzone/{Id}/disable-dnssec:
              POST:
                summary: DisableHostedZoneDNSSEC
                description: >-
                  <p>Disables DNSSEC signing in a specific hosted zone. This
                  action does not deactivate any key-signing keys (KSKs) that
                  are active in the hosted zone.</p>
                tags:
                  - Disable
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
            /2013-04-01/hostedzone/{Id}/disassociatevpc:
              POST:
                summary: DisassociateVPCFromHostedZone
                description: >-
                  <p>Disassociates an Amazon Virtual Private Cloud (Amazon VPC)
                  from an Amazon Route 53 private hosted zone. Note the
                  following:</p> <ul> <li> <p>You can't disassociate the last
                  Amazon VPC from a private hosted zone.</p> </li> <li> <p>You
                  can't convert a private hosted zone into a public hosted
                  zone.</p> </li> <li> <p>You can submit a
                  <code>DisassociateVPCFromHostedZone</code> request using
                  either the account that created the hosted zone or the account
                  that created the Amazon VPC.</p> </li> <li> <p>Some services,
                  such as Cloud Map and Amazon Elastic File System (Amazon EFS)
                  automatically create hosted zones and associate VPCs with the
                  hosted zones. A service can create a hosted zone using your
                  account or using its own account. You can disassociate a VPC
                  from a hosted zone only if the service created the hosted zone
                  using your account.</p> <p>When you run <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_ListHostedZonesByVPC.html">DisassociateVPCFromHostedZone</a>,
                  if the hosted zone has a value for <code>OwningAccount</code>,
                  you can use <code>DisassociateVPCFromHostedZone</code>. If the
                  hosted zone has a value for <code>OwningService</code>, you
                  can't use <code>DisassociateVPCFromHostedZone</code>.</p>
                  </li> </ul> <note> <p>When revoking access, the hosted zone
                  and the Amazon VPC must belong to the same partition. A
                  partition is a group of Amazon Web Services Regions. Each
                  Amazon Web Services account is scoped to one partition.</p>
                  <p>The following are the supported partitions:</p> <ul> <li>
                  <p> <code>aws</code> - Amazon Web Services Regions</p> </li>
                  <li> <p> <code>aws-cn</code> - China Regions</p> </li> <li>
                  <p> <code>aws-us-gov</code> - Amazon Web Services GovCloud
                  (US) Region</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Access
                  Management</a> in the <i>Amazon Web Services General
                  Reference</i>.</p> </note>
                tags:
                  - Disassociate
                  - From
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
            /2013-04-01/hostedzone/{Id}/enable-dnssec:
              POST:
                summary: EnableHostedZoneDNSSEC
                description: <p>Enables DNSSEC signing in a specific hosted zone.</p>
                tags:
                  - Enable
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
            /2013-04-01/accountlimit/{Type}:
              GET:
                summary: GetAccountLimit
                description: >-
                  <p>Gets the specified limit for the current account, for
                  example, the maximum number of health checks that you can
                  create using the account.</p> <p>For the default limit, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>. To request a
                  higher limit, <a
                  href="https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&amp;limitType=service-code-route53">open
                  a case</a>.</p> <note> <p>You can also view account limits in
                  Amazon Web Services Trusted Advisor. Sign in to the Amazon Web
                  Services Management Console and open the Trusted Advisor
                  console at <a
                  href="https://console.aws.amazon.com/trustedadvisor">https://console.aws.amazon.com/trustedadvisor/</a>.
                  Then choose <b>Service limits</b> in the navigation pane.</p>
                  </note>
                tags:
                  - Get
                  - Account
                  - Limits
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
            /2013-04-01/change/{Id}:
              GET:
                summary: GetChange
                description: >-
                  <p>Returns the current status of a change batch request. The
                  status is one of the following values:</p> <ul> <li> <p>
                  <code>PENDING</code> indicates that the changes in this
                  request have not propagated to all Amazon Route 53 DNS servers
                  managing the hosted zone. This is the initial status of all
                  change batch requests.</p> </li> <li> <p> <code>INSYNC</code>
                  indicates that the changes have propagated to all Route 53 DNS
                  servers managing the hosted zone. </p> </li> </ul>
                tags:
                  - Get
                  - Change
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
            /2013-04-01/checkeripranges:
              GET:
                summary: GetCheckerIpRanges
                description: >-
                  <p>Route 53 does not perform authorization for this API
                  because it retrieves information that is already available to
                  the public.</p> <important> <p>
                  <code>GetCheckerIpRanges</code> still works, but we recommend
                  that you download ip-ranges.json, which includes IP address
                  ranges for all Amazon Web Services services. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/route-53-ip-addresses.html">IP
                  Address Ranges of Amazon Route 53 Servers</a> in the <i>Amazon
                  Route 53 Developer Guide</i>.</p> </important>
                tags:
                  - Get
                  - Checker
                  - IP
                  - Ranges
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
            /2013-04-01/hostedzone/{Id}/dnssec:
              GET:
                summary: GetDNSSEC
                description: >-
                  <p>Returns information about DNSSEC for a specific hosted
                  zone, including the key-signing keys (KSKs) in the hosted
                  zone.</p>
                tags:
                  - Get
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
            /2013-04-01/geolocation:
              GET:
                summary: GetGeoLocation
                description: >-
                  <p>Gets information about whether a specified geographic
                  location is supported for Amazon Route 53 geolocation resource
                  record sets.</p> <p>Route 53 does not perform authorization
                  for this API because it retrieves information that is already
                  available to the public.</p> <p>Use the following syntax to
                  determine whether a continent is supported for
                  geolocation:</p> <p> <code>GET
                  /2013-04-01/geolocation?continentcode=<i>two-letter
                  abbreviation for a continent</i> </code> </p> <p>Use the
                  following syntax to determine whether a country is supported
                  for geolocation:</p> <p> <code>GET
                  /2013-04-01/geolocation?countrycode=<i>two-character country
                  code</i> </code> </p> <p>Use the following syntax to determine
                  whether a subdivision of a country is supported for
                  geolocation:</p> <p> <code>GET
                  /2013-04-01/geolocation?countrycode=<i>two-character country
                  code</i>&amp;subdivisioncode=<i>subdivision code</i> </code>
                  </p>
                tags:
                  - Get
                  - Geo
                  - Locations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
            /2013-04-01/healthcheckcount:
              GET:
                summary: GetHealthCheckCount
                description: >-
                  <p>Retrieves the number of health checks that are associated
                  with the current Amazon Web Services account.</p>
                tags:
                  - Get
                  - Health
                  - Checks
                  - Count
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
            /2013-04-01/healthcheck/{HealthCheckId}/lastfailurereason:
              GET:
                summary: GetHealthCheckLastFailureReason
                description: >-
                  <p>Gets the reason that a specified health check failed most
                  recently.</p>
                tags:
                  - Get
                  - Health
                  - Checks
                  - Last
                  - Failure
                  - Reasons
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
            /2013-04-01/healthcheck/{HealthCheckId}/status:
              GET:
                summary: GetHealthCheckStatus
                description: >-
                  <p>Gets status of a specified health check. </p> <important>
                  <p>This API is intended for use during development to diagnose
                  behavior. It doesn’t support production use-cases with high
                  query rates that require immediate and actionable
                  responses.</p> </important>
                tags:
                  - Get
                  - Health
                  - Checks
                  - Status
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
            /2013-04-01/hostedzonecount:
              GET:
                summary: GetHostedZoneCount
                description: >-
                  <p>Retrieves the number of hosted zones that are associated
                  with the current Amazon Web Services account.</p>
                tags:
                  - Get
                  - Hosted
                  - Zones
                  - Count
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
            /2013-04-01/hostedzonelimit/{Id}/{Type}:
              GET:
                summary: GetHostedZoneLimit
                description: >-
                  <p>Gets the specified limit for a specified hosted zone, for
                  example, the maximum number of records that you can create in
                  the hosted zone. </p> <p>For the default limit, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>. To request a
                  higher limit, <a
                  href="https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&amp;limitType=service-code-route53">open
                  a case</a>.</p>
                tags:
                  - Get
                  - Hosted
                  - Zones
                  - Limits
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
            /2013-04-01/reusabledelegationsetlimit/{Id}/{Type}:
              GET:
                summary: GetReusableDelegationSetLimit
                description: >-
                  <p>Gets the maximum number of hosted zones that you can
                  associate with the specified reusable delegation set.</p>
                  <p>For the default limit, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DNSLimitations.html">Limits</a>
                  in the <i>Amazon Route 53 Developer Guide</i>. To request a
                  higher limit, <a
                  href="https://console.aws.amazon.com/support/home#/case/create?issueType=service-limit-increase&amp;limitType=service-code-route53">open
                  a case</a>.</p>
                tags:
                  - Get
                  - Reusable
                  - Delegation
                  - Sets
                  - Limits
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
            /2013-04-01/trafficpolicyinstancecount:
              GET:
                summary: GetTrafficPolicyInstanceCount
                description: >-
                  <p>Gets the number of traffic policy instances that are
                  associated with the current Amazon Web Services account.</p>
                tags:
                  - Get
                  - Traffic
                  - Policies
                  - Instances
                  - Count
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
            /2013-04-01/cidrcollection/{CidrCollectionId}/cidrblocks:
              GET:
                summary: ListCidrBlocks
                description: >-
                  <p>Returns a paginated list of location objects and their CIDR
                  blocks.</p>
                tags:
                  - Lists
                  - CIDR
                  - Blocks
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
            /2013-04-01/geolocations:
              GET:
                summary: ListGeoLocations
                description: >-
                  <p>Retrieves a list of supported geographic locations.</p>
                  <p>Countries are listed first, and continents are listed last.
                  If Amazon Route 53 supports subdivisions for a country (for
                  example, states or provinces), the subdivisions for that
                  country are listed in alphabetical order immediately after the
                  corresponding country.</p> <p>Route 53 does not perform
                  authorization for this API because it retrieves information
                  that is already available to the public.</p> <p>For a list of
                  supported geolocation codes, see the <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html">GeoLocation</a>
                  data type.</p>
                tags:
                  - Lists
                  - Geo
                  - Locations
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
            /2013-04-01/hostedzonesbyname:
              GET:
                summary: ListHostedZonesByName
                description: >-
                  <p>Retrieves a list of your hosted zones in lexicographic
                  order. The response includes a <code>HostedZones</code> child
                  element for each hosted zone created by the current Amazon Web
                  Services account. </p> <p> <code>ListHostedZonesByName</code>
                  sorts hosted zones by name with the labels reversed. For
                  example:</p> <p> <code>com.example.www.</code> </p> <p>Note
                  the trailing dot, which can change the sort order in some
                  circumstances.</p> <p>If the domain name includes escape
                  characters or Punycode, <code>ListHostedZonesByName</code>
                  alphabetizes the domain name using the escaped or Punycoded
                  value, which is the format that Amazon Route 53 saves in its
                  database. For example, to create a hosted zone for
                  exämple.com, you specify ex\344mple.com for the domain name.
                  <code>ListHostedZonesByName</code> alphabetizes it as:</p> <p>
                  <code>com.ex\344mple.</code> </p> <p>The labels are reversed
                  and alphabetized using the escaped value. For more information
                  about valid domain name formats, including internationalized
                  domain names, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/DomainNameFormat.html">DNS
                  Domain Name Format</a> in the <i>Amazon Route 53 Developer
                  Guide</i>.</p> <p>Route 53 returns up to 100 items in each
                  response. If you have a lot of hosted zones, use the
                  <code>MaxItems</code> parameter to list them in groups of up
                  to 100. The response includes values that help navigate from
                  one group of <code>MaxItems</code> hosted zones to the
                  next:</p> <ul> <li> <p>The <code>DNSName</code> and
                  <code>HostedZoneId</code> elements in the response contain the
                  values, if any, specified for the <code>dnsname</code> and
                  <code>hostedzoneid</code> parameters in the request that
                  produced the current response.</p> </li> <li> <p>The
                  <code>MaxItems</code> element in the response contains the
                  value, if any, that you specified for the
                  <code>maxitems</code> parameter in the request that produced
                  the current response.</p> </li> <li> <p>If the value of
                  <code>IsTruncated</code> in the response is true, there are
                  more hosted zones associated with the current Amazon Web
                  Services account. </p> <p>If <code>IsTruncated</code> is
                  false, this response includes the last hosted zone that is
                  associated with the current account. The
                  <code>NextDNSName</code> element and
                  <code>NextHostedZoneId</code> elements are omitted from the
                  response.</p> </li> <li> <p>The <code>NextDNSName</code> and
                  <code>NextHostedZoneId</code> elements in the response contain
                  the domain name and the hosted zone ID of the next hosted zone
                  that is associated with the current Amazon Web Services
                  account. If you want to list more hosted zones, make another
                  call to <code>ListHostedZonesByName</code>, and specify the
                  value of <code>NextDNSName</code> and
                  <code>NextHostedZoneId</code> in the <code>dnsname</code> and
                  <code>hostedzoneid</code> parameters, respectively.</p> </li>
                  </ul>
                tags:
                  - Lists
                  - Hosted
                  - Zones
                  - By
                  - Names
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
            /2013-04-01/hostedzonesbyvpc:
              GET:
                summary: ListHostedZonesByVPC
                description: >-
                  <p>Lists all the private hosted zones that a specified VPC is
                  associated with, regardless of which Amazon Web Services
                  account or Amazon Web Services service owns the hosted zones.
                  The <code>HostedZoneOwner</code> structure in the response
                  contains one of the following values:</p> <ul> <li> <p>An
                  <code>OwningAccount</code> element, which contains the account
                  number of either the current Amazon Web Services account or
                  another Amazon Web Services account. Some services, such as
                  Cloud Map, create hosted zones using the current account. </p>
                  </li> <li> <p>An <code>OwningService</code> element, which
                  identifies the Amazon Web Services service that created and
                  owns the hosted zone. For example, if a hosted zone was
                  created by Amazon Elastic File System (Amazon EFS), the value
                  of <code>Owner</code> is <code>efs.amazonaws.com</code>. </p>
                  </li> </ul> <note> <p>When listing private hosted zones, the
                  hosted zone and the Amazon VPC must belong to the same
                  partition where the hosted zones were created. A partition is
                  a group of Amazon Web Services Regions. Each Amazon Web
                  Services account is scoped to one partition.</p> <p>The
                  following are the supported partitions:</p> <ul> <li> <p>
                  <code>aws</code> - Amazon Web Services Regions</p> </li> <li>
                  <p> <code>aws-cn</code> - China Regions</p> </li> <li> <p>
                  <code>aws-us-gov</code> - Amazon Web Services GovCloud (US)
                  Region</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html">Access
                  Management</a> in the <i>Amazon Web Services General
                  Reference</i>.</p> </note>
                tags:
                  - Lists
                  - Hosted
                  - Zones
                  - By
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
            /2013-04-01/hostedzone/{Id}/rrset:
              GET:
                summary: ListResourceRecordSets
                description: >-
                  <p>Lists the resource record sets in a specified hosted
                  zone.</p> <p> <code>ListResourceRecordSets</code> returns up
                  to 300 resource record sets at a time in ASCII order,
                  beginning at a position specified by the <code>name</code> and
                  <code>type</code> elements.</p> <p> <b>Sort order</b> </p> <p>
                  <code>ListResourceRecordSets</code> sorts results first by DNS
                  name with the labels reversed, for example:</p> <p>
                  <code>com.example.www.</code> </p> <p>Note the trailing dot,
                  which can change the sort order when the record name contains
                  characters that appear before <code>.</code> (decimal 46) in
                  the ASCII table. These characters include the following:
                  <code>! " # $ % &amp; ' ( ) * + , -</code> </p> <p>When
                  multiple records have the same DNS name,
                  <code>ListResourceRecordSets</code> sorts results by the
                  record type.</p> <p> <b>Specifying where to start listing
                  records</b> </p> <p>You can use the name and type elements to
                  specify the resource record set that the list begins with:</p>
                  <dl> <dt>If you do not specify Name or Type</dt> <dd> <p>The
                  results begin with the first resource record set that the
                  hosted zone contains.</p> </dd> <dt>If you specify Name but
                  not Type</dt> <dd> <p>The results begin with the first
                  resource record set in the list whose name is greater than or
                  equal to <code>Name</code>.</p> </dd> <dt>If you specify Type
                  but not Name</dt> <dd> <p>Amazon Route 53 returns the
                  <code>InvalidInput</code> error.</p> </dd> <dt>If you specify
                  both Name and Type</dt> <dd> <p>The results begin with the
                  first resource record set in the list whose name is greater
                  than or equal to <code>Name</code>, and whose type is greater
                  than or equal to <code>Type</code>.</p> </dd> </dl> <p>
                  <b>Resource record sets that are PENDING</b> </p> <p>This
                  action returns the most current version of the records. This
                  includes records that are <code>PENDING</code>, and that are
                  not yet available on all Route 53 DNS servers.</p> <p>
                  <b>Changing resource record sets</b> </p> <p>To ensure that
                  you get an accurate listing of the resource record sets for a
                  hosted zone at a point in time, do not submit a
                  <code>ChangeResourceRecordSets</code> request while you're
                  paging through the results of a
                  <code>ListResourceRecordSets</code> request. If you do, some
                  pages may display results without the latest changes while
                  other pages display results with the latest changes.</p> <p>
                  <b>Displaying the next page of results</b> </p> <p>If a
                  <code>ListResourceRecordSets</code> command returns more than
                  one page of results, the value of <code>IsTruncated</code> is
                  <code>true</code>. To display the next page of results, get
                  the values of <code>NextRecordName</code>,
                  <code>NextRecordType</code>, and
                  <code>NextRecordIdentifier</code> (if any) from the response.
                  Then submit another <code>ListResourceRecordSets</code>
                  request, and specify those values for
                  <code>StartRecordName</code>, <code>StartRecordType</code>,
                  and <code>StartRecordIdentifier</code>.</p>
                tags:
                  - Lists
                  - Resources
                  - Record
                  - Sets
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
            /2013-04-01/tags/{ResourceType}:
              POST:
                summary: ListTagsForResources
                description: >-
                  <p>Lists tags for up to 10 health checks or hosted zones.</p>
                  <p>For information about using tags for cost allocation, see
                  <a
                  href="https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html">Using
                  Cost Allocation Tags</a> in the <i>Billing and Cost Management
                  User Guide</i>.</p>
                tags:
                  - Lists
                  - Tags
                  - For
                  - Resources
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
            /2013-04-01/trafficpolicies:
              GET:
                summary: ListTrafficPolicies
                description: >-
                  <p>Gets information about the latest version for every traffic
                  policy that is associated with the current Amazon Web Services
                  account. Policies are listed in the order that they were
                  created in. </p> <p>For information about how of deleting a
                  traffic policy affects the response from
                  <code>ListTrafficPolicies</code>, see <a
                  href="https://docs.aws.amazon.com/Route53/latest/APIReference/API_DeleteTrafficPolicy.html">DeleteTrafficPolicy</a>.
                  </p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
            /2013-04-01/trafficpolicyinstances:
              GET:
                summary: ListTrafficPolicyInstances
                description: >-
                  <p>Gets information about the traffic policy instances that
                  you created by using the current Amazon Web Services
                  account.</p> <note> <p>After you submit an
                  <code>UpdateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. For
                  more information, see the <code>State</code> response
                  element.</p> </note> <p>Route 53 returns a maximum of 100
                  items in each response. If you have a lot of traffic policy
                  instances, you can use the <code>MaxItems</code> parameter to
                  list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Instances
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicyinstances/hostedzone:
              GET:
                summary: ListTrafficPolicyInstancesByHostedZone
                description: >-
                  <p>Gets information about the traffic policy instances that
                  you created in a specified hosted zone.</p> <note> <p>After
                  you submit a <code>CreateTrafficPolicyInstance</code> or an
                  <code>UpdateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. For
                  more information, see the <code>State</code> response
                  element.</p> </note> <p>Route 53 returns a maximum of 100
                  items in each response. If you have a lot of traffic policy
                  instances, you can use the <code>MaxItems</code> parameter to
                  list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Instances
                  - By
                  - Hosted
                  - Zones
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicyinstances/trafficpolicy:
              GET:
                summary: ListTrafficPolicyInstancesByPolicy
                description: >-
                  <p>Gets information about the traffic policy instances that
                  you created by using a specify traffic policy version.</p>
                  <note> <p>After you submit a
                  <code>CreateTrafficPolicyInstance</code> or an
                  <code>UpdateTrafficPolicyInstance</code> request, there's a
                  brief delay while Amazon Route 53 creates the resource record
                  sets that are specified in the traffic policy definition. For
                  more information, see the <code>State</code> response
                  element.</p> </note> <p>Route 53 returns a maximum of 100
                  items in each response. If you have a lot of traffic policy
                  instances, you can use the <code>MaxItems</code> parameter to
                  list them in groups of up to 100.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Instances
                  - By
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
            /2013-04-01/trafficpolicies/{Id}/versions:
              GET:
                summary: ListTrafficPolicyVersions
                description: >-
                  <p>Gets information about all of the versions for a specified
                  traffic policy.</p> <p>Traffic policy versions are listed in
                  numerical order by <code>VersionNumber</code>.</p>
                tags:
                  - Lists
                  - Traffic
                  - Policies
                  - Versions
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Versions
            /2013-04-01/testdnsanswer:
              GET:
                summary: TestDNSAnswer
                description: >-
                  <p>Gets the value that Amazon Route 53 returns in response to
                  a DNS request for a specified record name and type. You can
                  optionally specify the IP address of a DNS resolver, an EDNS0
                  client subnet IP address, and a subnet mask. </p> <p>This call
                  only supports querying public hosted zones.</p> <note> <p>The
                  <code>TestDnsAnswer </code> returns information similar to
                  what you would expect from the answer section of the
                  <code>dig</code> command. Therefore, if you query for the name
                  servers of a subdomain that point to the parent name servers,
                  those will not be returned.</
                tags:
                  - Tests
                  - Answers
                  - Hosted
                  - Zones
                  - Identifiers
                  - Names
                  - Activate
                  - Associate VPC
                  - CIDR
                  - Collections
                  - Rrset
                  - Resources
                  - Types
                  - '2013'
                  - '04'
                  - '01'
                  - CIDR Collection
                  - Health Check
                  - Hosted Zones
                  - Key Signing
                  - Query Logging Configurations
                  - Delegation Sets
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Authorizers VPC Association
                  - Deactivate
                  - Health
                  - Checks
                  - Versions
                  - Deauthorize VPC Association
                  - Disable
                  - DNS Security
                  - Disassociate VPC
                  - Enable
                  - Checker IP Ranges
                  - Geolocation
                  - Health Check
                  - Last Failure Reasons
                  - Status
                  - Hosted Zone Count
                  - Traffic Policy Instance Count
                  - CIDR Blocks
                  - Geolocation
                  - Hosted Zones
                  - Hosted Zones
                  - Traffic Policies
                  - Traffic Policy Instances
                  - Versions
                  - Testdnsansw
    overlays:
      - type: APIs.io Search
        url: overlays/route53-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53
  - aid: bigcommerce:themes
    name: Themes
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
          openapi: 3.0.0
          info:
            title: Themes
            version: ''
            license:
              name: ''
          tags:
            - name: Themes
            - name: Theme Actions
            - name: Theme Configurations
            - name: Theme Custom Templates
            - name: Theme Jobs
          paths:
            /themes:
              parameters:
                - null
              get:
                tags:
                  - Get
                  - All
                  - Themes
                  - Themes
                summary: Get all Themes
                description: Returns a list of store *Themes*.
              post:
                tags:
                  - Upload
                  - Theme
                  - Themes
                summary: Upload a Theme
                description: |-
                  Uploads a new *Theme* to your BigCommerce store.

                  **Required Fields**
                  * file
            /themes/{uuid}:
              get:
                tags:
                  - Get
                  - Theme
                  - Themes
                  - Uuid
                summary: Get a Theme
                description: >-
                  Returns a store *Theme*. The theme variation is not available
                  at this endpoint.
              delete:
                tags:
                  - Delete
                  - Theme
                  - Themes
                  - Uuid
                summary: Delete a Theme
                description: >-
                  Deletes a store *Theme*.

                  Theme variations can not be deleted using this endpoint. This
                  will delete the theme and all variations.
              parameters:
                - null
                - null
            /themes/{uuid}/actions/download:
              parameters:
                - null
                - null
              post:
                tags:
                  - Download
                  - Theme
                  - Themes
                  - Uuid
                  - Actions
                  - Download
                summary: Download a Theme
                description: Downloads a stores *Theme*.
            /themes/actions/activate:
              parameters:
                - null
                - null
              post:
                tags:
                  - Activate
                  - Theme
                  - Themes
                  - Uuid
                  - Actions
                  - Download
                  - Activate
                summary: Activate a Theme
                description: |-
                  Actives a store *Theme*.

                  This returns a 204 response upon success.
            /themes/jobs/{job_id}:
              get:
                tags:
                  - Get
                  - Theme
                  - Job
                  - Themes
                  - Uuid
                  - Actions
                  - Download
                  - Activate
                  - Jobs
                  - Job_id
                summary: Get a Theme Job
                description: >-
                  Returns a theme *Job*. When the job is complete, the results
                  array provides a generated link to access the theme. The link
                  is active for 60 seconds.
              parameters:
                - null
                - null
            /themes/{uuid}/configurations:
              get:
                tags:
                  - Get
                  - Theme
                  - Configuration
                  - Themes
                  - Uuid
                  - Actions
                  - Download
                  - Activate
                  - Jobs
                  - Job_id
                  - Configurations
                summary: Get Theme Configuration
                description: |-
                  Returns a list of theme's configurations.

                  **Usage Notes**:
                  * At least one filter must be provided.
              parameters:
                - null
                - null
                - null
                - null
                - null
                - null
            /themes/{uuid}/configurations/validate:
              post:
                summary: Validate Theme Configuration
                tags:
                  - Validate
                  - Theme
                  - Configuration
                  - Themes
                  - Uuid
                  - Actions
                  - Download
                  - Activate
                  - Jobs
                  - Job_id
                  - Configurations
                  - Validate
                description: >-
                  Validates a theme configuration against the theme's schema
                  without creating it. Useful for testing schemas before
                  creation.
              parameters:
                - null
                - null
            /themes/custom-templates/{version_uuid}:
              parameters:
                - null
                - null
              get:
                summary: Get Custom Templates
                tags:
                  - Get
                  - Custom
                  - Templates
                  - Themes
                  - Uuid
                  - Actions
                  - Download
                  - Activate
                  - Jobs
                  - Job_id
                  - Configurations
                  - Validate
                  - Custom
                  - Templates
                  - Version_uuid
                description: >-
                  Enumerate available custom templates for in the theme files in
                  a specific theme version for each supported 
    overlays:
      - type: APIs.io Search
        url: overlays/themes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/themes-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---