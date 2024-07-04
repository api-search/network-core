---
name: Conditions
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/conditions.png
url: https://example.com/apis/conditions.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Conditions
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
                  - null
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
  - name: FactSet Terms and Conditions API
    description: FactSet Security Reference - Fixed Income Terms & Conditions
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-terms-and-conditions-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-terms-and-conditions-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Terms & Conditions API
            license:
              name: License Information
              url: http://www.factset.com/api/license.html
          tags:
            - name: Terms & Conditions
              description: >-
                Select specific Terms & Conditions fields for a list of Fixed
                Income Security identifiers.
            - name: Issue Size
              description: >-
                Fetch the Fixed Income Issue Details, such as Amount
                Outstanding, Change, and Type.
            - name: Coupons
              description: Coupon History and Schedules
            - name: Covenants
              description: Covenant Details and Negative Covenants
            - name: Redemptions
              description: Redemption Prices
            - name: Agents
              description: Agency Details
            - name: Use of Proceeds
              description: Use of Proceeds raised from Fixed Income Issues
            - name: Underwriters
              description: Lead Underwriter Details
            - name: Convertibles
              description: Convertible Details, History, and Triggers
          paths:
            /factset-terms-and-conditions/v1/terms-and-conditions:
              get:
                summary: >-
                  Return select Terms and Conditions items for a Fixed Income
                  security.
                description: >
                  Returns Terms and Conditions data items for the Fixed Income
                  security. Includes items for Conditional Redemptions,
                  Redemption Options, Security Details, and Coupon Details.

                  Use the `fields` parameter to request specific items only or
                  request an entire category of items to fetch all available
                  fields matching that category(s).

                  <p>*For T&C data related to Agency, Coupon History, Issue
                  Size, Negative Covenants, or Redemption Prices, Lead
                  Underwriters, and Use of Proceeds, please use respective
                  endpoints optimized for that content.*</p>
                tags:
                  - Return
                  - Select
                  - Terms
                  - And
                  - Conditions
                  - Items
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
              post:
                summary: >-
                  Return Terms and Conditions for a list of Fixed Income
                  securities.
                description: >
                  Returns Terms and Conditions data items for the Fixed Income
                  security. Includes reference items for Conditional
                  Redemptions, Redemption Options, Security Details, Convertible
                  Features, and Coupon Details.

                  Use the `fields` parameter to request specific items only or
                  request an entire category of items to fetch all available
                  fields matching that category(s).

                  <p>*For T&C data related to Agency, Coupon History, Issue
                  Size, Negative Covenants, or Redemption Prices, Lead
                  Underwriters, and Use of Proceeds, please use respective
                  endpoints optimized for that content.*</p>
                tags:
                  - Return
                  - Terms
                  - And
                  - Conditions
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
            /factset-terms-and-conditions/v1/fields:
              get:
                summary: Available fields for /terms-and-conditions endpoint
                tags:
                  - Available
                  - Fields
                  - For
                  - /terms-and-conditions
                  - Endpoint
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                description: >
                  Returns a list of available fields that can be used in the
                  `fields`

                  parameter of the **/terms-and-conditions** endpoint.

                  Leave _category_ blank to request all available items.

                  Make Note, this does not represent all available fields within
                  the Terms and Conditions API and all other endpoints.
            /factset-terms-and-conditions/v1/issue-size:
              get:
                summary: Return Issue Size data for a list of Fixed Income securities.
                description: |
                  Returns Issue Size data for the Fixed Income security.
                tags:
                  - Return
                  - Issue
                  - Size
                  - Data
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
              post:
                summary: >-
                  Return Issue Size data for a large list of Fixed Income
                  securities.
                description: |
                  Returns Issue Size data for a list of Fixed Income securities.
                tags:
                  - Return
                  - Issue
                  - Size
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
            /factset-terms-and-conditions/v1/coupon-history:
              get:
                summary: >-
                  Return historical Coupon information for a Fixed Income
                  security.
                description: >
                  Returns historical Coupon information for the Fixed Income
                  security.
                tags:
                  - Return
                  - Historical
                  - Coupon
                  - Information
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
              post:
                summary: >-
                  Return historical Coupon information for a list of Fixed
                  Income securities.
                description: >
                  Returns historical Coupon information for a list of Fixed
                  Income securities.
                tags:
                  - Return
                  - Historical
                  - Coupon
                  - Information
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
            /factset-terms-and-conditions/v1/coupon-schedules:
              get:
                summary: Return Coupon Sechedules for a Fixed Income security.
                description: >
                  Returns Coupon Schedules information for the Fixed Income
                  security.
                tags:
                  - Return
                  - Coupon
                  - Sechedules
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
              post:
                summary: >-
                  Return Coupon Schedules information for a list of Fixed Income
                  securities.
                description: >
                  Returns historical Coupon Schedules information for a list of
                  Fixed Income securities.
                tags:
                  - Return
                  - Coupon
                  - Schedules
                  - Information
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
            /factset-terms-and-conditions/v1/covenant-details:
              get:
                summary: Return Covenant Details for a Fixed Income security.
                description: |
                  Returns Covenant Details for the Fixed Income security.
                tags:
                  - Return
                  - Covenant
                  - Details
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
              post:
                summary: Return Covenant Details for a list of Fixed Income securities.
                description: >
                  Returns Covenant Details for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Covenant
                  - Details
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
            /factset-terms-and-conditions/v1/redemption-prices:
              get:
                summary: Return Redemption Prices for a Fixed Income security.
                description: |
                  Returns Redemption Prices for the Fixed Income security.
                tags:
                  - Return
                  - Redemption
                  - Prices
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
              post:
                summary: >-
                  Return Redemption Prices for a list of Fixed Income
                  securities.
                description: >
                  Returns Redemption Prices for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Redemption
                  - Prices
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
            /factset-terms-and-conditions/v1/agents:
              get:
                summary: Return Agents items for a Fixed Income security.
                description: |
                  Returns Agents data items for the Fixed Income security.
                tags:
                  - Return
                  - Agents
                  - Items
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
              post:
                summary: Return Agents items for a list of Fixed Income securities.
                description: >
                  Returns Agents data items for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Agents
                  - Items
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
            /factset-terms-and-conditions/v1/lead-underwriters:
              get:
                summary: Return Lead Underwriters for a Fixed Income security.
                description: |
                  Returns Lead Underwriters for the Fixed Income security.
                tags:
                  - Return
                  - Lead
                  - Underwriters
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
              post:
                summary: >-
                  Return Lead Underwriters for a list of Fixed Income
                  securities.
                description: >
                  Returns Lead Underwriters for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Lead
                  - Underwriters
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
            /factset-terms-and-conditions/v1/use-of-proceeds:
              get:
                summary: Return Use of Proceeds for a Fixed Income security.
                description: |
                  Returns Use of Proceeds for the Fixed Income security.
                tags:
                  - Return
                  - Use
                  - Of
                  - Proceeds
                  - For
                  - Fixed
                  - Income
                  - Security.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
              post:
                summary: Return Use of Proceeds for a list of Fixed Income securities.
                description: |
                  Returns Use of Proceeds for a list of Fixed Income securities.
                tags:
                  - Return
                  - Use
                  - Of
                  - Proceeds
                  - For
                  - List
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
            /factset-terms-and-conditions/v1/convertible-details:
              get:
                summary: >-
                  Return Convertible Details for a list of Convertible Fixed
                  Income securities.
                description: >
                  Returns Convertible Details for a list of securities, such as
                  -
                    * Convertible Currency
                    * Convertible Effective Date
                    * Convertible Notice Days Max and Min
                    * Convertible Payment Form
                    * Convertible Payment Details
                    * Convertible Payment Form Election
                    * Convertible Price Method
                    * Convertible Type
                    * Convertibles Ratio
                    * More
                tags:
                  - Return
                  - Convertible
                  - Details
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
              post:
                summary: >-
                  Return Convertible Details data for a large list of Fixed
                  Income securities.
                description: >
                  Returns Convertible Details for a list of securities, such as
                  -
                    * Convertible Currency
                    * Convertible Effective Date
                    * Convertible Notice Days Max and Min
                    * Convertible Payment Form
                    * Convertible Payment Details
                    * Convertible Payment Form Election
                    * Convertible Price Method
                    * Convertible Type
                    * Convertibles Ratio
                    * More
                tags:
                  - Return
                  - Convertible
                  - Details
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
            /factset-terms-and-conditions/v1/convertible-history:
              get:
                summary: >-
                  Return Convertible History data for a list of Fixed Income
                  securities.
                description: >
                  Returns Convertible History data for the Fixed Income
                  security, including - * Convertibles Price * Convertibles
                  Effective Date
                tags:
                  - Return
                  - Convertible
                  - History
                  - Data
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
              post:
                summary: >-
                  Return Convertible History data for a large list of Fixed
                  Income securities.
                description: >
                  Returns Convertible History data for a list of Fixed Income
                  securities.
                tags:
                  - Return
                  - Convertible
                  - History
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
            /factset-terms-and-conditions/v1/convertible-triggers:
              get:
                summary: >-
                  Return Convertible Triggers data for a list of Fixed Income
                  securities.
                description: >
                  Returns Convertible Triggers data for the Fixed Income
                  security including the Convertible Trigger Id, Event, and
                  Description.
                tags:
                  - Return
                  - Convertible
                  - Triggers
                  - Data
                  - For
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
                  - Triggers
              post:
                summary: >-
                  Return Convertible Trigger data for a large list of Fixed
                  Income securities.
                description: >
                  Returns Convertible Triggers data for the Fixed Income
                  security including the Convertible Trigger Id, Event, and
                  Description.
                tags:
                  - Return
                  - Convertible
                  - Trigger
                  - Data
                  - For
                  - Large
                  - List
                  - Of
                  - Fixed
                  - Income
                  - Securities.
                  - Factset
                  - Terms
                  - And
                  - Conditions
                  - V1
                  - Fields
                  - Issue
                  - Size
                  - Coupon
                  - History
                  - Schedules
                  - Covenant
                  - Details
                  - Redemption
                  - Prices
                  - Agents
                  - Lead
                  - Underwriters
                  - Use
                  - Of
                  - Proceeds
                  - Convertible
                  - Trigge
    overlays:
      - type: APIs.io Search
        url: overlays/terms-and-conditions-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/terms-and-conditions-openapi-api-evangelist-ratings.yml
    aid: factset:factset-terms-and-conditions-api
  - name: FactSet Options API
    description: >-
      The FactSet Options API provides Chains and related pricing data such as
      mid bid-ask price, reference data (e.g., strike price), and risk measures
      (e.g., Greeks and implied volatility).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/factset-options-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/factset-options-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-options-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FactSet Options API
          tags:
            - name: Option Chains & Screening
              description: >-
                Generate a list or universe of options ids based on underlying
                securities or other conditions
            - name: Snapshot
              description: >-
                A generic profile for a list of option securities as of a
                specific date
            - name: Reference
              description: Option Reference Information and Dates
            - name: Prices & Volume
              description: >-
                Option Prices & Volume information for a requested time-range
                for the option security or aggregated for all options associated
                to the underlying security
            - name: Risk Measures
              description: >-
                Option Risk measures such as Greeks, Implied Volatilities, and
                Calculators
          paths:
            /factset-options/v1/chains:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Underlying
                  - Option
                  - Identifiers
                  - For
                  - Specified
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                summary: >-
                  Returns all the underlying option identifiers for the
                  specified underlying Security identifier
                description: >
                  Returns all the underlying option identifiers for the
                  underlying security identifier. Specify the date and or
                  exhcange for the list of options associated to the id. 

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/option-screening:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Option
                  - Identifiers
                  - Based
                  - 'On'
                  - Conditions
                  - Provided
                  - As
                  - Input
                  - In
                  - Request
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                summary: >-
                  Returns all the option identifiers based on the conditions
                  provided as input in the request
                description: >
                  Returns all the option identifiers based on the conditions
                  provided as input in the request. Conditions are as follows
                  and will follow "AND" logic if more than one condition is
                  applied and allows up to **three conditions** using AND
                  Logic.If a condition is used the accompanying value MUST be
                  used - 

                  |conditions|description|

                  |||

                  |P_OPT_UNDERLYING_SECURITY_E|Underlying Security Equal To|

                  |P_OPT_STRIKE_PRICE_E|Strike Price Equal To|

                  |P_OPT_EXP_DATEN_E|Expiration Date (YYYYMMDD) Equal To|

                  |P_OPT_VOLUME_G|Volume Greater Than|

                  |P_OPT_VOLUME_GE|Volume Greater Than or Equal To|

                  |P_OPT_VOLUME_L|Volume Less Than|

                  |P_OPT_VOLUME_LE|Volume Less Than or Equal To|

                  |P_OPT_VOLUME_E|Volume Equal To|

                  |P_OPT_OPTION_TYPE_E|Option Type (1= Equity, 2=Index)|

                  |P_OPT_CALL_OR_PUT_E|Call or Put (0=Call, 1=Put)|

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/snapshot:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Profile
                  - Information
                  - For
                  - List
                  - Of
                  - Identifiers
                  - As
                  - Specific
                  - Date
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                summary: >-
                  Returns all the profile information for the list of
                  identifiers as of a specific date
                description: >
                  Returns all the profile information for the list of
                  identifiers for a specific date. The data includes - 

                  * Expiration Date

                  * Greek - Delta

                  * Implied Volatility

                  * Price 

                  * Style

                  * Type

                  * Underlying Security

                  * Underlying Security Price

                  * Open Interest

                  * Name

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/references:
              post:
                tags:
                  - Returns
                  - Basic
                  - Reference
                  - Details
                  - For
                  - The
                  - Options
                  - Such
                  - As
                  - Currency,
                  - Exchange,
                  - Symbols,
                  - Flags
                  - And
                  - More
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                summary: >-
                  Returns basic reference details for the options such as
                  currency, exchange, symbols, flags and more
                description: >
                  Returns basic reference details for the options. Data items
                  include - 

                  * Name

                  * Exchange

                  * Call or Put Flag

                  * Call or Put Pair Symbol

                  * Other symbols such as OPRA17 and OCC21

                  * Currency

                  * Underlying Security Symbols

                  * Expiration Month, Dates, and Frequency


                  *For details or definitions of all available response fields
                  visit the associated schema.*

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/dates:
              post:
                tags:
                  - Returns
                  - Option
                  - Security
                  - Dates
                  - Such
                  - As
                  - Expiration
                  - And
                  - Trade.
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                summary: Returns option security dates such as expiration and trade.
                description: >
                  Returns all relevant dates such as  for the specified Option
                  identifier. Data Items include - 

                  * Expiration Date

                  * First Dates for Ask, Bid, Settlement, and Trade

                  * Last Dates for Ask, Bid, Settlement, and Trade

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/prices:
              post:
                tags:
                  - Returns
                  - The
                  - Pricing
                  - Related
                  - Information
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                summary: >-
                  Returns the pricing related information for the specified
                  option identifier
                description: >
                  Returns the pricing related information for the specified
                  option identifier. Items include - 

                  * Ask

                  * Bid

                  * Mid

                  * Mid Bid Ask

                  * Settlement

                  * Last Price Type (Settlement or MidBidAsk)

                  * Last Price

                  * Strike Price

                  * Underlying Security Price

                  * 52 Week High/Low

                  * Open, High, Low for day. Note securities must be trading for
                  day requested.

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/underlying-volume:
              post:
                tags:
                  - Returns
                  - The
                  - Aggregate
                  - Volume
                  - And
                  - Open
                  - Interest
                  - For
                  - List
                  - Of
                  - Options
                  - Under
                  - Specified
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                summary: >-
                  Returns the aggregate volume and open interest for the list of
                  the options under the specified security identifier
                description: >
                  Return the Volume and Open Interest details for list of the
                  options for the specified underlying security identifier. The
                  data is aggregated for all options contracts associated to the
                  underlying id, or specified in the request only the contracts
                  listed on a specific exchange. Data Includes - 

                  * Put Call Ratio 

                  * Total Put Volume & Open Interest

                  * Total Call Volume & Open Interest

                  * Total Put & Call Volume & Open Interest

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/volume:
              post:
                tags:
                  - Returns
                  - The
                  - Volume
                  - Details
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                summary: Returns the volume details for the specified option identifier
                description: >
                  Returns the volume details for the specified option identifier
                  for a specified exchange. Data items include - 

                  * Open Interest

                  * Volume

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/greeks:
              post:
                tags:
                  - Returns
                  - All
                  - The
                  - Greeks
                  - Details
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                summary: >-
                  Returns all the Greeks details for the specified option
                  identifier
                description: >
                  Returns all the greeks details for the specified option
                  identifier. Greeks provide quantifiable factors for measuring
                  the option's price sensativity. Greeks include -


                  |Greek|Description|

                  |||

                  |Delta| The ratio comparing the change in the price of the
                  underlying asset to the corresponding change in the price of a
                  derivative. Sometimes referred to as the "hedge ratio". For
                  example, with respect to call options, a delta of 0.7 means
                  that for every $1 the underlying stock increases, the call
                  option will increase by $0.70. Put option deltas, on the other
                  hand, will be negative, because as the underlying security
                  increases, the value of the option will decrease. So a put
                  option with a delta of -0.7 will decrease by $0.70 for every
                  $1 the underlying increases in price. As an in-the-money call
                  option nears expiration, it will approach a delta of 1.00, and
                  as an in-the-money put option nears expiration, it will
                  approach a delta of -1.00.|

                  |Gamma| The rate of change for delta with respect to the
                  underlying asset's price. Mathematically, gamma is the first
                  derivative of delta and is used when trying to gauge the price
                  of an option relative to the amount it is in or out of the
                  money. When the option being measured is deep in or out of the
                  money, gamma is small. When the option is near the money,
                  gamma is largest.|

                  |Rho|The rate at which the price of a derivative changes
                  relative to a change in the risk-free rate of interest. Rho
                  measures the sensitivity of an option or options portfolio to
                  a change in interest rate.|

                  |Theta|A measure of the rate of decline in the value of an
                  option due to the passage of time. Theta can also be referred
                  to as the time decay on the value of an option. If everything
                  is held constant, then the option will lose value as time
                  moves closer to the maturity of the option. For example, if
                  the strike price of an option is $1,150 and theta is 53.80,
                  then in theory the value of the option will drop $53.80 per
                  day. The measure of theta quantifies the risk that time
                  imposes on options as options are only exercisable for a
                  certain period of time.|

                  |Vega|The amount that the price of an option changes compared
                  to a 1% change in volatility. Vega changes when there are
                  large price movements in the underlying asset and vega falls
                  as the option gets closer to maturity. Vega can change even if
                  there is no change in the price of the underlying asset, this
                  would happen if there is a change in expected volatility. For
                  example, if the vega of an option is -96.94 and if implied
                  volatility were to rise by 1% then the option value would fall
                  by $96.94.|


                  Note
                    * Each step in the binomial model represents a change in time, therefore, point estimates of the Greeks can be calculated for American options. The following can be used to calculate the Greeks for the Binomial Option Pricing Model (BOPM) pricing model, using the notation fstep,node so f1,1 represents the option price at the first step, top node (nodes are counted at each step starting with 0 at the bottom. See [Constructing the Tree](https://my.apps.factset.com/oa/pages/17735#tree) for more information).
                    
                  For more detials on calculation methodologies, visit [OA
                  14933](https://my.apps.factset.com/oa/pages/14933). 

                    *Currently only OPRA Exchange is supported with exchange ISO "USA"*
            /factset-options/v1/implied-volatility:
              post:
                tags:
                  - Returns
                  - The
                  - Implied
                  - Volatility
                  - Information
                  - For
                  - Specified
                  - Option
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                  - Implied
                  - Volatility
                summary: >-
                  Returns the implied volatility information for the specified
                  option identifier
                description: >
                  Returns the Implied Volatility for the specified option across
                  European and American contracts. For more details regarding
                  Implied Volatility calculations visit - [OA
                  14932](https://my.apps.factset.com/oa/pages/14932)


                  *Currently the following exchanges are not supported for API
                  use cases - CME, CMEE, CBT, CBTE, NYM, NYME*
            /factset-options/v1/atm-implied-volatility:
              post:
                tags:
                  - Returns
                  - The
                  - At-the-money
                  - M)
                  - Implied
                  - Volatility
                  - Details
                  - For
                  - Specified
                  - Underlying
                  - Security
                  - Identifier
                  - Factset
                  - Options
                  - V1
                  - Chains
                  - Option
                  - Screening
                  - Snapshot
                  - References
                  - Dates
                  - Prices
                  - Underlying
                  - Volume
                  - Greeks
                  - Implied
                  - Volatility
                  - Atm
                summary: >-
                  Returns the at-the-money (ATM) implied volatility details for
                  the specified underlying security identifier
                description: >
                  Returns weighted average of the implied volatilities from the
                  options listed for a specified security identifier. 


                  There are three different methods available for calculating
                  at-the-money implied volatility (ATM IV), which gives a
                  weighted average of the implied volatilities from the options
                  listed on a given stock. They are ATM IV (Filtered), ATM IV
                  (Filtered with Smoothing), and ATM IV (Market). Each of these
                  ATM IV calculations is available for just the calls on a given
                  stock, just the puts, or the composite of both the calls and
                  puts.

                  This at-the-money implied volatility market can calculated for
                  different periods -

                  * One Month

                  * Two Months

                  * Three Months

                  * Four Months

                  * Five Months

                  * Six Months


                  *For more details regarding ATM Volatility calculations, visit
                  [OA 16276](https://my.apps.factset.com/oa/pages/16276)*

                    *Currently only OPRA Exchange traded op
    overlays:
      - type: APIs.io Search
        url: overlays/options-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/options-openapi-api-evangelist-ratings.yml
    aid: factset:factset-options-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---