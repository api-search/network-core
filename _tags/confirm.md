---
name: Confirm
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/confirm.png
url: https://example.com/apis/confirm.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Confirm
apis:
  - name: Adyen Legal Entity API
    description: >-
      The Legal Entity Management API enables you to manage legal entities that
      contain information required for verification.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Legal Entity Management API
          tags:
            - name: Legal entities
            - name: Transfer instruments
            - name: Business lines
            - name: Documents
            - name: Terms of Service
            - name: Hosted Onboarding
            - name: Questionnaires
          paths:
            /businessLines:
              post:
                tags:
                  - Create
                  - Business
                  - Line
                  - Lines
                summary: Create a business line
                description: >+
                  Creates a business line. 


                  This resource contains information about your user's line of
                  business, including their industry and their source of funds.
                  Adyen uses this information to verify your users as required
                  by payment industry regulations. Adyen informs you of the
                  verification results through webhooks or API responses.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /businessLines/{id}:
              delete:
                tags:
                  - Delete
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Delete a business line
                description: |-
                  Deletes a business line.

                   >If you delete a business line linked to a [payment method](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api), it can affect your merchant account's ability to use the [payment method](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/_merchantId_/paymentMethodSettings). The business line is removed from all linked merchant accounts.
              get:
                tags:
                  - Get
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Get a business line
                description: Returns the detail of a business line.
              patch:
                tags:
                  - Update
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Update a business line
                description: Updates a business line.
            /documents:
              post:
                tags:
                  - Uploads
                  - Document
                  - For
                  - Verification
                  - Checks
                  - Lines
                  - Identifiers
                  - Documents
                summary: Upload a document for verification checks
                description: |-
                  Uploads a document for verification checks.

                   Adyen uses the information from the [legal entity](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/legalEntities) to run automated verification checks. If these checks fail, you will be notified to provide additional documents.

                   You should only upload documents when Adyen requests additional information for the legal entity.

                   >You can upload a maximum of 15 pages for photo IDs.
            /documents/{id}:
              delete:
                tags:
                  - Delete
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Delete a document
                description: Deletes a document.
              get:
                tags:
                  - Get
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Get a document
                description: Returns a document.
              patch:
                tags:
                  - Update
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Update a document
                description: |-
                  Updates a document.

                   >You can upload a maximum of 15 pages for photo IDs.
            /legalEntities:
              post:
                tags:
                  - Create
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Create a legal entity
                description: >+
                  Creates a legal entity. 


                  This resource contains information about the user that will be
                  onboarded in your platform. Adyen uses this information to
                  perform verification checks as required by payment industry
                  regulations. Adyen informs you of the verification results
                  through webhooks or API responses. 


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}:
              get:
                tags:
                  - Get
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Get a legal entity
                description: Returns a legal entity.
              patch:
                tags:
                  - Update
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Update a legal entity
                description: |-
                  Updates a legal entity.

                   >To change the legal entity type, include only the new `type` in your request. To update the `entityAssociations` array, you need to replace the entire array. For example, if the array has 3 entries and you want to remove 1 entry, you need to PATCH the resource with the remaining 2 entries.
            /legalEntities/{id}/businessLines:
              get:
                tags:
                  - Get
                  - All
                  - Business
                  - Lines
                  - Under
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                summary: Get all business lines under a legal entity
                description: Returns the business lines owned by a legal entity.
            /legalEntities/{id}/checkVerificationErrors:
              post:
                tags:
                  - Checks
                  - Legal
                  - Entities
                  - Verification
                  - Errors
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                summary: Check a legal entity's verification errors
                description: >-
                  Returns the verification errors for a legal entity and its
                  supporting entities.
            /legalEntities/{id}/confirmDataReview:
              post:
                tags:
                  - Confirm
                  - Data
                  - Reviews
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                summary: Confirm data review
                description: >-
                  Confirms that your user has reviewed the data for the legal
                  entity specified in the path. Call this endpoint to inform
                  Adyen that your user reviewed and verified that the data is
                  up-to-date. The endpoint returns the timestamp of when Adyen
                  received the request.
            /legalEntities/{id}/onboardingLinks:
              post:
                tags:
                  - Get
                  - Link
                  - To
                  - null
                  - Adyen-hosted
                  - Onboarding
                  - Page
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                summary: Get a link to an Adyen-hosted onboarding page
                description: >+
                  Returns a link to an Adyen-hosted onboarding page where you
                  need to redirect your user.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}/pciQuestionnaires:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Details
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                summary: Get PCI questionnaire details
                description: Get a list of signed PCI questionnaires.
            /legalEntities/{id}/pciQuestionnaires/generatePciTemplates:
              post:
                tags:
                  - Generate
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                summary: Generate PCI questionnaire
                description: >-
                  Generates the required PCI questionnaires based on the user's
                  [salesChannel](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/businessLines__reqParam_salesChannels).
            /legalEntities/{id}/pciQuestionnaires/signPciTemplates:
              post:
                tags:
                  - Sign
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                summary: Sign PCI questionnaire
                description: Signs the required PCI questionnaire.
            /legalEntities/{id}/pciQuestionnaires/{pciid}:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                summary: Get PCI questionnaire
                description: Returns the signed PCI questionnaire.
            /legalEntities/{id}/termsOfService:
              post:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                summary: Get Terms of Service document
                description: Returns the Terms of Service document for a legal entity.
            /legalEntities/{id}/termsOfService/{termsofservicedocumentid}:
              patch:
                tags:
                  - Accept
                  - Terms
                  - Of
                  - Services
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                summary: Accept Terms of Service
                description: Accepts Terms of Service.
            /legalEntities/{id}/termsOfServiceAcceptanceInfos:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Information
                  - For
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                summary: Get Terms of Service information for a legal entity
                description: Returns Terms of Service information for a legal entity.
            /legalEntities/{id}/termsOfServiceStatus:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Status
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                summary: Get Terms of Service status
                description: >-
                  Returns the required types of Terms of Service that need to be
                  accepted by a legal entity.
            /themes:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Hosted
                  - Onboarding
                  - Page
                  - Themes
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get a list of hosted onboarding page themes
                description: >+
                  Returns a list of hosted onboarding page themes.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /themes/{id}:
              get:
                tags:
                  - Get
                  - null
                  - Onboarding
                  - Link
                  - Theme
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get an onboarding link theme
                description: >+
                  Returns the details of the theme identified in the path.>If
                  you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /transferInstruments:
              post:
                tags:
                  - Create
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Create a transfer instrument
                description: >-
                  Creates a transfer instrument. 


                  A transfer instrument is a bank account that a legal entity
                  owns. Adyen performs verification checks on the transfer
                  instrument as required by payment industry regulations. We
                  inform you of the verification results through webhooks or API
                  responses.


                  When the transfer instrument passes the verification checks,
                  you can start sending funds from the balance platform to the
                  transfer instrument (such as payouts).
            /transferInstruments/{id}:
              delete:
                tags:
                  - Delete
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Delete a transfer instrument
                description: Deletes a transfer instrument.
              get:
                tags:
                  - Get
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Get a transfer instrument
                description: Returns the details of a transfer instrument.
              patch:
                tags:
                  - Update
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Update a transfer instrument
                description: null
    overlays:
      - type: APIs.io Search
        url: overlays/legal-entity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/legal-entity-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-legal-entity-api
  - name: Adyen Legal Entity API
    description: >-
      The Legal Entity Management API enables you to manage legal entities that
      contain information required for verification.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://docs.adyen.com/marketplaces-and-platforms/legal-entity-management-api/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Legal Entity Management API
          tags:
            - name: Legal entities
            - name: Transfer instruments
            - name: Business lines
            - name: Documents
            - name: Terms of Service
            - name: Hosted Onboarding
            - name: Questionnaires
          paths:
            /businessLines:
              post:
                tags:
                  - Create
                  - Business
                  - Line
                  - Lines
                summary: Create a business line
                description: >+
                  Creates a business line. 


                  This resource contains information about your user's line of
                  business, including their industry and their source of funds.
                  Adyen uses this information to verify your users as required
                  by payment industry regulations. Adyen informs you of the
                  verification results through webhooks or API responses.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /businessLines/{id}:
              delete:
                tags:
                  - Delete
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Delete a business line
                description: |-
                  Deletes a business line.

                   >If you delete a business line linked to a [payment method](https://docs.adyen.com/development-resources/paymentmethodvariant#management-api), it can affect your merchant account's ability to use the [payment method](https://docs.adyen.com/api-explorer/Management/latest/post/merchants/_merchantId_/paymentMethodSettings). The business line is removed from all linked merchant accounts.
              get:
                tags:
                  - Get
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Get a business line
                description: Returns the detail of a business line.
              patch:
                tags:
                  - Update
                  - Business
                  - Line
                  - Lines
                  - Identifiers
                summary: Update a business line
                description: Updates a business line.
            /documents:
              post:
                tags:
                  - Uploads
                  - Document
                  - For
                  - Verification
                  - Checks
                  - Lines
                  - Identifiers
                  - Documents
                summary: Upload a document for verification checks
                description: |-
                  Uploads a document for verification checks.

                   Adyen uses the information from the [legal entity](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/legalEntities) to run automated verification checks. If these checks fail, you will be notified to provide additional documents.

                   You should only upload documents when Adyen requests additional information for the legal entity.

                   >You can upload a maximum of 15 pages for photo IDs.
            /documents/{id}:
              delete:
                tags:
                  - Delete
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Delete a document
                description: Deletes a document.
              get:
                tags:
                  - Get
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Get a document
                description: Returns a document.
              patch:
                tags:
                  - Update
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                summary: Update a document
                description: |-
                  Updates a document.

                   >You can upload a maximum of 15 pages for photo IDs.
            /legalEntities:
              post:
                tags:
                  - Create
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Create a legal entity
                description: >+
                  Creates a legal entity. 


                  This resource contains information about the user that will be
                  onboarded in your platform. Adyen uses this information to
                  perform verification checks as required by payment industry
                  regulations. Adyen informs you of the verification results
                  through webhooks or API responses. 


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}:
              get:
                tags:
                  - Get
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Get a legal entity
                description: Returns a legal entity.
              patch:
                tags:
                  - Update
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                summary: Update a legal entity
                description: |-
                  Updates a legal entity.

                   >To change the legal entity type, include only the new `type` in your request. To update the `entityAssociations` array, you need to replace the entire array. For example, if the array has 3 entries and you want to remove 1 entry, you need to PATCH the resource with the remaining 2 entries.
            /legalEntities/{id}/businessLines:
              get:
                tags:
                  - Get
                  - All
                  - Business
                  - Lines
                  - Under
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                summary: Get all business lines under a legal entity
                description: Returns the business lines owned by a legal entity.
            /legalEntities/{id}/checkVerificationErrors:
              post:
                tags:
                  - Checks
                  - Legal
                  - Entities
                  - Verification
                  - Errors
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                summary: Check a legal entity's verification errors
                description: >-
                  Returns the verification errors for a legal entity and its
                  supporting entities.
            /legalEntities/{id}/confirmDataReview:
              post:
                tags:
                  - Confirm
                  - Data
                  - Reviews
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                summary: Confirm data review
                description: >-
                  Confirms that your user has reviewed the data for the legal
                  entity specified in the path. Call this endpoint to inform
                  Adyen that your user reviewed and verified that the data is
                  up-to-date. The endpoint returns the timestamp of when Adyen
                  received the request.
            /legalEntities/{id}/onboardingLinks:
              post:
                tags:
                  - Get
                  - Link
                  - To
                  - null
                  - Adyen-hosted
                  - Onboarding
                  - Page
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                summary: Get a link to an Adyen-hosted onboarding page
                description: >+
                  Returns a link to an Adyen-hosted onboarding page where you
                  need to redirect your user.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /legalEntities/{id}/pciQuestionnaires:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Details
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                summary: Get PCI questionnaire details
                description: Get a list of signed PCI questionnaires.
            /legalEntities/{id}/pciQuestionnaires/generatePciTemplates:
              post:
                tags:
                  - Generate
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                summary: Generate PCI questionnaire
                description: >-
                  Generates the required PCI questionnaires based on the user's
                  [salesChannel](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/businessLines__reqParam_salesChannels).
            /legalEntities/{id}/pciQuestionnaires/signPciTemplates:
              post:
                tags:
                  - Sign
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                summary: Sign PCI questionnaire
                description: Signs the required PCI questionnaire.
            /legalEntities/{id}/pciQuestionnaires/{pciid}:
              get:
                tags:
                  - Get
                  - Questionnaires
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                summary: Get PCI questionnaire
                description: Returns the signed PCI questionnaire.
            /legalEntities/{id}/termsOfService:
              post:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Document
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                summary: Get Terms of Service document
                description: Returns the Terms of Service document for a legal entity.
            /legalEntities/{id}/termsOfService/{termsofservicedocumentid}:
              patch:
                tags:
                  - Accept
                  - Terms
                  - Of
                  - Services
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                summary: Accept Terms of Service
                description: Accepts Terms of Service.
            /legalEntities/{id}/termsOfServiceAcceptanceInfos:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Information
                  - For
                  - Legal
                  - Entities
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                summary: Get Terms of Service information for a legal entity
                description: Returns Terms of Service information for a legal entity.
            /legalEntities/{id}/termsOfServiceStatus:
              get:
                tags:
                  - Get
                  - Terms
                  - Of
                  - Services
                  - Status
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                summary: Get Terms of Service status
                description: >-
                  Returns the required types of Terms of Service that need to be
                  accepted by a legal entity.
            /themes:
              get:
                tags:
                  - Get
                  - Lists
                  - Of
                  - Hosted
                  - Onboarding
                  - Page
                  - Themes
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get a list of hosted onboarding page themes
                description: >+
                  Returns a list of hosted onboarding page themes.


                  >If you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /themes/{id}:
              get:
                tags:
                  - Get
                  - null
                  - Onboarding
                  - Link
                  - Theme
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                summary: Get an onboarding link theme
                description: >+
                  Returns the details of the theme identified in the path.>If
                  you are using hosted onboarding and just beginning your
                  integration, use v3 for your API requests. Otherwise, use v2.

            /transferInstruments:
              post:
                tags:
                  - Create
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Create a transfer instrument
                description: >-
                  Creates a transfer instrument. 


                  A transfer instrument is a bank account that a legal entity
                  owns. Adyen performs verification checks on the transfer
                  instrument as required by payment industry regulations. We
                  inform you of the verification results through webhooks or API
                  responses.


                  When the transfer instrument passes the verification checks,
                  you can start sending funds from the balance platform to the
                  transfer instrument (such as payouts).
            /transferInstruments/{id}:
              delete:
                tags:
                  - Delete
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Delete a transfer instrument
                description: Deletes a transfer instrument.
              get:
                tags:
                  - Get
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Get a transfer instrument
                description: Returns the details of a transfer instrument.
              patch:
                tags:
                  - Update
                  - Transfers
                  - Instruments
                  - Lines
                  - Identifiers
                  - Documents
                  - Entities
                  - Business
                  - Checks
                  - Verification
                  - Errors
                  - Confirm
                  - Data
                  - Reviews
                  - Onboarding
                  - Links
                  - PCI
                  - Questionnaires
                  - Generate
                  - Templates
                  - Sign
                  - Pciid
                  - Terms
                  - Of
                  - Services
                  - Terms Of Service Documents
                  - Acceptance
                  - Information
                  - Status
                  - Themes
                  - Instruments
                summary: Update a transfer instrument
                description: null
    overlays:
      - type: APIs.io Search
        url: overlays/legal-entity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/legal-entity-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-legal-entity-api
  - name: Adyen Payouts API
    description: >-
      A set of API endpoints that allow you to store payout details, confirm, or
      decline a payout.\n\nFor more information, refer to [Online
      payouts](https://docs.adyen.com/online-payments/online-payouts).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/online-payments/online-payouts
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/online-payments/online-payouts
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Adyen Payout API
          tags:
            - name: Initialization
            - name: Reviewing
            - name: Instant payouts
          paths:
            /confirmThirdParty:
              post:
                tags:
                  - Confirm
                  - Payouts
                  - Third
                  - Party
                summary: Confirm a payout
                description: |-
                  Confirms a previously submitted payout.

                  To cancel a payout, use the `/declineThirdParty` endpoint.
            /declineThirdParty:
              post:
                tags:
                  - Cancel
                  - Payouts
                  - Third
                  - Party
                summary: Cancel a payout
                description: >-
                  Cancels a previously submitted payout.


                  To confirm and send a payout, use the `/confirmThirdParty`
                  endpoint.
            /payout:
              post:
                tags:
                  - Make
                  - null
                  - Instant
                  - Cards
                  - Payouts
                  - Third
                  - Party
                  - Payouts
                summary: Make an instant card payout
                description: >-
                  With this call, you can pay out to your customers, and funds
                  will be made available within 30 minutes on the cardholder's
                  bank account (this is dependent on whether the issuer supports
                  this functionality). Instant card payouts are only supported
                  for Visa and Mastercard cards.
            /storeDetail:
              post:
                tags:
                  - Store
                  - Payouts
                  - Details
                  - Third
                  - Party
                  - Payouts
                  - Detail
                summary: Store payout details
                description: >-
                  Stores payment details under the `PAYOUT` recurring contract.
                  These payment details can be used later to submit a payout via
                  the `/submitThirdParty` call.
            /storeDetailAndSubmitThirdParty:
              post:
                tags:
                  - Store
                  - Details
                  - And
                  - Submit
                  - Payouts
                  - Third
                  - Party
                  - Payouts
                  - Detail
                  - And
                  - Submit
                summary: Store details and submit a payout
                description: >-
                  Submits a payout and stores its details for subsequent
                  payouts.


                  The submitted payout must be confirmed or declined either by a
                  reviewer or via `/confirmThirdParty` or `/declineThirdParty`
                  calls.
            /submitThirdParty:
              post:
                tags:
                  - Submit
                  - Payouts
                  - Third
                  - Party
                  - Payouts
                  - Detail
                  - And
                  - Submit
                summary: Submit a payout
                description: >-
                  Submits a payout using the previously stored payment details.
                  To store payment details, use the `/storeDetail` API call.


                  The submitted payout must be confirmed or declined either by a
                  reviewer or via `/confirmThirdPar
    overlays:
      - type: APIs.io Search
        url: overlays/payouts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payouts-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-payouts-api
  - name: iot
    description: >-
      <fullname>IoT</fullname> <p>IoT provides secure, bi-directional
      communication between Internet-connected devices (such as sensors,
      actuators, embedded devices, or smart appliances) and the Amazon Web
      Services cloud. You can discover your custom IoT-Data endpoint to
      communicate with, configure rules for data processing and integration with
      other services, organize resources associated with each device (Registry),
      configure logging, and create and manage policies and credentials to
      authenticate devices.</p> <p>The service endpoints that expose this API
      are listed in <a
      href="https://docs.aws.amazon.com/general/latest/gr/iot-core.html">Amazon
      Web Services IoT Core Endpoints and Quotas</a>. You must use the endpoint
      for the region that has the resources you want to access.</p> <p>The
      service name used by <a
      href="https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html">Amazon
      Web Services Signature Version 4</a> to sign the request is:
      <i>execute-api</i>.</p> <p>For more information about how IoT works, see
      the <a
      href="https://docs.aws.amazon.com/iot/latest/developerguide/aws-iot-how-it-works.html">Developer
      Guide</a>.</p> <p>For information about how to use the credentials
      provider for IoT, see <a
      href="https://docs.aws.amazon.com/iot/latest/developerguide/authorizing-direct-aws.html">Authorizing
      Direct Calls to Amazon Web Services Services</a>.</p>
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
            title: iot
          paths:
            /accept-certificate-transfer/{certificateId}:
              PATCH:
                summary: AcceptCertificateTransfer
                description: >-
                  <p>Accepts a pending certificate transfer. The default state
                  of the certificate is INACTIVE.</p> <p>To check for pending
                  certificate transfers, call <a>ListCertificates</a> to
                  enumerate your certificates.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AcceptCertificateTransfer</a>
                  action.</p>
                tags:
                  - Accept
                  - Certificates
                  - Transfers
                  - Identifiers
            /billing-groups/addThingToBillingGroup:
              PUT:
                summary: AddThingToBillingGroup
                description: >-
                  <p>Adds a thing to a billing group.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AddThingToBillingGroup</a>
                  action.</p>
                tags:
                  - Add
                  - Things
                  - To
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
            /thing-groups/addThingToThingGroup:
              PUT:
                summary: AddThingToThingGroup
                description: >-
                  <p>Adds a thing to a thing group.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AddThingToThingGroup</a>
                  action.</p>
                tags:
                  - Add
                  - Things
                  - To
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
            /jobs/{jobId}/targets:
              POST:
                summary: AssociateTargetsWithJob
                description: >-
                  <p>Associates a group with a continuous job. The following
                  criteria must be met: </p> <ul> <li> <p>The job must have been
                  created with the <code>targetSelection</code> field set to
                  "CONTINUOUS".</p> </li> <li> <p>The job status must currently
                  be "IN_PROGRESS".</p> </li> <li> <p>The total number of
                  targets associated with a job must not exceed 100.</p> </li>
                  </ul> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">AssociateTargetsWithJob</a>
                  action.</p>
                tags:
                  - Associate
                  - Targets
                  - With
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
            /target-policies/{policyName}:
              POST:
                summary: DetachPolicy
                description: >-
                  <p>Detaches a policy from the specified target.</p> <note>
                  <p>Because of the distributed nature of Amazon Web Services,
                  it can take up to five minutes after a policy is detached
                  before it's ready to be deleted.</p> </note> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DetachPolicy</a>
                  action.</p>
                tags:
                  - Detach
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
            /principal-policies/{policyName}:
              DELETE:
                summary: DetachPrincipalPolicy
                description: >-
                  <p>Removes the specified policy from the specified
                  certificate.</p> <p> <b>Note:</b> This action is deprecated
                  and works as expected for backward compatibility, but we won't
                  add enhancements. Use <a>DetachPolicy</a> instead.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DetachPrincipalPolicy</a>
                  action.</p>
                tags:
                  - Detach
                  - Principals
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
            /security-profiles/{securityProfileName}/targets:
              GET:
                summary: ListTargetsForSecurityProfile
                description: >-
                  <p>Lists the targets (thing groups) associated with a given
                  Device Defender security profile.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListTargetsForSecurityProfile</a>
                  action.</p>
                tags:
                  - Lists
                  - Targets
                  - For
                  - Security
                  - Profiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
            /things/{thingName}/principals:
              GET:
                summary: ListThingPrincipals
                description: >-
                  <p>Lists the principals associated with the specified thing. A
                  principal can be X.509 certificates, IAM users, groups, and
                  roles, Amazon Cognito identities or federated identities.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingPrincipals</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Principals
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
            /audit/mitigationactions/tasks/{taskId}/cancel:
              PUT:
                summary: CancelAuditMitigationActionsTask
                description: >-
                  <p>Cancels a mitigation action task that is in progress. If
                  the task is not in progress, an InvalidRequestException
                  occurs.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelAuditMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Cancel
                  - Audit
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /audit/tasks/{taskId}/cancel:
              PUT:
                summary: CancelAuditTask
                description: >-
                  <p>Cancels an audit that is in progress. The audit can be
                  either scheduled or on demand. If the audit isn't in progress,
                  an "InvalidRequestException" occurs.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelAuditTask</a>
                  action.</p>
                tags:
                  - Cancel
                  - Audit
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /cancel-certificate-transfer/{certificateId}:
              PATCH:
                summary: CancelCertificateTransfer
                description: >-
                  <p>Cancels a pending transfer for the specified
                  certificate.</p> <p> <b>Note</b> Only the transfer source
                  account can use this operation to cancel a transfer. (Transfer
                  destinations can use <a>RejectCertificateTransfer</a>
                  instead.) After transfer, IoT returns the certificate to the
                  source account in the INACTIVE state. After the destination
                  account has accepted the transfer, the transfer cannot be
                  cancelled.</p> <p>After a certificate transfer is cancelled,
                  the status of the certificate changes from PENDING_TRANSFER to
                  INACTIVE.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelCertificateTransfer</a>
                  action.</p>
                tags:
                  - Cancel
                  - Certificates
                  - Transfers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /detect/mitigationactions/tasks/{taskId}/cancel:
              PUT:
                summary: CancelDetectMitigationActionsTask
                description: >-
                  <p> Cancels a Device Defender ML Detect mitigation action.
                  </p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelDetectMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Cancel
                  - Detect
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /jobs/{jobId}/cancel:
              PUT:
                summary: CancelJob
                description: >-
                  <p>Cancels a job.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelJob</a>
                  action.</p>
                tags:
                  - Cancel
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
            /things/{thingName}/jobs/{jobId}/cancel:
              PUT:
                summary: CancelJobExecution
                description: >-
                  <p>Cancels the execution of a job for a given thing.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CancelJobExecution</a>
                  action.</p>
                tags:
                  - Cancel
                  - Jobs
                  - Execution
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
            /default-authorizer:
              POST:
                summary: SetDefaultAuthorizer
                description: >-
                  <p>Sets the default authorizer. This will be used if a
                  websocket connection is made without specifying an
                  authorizer.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetDefaultAuthorizer</a>
                  action.</p>
                tags:
                  - Sets
                  - Default
                  - Authorizer
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
            /confirmdestination/{confirmationToken+}:
              GET:
                summary: ConfirmTopicRuleDestination
                description: >-
                  <p>Confirms a topic rule destination. When you create a rule
                  requiring a destination, IoT sends a confirmation message to
                  the endpoint or base address you specify. The message includes
                  a token which you pass back when calling
                  <code>ConfirmTopicRuleDestination</code> to confirm that you
                  own or have access to the endpoint.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ConfirmTopicRuleDestination</a>
                  action.</p>
                tags:
                  - Confirm
                  - Topics
                  - Rules
                  - Destinations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
            /audit/suppressions/create:
              POST:
                summary: CreateAuditSuppression
                description: >-
                  <p> Creates a Device Defender audit suppression. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CreateAuditSuppression</a>
                  action.</p>
                tags:
                  - Create
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
            /authorizer/{authorizerName}:
              PUT:
                summary: UpdateAuthorizer
                description: >-
                  <p>Updates an authorizer.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateAuthorizer</a>
                  action.</p>
                tags:
                  - Update
                  - Authorizer
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
            /billing-groups/{billingGroupName}:
              PATCH:
                summary: UpdateBillingGroup
                description: >-
                  <p>Updates information about the billing group.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateBillingGroup</a>
                  action.</p>
                tags:
                  - Update
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
            /certificates:
              GET:
                summary: ListCertificates
                description: >-
                  <p>Lists the certificates registered in your Amazon Web
                  Services account.</p> <p>The results are paginated with a
                  default page size of 25. You can use the returned marker to
                  retrieve additional results.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCertificates</a>
                  action.</p>
                tags:
                  - Lists
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
            /certificate-providers/{certificateProviderName}:
              PUT:
                summary: UpdateCertificateProvider
                description: >-
                  <p>Updates a certificate provider.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCertificateProvider</a>
                  action. </p>
                tags:
                  - Update
                  - Certificates
                  - Providers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
            /custom-metric/{metricName}:
              PATCH:
                summary: UpdateCustomMetric
                description: >-
                  <p>Updates a Device Defender detect custom metric. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCustomMetric</a>
                  action.</p>
                tags:
                  - Update
                  - Custom
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
            /dimensions/{name}:
              PATCH:
                summary: UpdateDimension
                description: >-
                  <p>Updates the definition for a dimension. You cannot change
                  the type of a dimension after it is created (you can delete it
                  and recreate it).</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateDimension</a>
                  action.</p>
                tags:
                  - Update
                  - Dimensions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
            /domainConfigurations/{domainConfigurationName}:
              PUT:
                summary: UpdateDomainConfiguration
                description: >-
                  <p>Updates values stored in the domain configuration. Domain
                  configurations for default endpoints can't be updated.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateDomainConfiguration</a>
                  action.</p>
                tags:
                  - Update
                  - Domains
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /dynamic-thing-groups/{thingGroupName}:
              PATCH:
                summary: UpdateDynamicThingGroup
                description: >-
                  <p>Updates a dynamic thing group.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateDynamicThingGroup</a>
                  action.</p>
                tags:
                  - Update
                  - Dynamic
                  - Things
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /fleet-metric/{metricName}:
              PATCH:
                summary: UpdateFleetMetric
                description: >-
                  <p>Updates the data for a fleet metric.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateFleetMetric</a>
                  action.</p>
                tags:
                  - Update
                  - Fleets
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /jobs/{jobId}:
              PATCH:
                summary: UpdateJob
                description: >-
                  <p>Updates supported fields of the specified job.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateJob</a>
                  action.</p>
                tags:
                  - Update
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
            /job-templates/{jobTemplateId}:
              GET:
                summary: DescribeJobTemplate
                description: <p>Returns information about a job template.</p>
                tags:
                  - Describe
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
            /keys-and-certificate:
              POST:
                summary: CreateKeysAndCertificate
                description: >-
                  <p>Creates a 2048-bit RSA key pair and issues an X.509
                  certificate using the issued public key. You can also call
                  <code>CreateKeysAndCertificate</code> over MQTT from a device,
                  for more information, see <a
                  href="https://docs.aws.amazon.com/iot/latest/developerguide/provision-wo-cert.html#provision-mqtt-api">Provisioning
                  MQTT API</a>.</p> <p> <b>Note</b> This is the only time IoT
                  issues the private key for this certificate, so it is
                  important to keep it in a secure location.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CreateKeysAndCertificate</a>
                  action.</p>
                tags:
                  - Create
                  - Keys
                  - And
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
            /mitigationactions/actions/{actionName}:
              PATCH:
                summary: UpdateMitigationAction
                description: >-
                  <p>Updates the definition for the specified mitigation
                  action.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateMitigationAction</a>
                  action.</p>
                tags:
                  - Update
                  - Mitigation
                  - Actions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
            /otaUpdates/{otaUpdateId}:
              GET:
                summary: GetOTAUpdate
                description: >-
                  <p>Gets an OTA update.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetOTAUpdate</a>
                  action.</p>
                tags:
                  - Get
                  - Update
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
            /packages/{packageName}:
              PATCH:
                summary: UpdatePackage
                description: >-
                  <p>Updates the supported fields for a specific software
                  package.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdatePackage</a>
                  and <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetIndexingConfiguration</a>
                  actions.</p>
                tags:
                  - Update
                  - Packages
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
            /packages/{packageName}/versions/{versionName}:
              PATCH:
                summary: UpdatePackageVersion
                description: >-
                  <p>Updates the supported fields for a specific package
                  version.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdatePackageVersion</a>
                  and <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetIndexingConfiguration</a>
                  actions.</p>
                tags:
                  - Update
                  - Packages
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
            /policies/{policyName}:
              GET:
                summary: GetPolicy
                description: >-
                  <p>Gets information about the specified policy with the policy
                  document of the default version.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetPolicy</a>
                  action.</p>
                tags:
                  - Get
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
            /policies/{policyName}/version:
              GET:
                summary: ListPolicyVersions
                description: >-
                  <p>Lists the versions of the specified policy and identifies
                  the default version.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPolicyVersions</a>
                  action.</p>
                tags:
                  - Lists
                  - Policies
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
            /provisioning-templates/{templateName}/provisioning-claim:
              POST:
                summary: CreateProvisioningClaim
                description: >-
                  <p>Creates a provisioning claim.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">CreateProvisioningClaim</a>
                  action.</p>
                tags:
                  - Create
                  - Provisioning
                  - Claim
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
            /provisioning-templates:
              GET:
                summary: ListProvisioningTemplates
                description: >-
                  <p>Lists the provisioning templates in your Amazon Web
                  Services account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListProvisioningTemplates</a>
                  action.</p>
                tags:
                  - Lists
                  - Provisioning
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
            /provisioning-templates/{templateName}/versions:
              GET:
                summary: ListProvisioningTemplateVersions
                description: >-
                  <p>A list of provisioning template versions.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListProvisioningTemplateVersions</a>
                  action.</p>
                tags:
                  - Lists
                  - Provisioning
                  - Templates
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
            /role-aliases/{roleAlias}:
              PUT:
                summary: UpdateRoleAlias
                description: >-
                  <p>Updates a role alias.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateRoleAlias</a>
                  action.</p>
                tags:
                  - Update
                  - Roles
                  - Alias
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /audit/scheduledaudits/{scheduledAuditName}:
              PATCH:
                summary: UpdateScheduledAudit
                description: >-
                  <p>Updates a scheduled audit, including which checks are
                  performed and how often the audit takes place.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateScheduledAudit</a>
                  action.</p>
                tags:
                  - Update
                  - Scheduled
                  - Audit
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /security-profiles/{securityProfileName}:
              PATCH:
                summary: UpdateSecurityProfile
                description: >-
                  <p>Updates a Device Defender security profile.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateSecurityProfile</a>
                  action.</p>
                tags:
                  - Update
                  - Security
                  - Profiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /streams/{streamId}:
              PUT:
                summary: UpdateStream
                description: >-
                  <p>Updates an existing stream. The stream version will be
                  incremented by one.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateStream</a>
                  action.</p>
                tags:
                  - Update
                  - Stream
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /things/{thingName}:
              PATCH:
                summary: UpdateThing
                description: >-
                  <p>Updates the data for a thing.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateThing</a>
                  action.</p>
                tags:
                  - Update
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /thing-groups/{thingGroupName}:
              PATCH:
                summary: UpdateThingGroup
                description: >-
                  <p>Update a thing group.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateThingGroup</a>
                  action.</p>
                tags:
                  - Update
                  - Things
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
            /thing-types/{thingTypeName}:
              GET:
                summary: DescribeThingType
                description: >-
                  <p>Gets information about the specified thing type.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeThingType</a>
                  action.</p>
                tags:
                  - Describe
                  - Things
                  - Types
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
            /rules/{ruleName}:
              PATCH:
                summary: ReplaceTopicRule
                description: >-
                  <p>Replaces the rule. You must specify all parameters for the
                  new rule. Creating rules is an administrator-level action. Any
                  user who has permission to create rules will be able to access
                  data processed by the rule.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ReplaceTopicRule</a>
                  action.</p>
                tags:
                  - Replace
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
            /destinations:
              PATCH:
                summary: UpdateTopicRuleDestination
                description: >-
                  <p>Updates a topic rule destination. You use this to change
                  the status, endpoint URL, or confirmation URL of the
                  destination.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateTopicRuleDestination</a>
                  action.</p>
                tags:
                  - Update
                  - Topics
                  - Rules
                  - Destinations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
            /audit/configuration:
              PATCH:
                summary: UpdateAccountAuditConfiguration
                description: >-
                  <p>Configures or reconfigures the Device Defender audit
                  settings for this account. Settings include how audit
                  notifications are sent and which audit checks are enabled or
                  disabled.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateAccountAuditConfiguration</a>
                  action.</p>
                tags:
                  - Update
                  - Account
                  - Audit
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
            /audit/suppressions/delete:
              POST:
                summary: DeleteAuditSuppression
                description: >-
                  <p> Deletes a Device Defender audit suppression. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DeleteAuditSuppression</a>
                  action.</p>
                tags:
                  - Delete
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
            /cacertificate/{caCertificateId}:
              PUT:
                summary: UpdateCACertificate
                description: >-
                  <p>Updates a registered CA certificate.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCACertificate</a>
                  action.</p>
                tags:
                  - Update
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
            /certificates/{certificateId}:
              PUT:
                summary: UpdateCertificate
                description: >-
                  <p>Updates the status of the specified certificate. This
                  operation is idempotent.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateCertificate</a>
                  action.</p> <p>Certificates must be in the ACTIVE state to
                  authenticate devices that use a certificate to connect to
                  IoT.</p> <p>Within a few minutes of updating a certificate
                  from the ACTIVE state to any other state, IoT disconnects all
                  devices that used that certificate to connect. Devices cannot
                  use a certificate that is not in the ACTIVE state to
                  reconnect.</p>
                tags:
                  - Update
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
            /things/{thingName}/jobs/{jobId}/executionNumber/{executionNumber}:
              DELETE:
                summary: DeleteJobExecution
                description: >-
                  <p>Deletes a job execution.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DeleteJobExecution</a>
                  action.</p>
                tags:
                  - Delete
                  - Jobs
                  - Execution
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
            /policies/{policyName}/version/{policyVersionId}:
              PATCH:
                summary: SetDefaultPolicyVersion
                description: >-
                  <p>Sets the specified version of the specified policy as the
                  policy's default (operative) version. This action affects all
                  certificates to which the policy is attached. To list the
                  principals the policy is attached to, use the
                  <a>ListPrincipalPolicies</a> action.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetDefaultPolicyVersion</a>
                  action.</p>
                tags:
                  - Sets
                  - Default
                  - Policies
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
            /provisioning-templates/{templateName}:
              PATCH:
                summary: UpdateProvisioningTemplate
                description: >-
                  <p>Updates a provisioning template.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateProvisioningTemplate</a>
                  action.</p>
                tags:
                  - Update
                  - Provisioning
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
            /provisioning-templates/{templateName}/versions/{versionId}:
              GET:
                summary: DescribeProvisioningTemplateVersion
                description: >-
                  <p>Returns information about a provisioning template
                  version.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeProvisioningTemplateVersion</a>
                  action.</p>
                tags:
                  - Describe
                  - Provisioning
                  - Templates
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
            /registrationcode:
              GET:
                summary: GetRegistrationCode
                description: >-
                  <p>Gets a registration code used to register a CA certificate
                  with IoT.</p> <p>IoT will create a registration code as part
                  of this API call if the registration code doesn't exist or has
                  been deleted. If you already have a registration code, this
                  API call will return the same registration code.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetRegistrationCode</a>
                  action.</p>
                tags:
                  - Get
                  - Registrations
                  - Code
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
            /destinations/{arn+}:
              GET:
                summary: GetTopicRuleDestination
                description: >-
                  <p>Gets information about a topic rule destination.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetTopicRuleDestination</a>
                  action.</p>
                tags:
                  - Get
                  - Topics
                  - Rules
                  - Destinations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
            /v2LoggingLevel:
              POST:
                summary: SetV2LoggingLevel
                description: >-
                  <p>Sets the logging level.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetV2LoggingLevel</a>
                  action.</p>
                tags:
                  - Sets
                  - V2
                  - Logging
                  - Levels
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
            /thing-types/{thingTypeName}/deprecate:
              POST:
                summary: DeprecateThingType
                description: >-
                  <p>Deprecates a thing type. You can not associate new things
                  with deprecated thing type.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DeprecateThingType</a>
                  action.</p>
                tags:
                  - Deprecate
                  - Things
                  - Types
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
            /audit/findings/{findingId}:
              GET:
                summary: DescribeAuditFinding
                description: >-
                  <p>Gets information about a single audit finding. Properties
                  include the reason for noncompliance, the severity of the
                  issue, and the start time when the audit that returned the
                  finding.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeAuditFinding</a>
                  action.</p>
                tags:
                  - Describe
                  - Audit
                  - Findings
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
            /audit/mitigationactions/tasks/{taskId}:
              POST:
                summary: StartAuditMitigationActionsTask
                description: >-
                  <p>Starts a task that applies a set of mitigation actions to
                  the specified target.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartAuditMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Start
                  - Audit
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
            /audit/suppressions/describe:
              POST:
                summary: DescribeAuditSuppression
                description: >-
                  <p> Gets information about a Device Defender audit
                  suppression. </p>
                tags:
                  - Describe
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
            /audit/tasks/{taskId}:
              GET:
                summary: DescribeAuditTask
                description: >-
                  <p>Gets information about a Device Defender audit.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeAuditTask</a>
                  action.</p>
                tags:
                  - Describe
                  - Audit
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
            /detect/mitigationactions/tasks/{taskId}:
              PUT:
                summary: StartDetectMitigationActionsTask
                description: >-
                  <p> Starts a Device Defender ML Detect mitigation actions
                  task. </p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartDetectMitigationActionsTask</a>
                  action.</p>
                tags:
                  - Start
                  - Detect
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
            /endpoint:
              GET:
                summary: DescribeEndpoint
                description: >-
                  <p>Returns or creates a unique endpoint specific to the Amazon
                  Web Services account making the call.</p> <note> <p>The first
                  time <code>DescribeEndpoint</code> is called, an endpoint is
                  created. All subsequent calls to <code>DescribeEndpoint</code>
                  return the same endpoint.</p> </note> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeEndpoint</a>
                  action.</p>
                tags:
                  - Describe
                  - Endpoints
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
            /event-configurations:
              PATCH:
                summary: UpdateEventConfigurations
                description: >-
                  <p>Updates the event configurations.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateEventConfigurations</a>
                  action.</p>
                tags:
                  - Update
                  - Events
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /indices/{indexName}:
              GET:
                summary: DescribeIndex
                description: >-
                  <p>Describes a search index.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeIndex</a>
                  action.</p>
                tags:
                  - Describe
                  - Index
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /things/{thingName}/jobs/{jobId}:
              GET:
                summary: DescribeJobExecution
                description: >-
                  <p>Describes a job execution.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeJobExecution</a>
                  action.</p>
                tags:
                  - Describe
                  - Jobs
                  - Execution
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /managed-job-templates/{templateName}:
              GET:
                summary: DescribeManagedJobTemplate
                description: <p>View details of a managed job template.</p>
                tags:
                  - Describe
                  - Managed
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /thing-registration-tasks/{taskId}:
              GET:
                summary: DescribeThingRegistrationTask
                description: >-
                  <p>Describes a bulk thing provisioning task.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DescribeThingRegistrationTask</a>
                  action.</p>
                tags:
                  - Describe
                  - Things
                  - Registrations
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
            /rules/{ruleName}/disable:
              POST:
                summary: DisableTopicRule
                description: >-
                  <p>Disables the rule.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">DisableTopicRule</a>
                  action.</p>
                tags:
                  - Disable
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
            /rules/{ruleName}/enable:
              POST:
                summary: EnableTopicRule
                description: >-
                  <p>Enables the rule.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">EnableTopicRule</a>
                  action.</p>
                tags:
                  - Enable
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
            /behavior-model-training/summaries:
              GET:
                summary: GetBehaviorModelTrainingSummaries
                description: >-
                  <p> Returns a Device Defender's ML Detect Security Profile
                  training model's status. </p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetBehaviorModelTrainingSummaries</a>
                  action.</p>
                tags:
                  - Get
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
            /indices/buckets:
              POST:
                summary: GetBucketsAggregation
                description: >-
                  <p>Aggregates on indexed data with search queries pertaining
                  to particular fields. </p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetBucketsAggregation</a>
                  action.</p>
                tags:
                  - Get
                  - Buckets
                  - Aggregation
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
            /indices/cardinality:
              POST:
                summary: GetCardinality
                description: >-
                  <p>Returns the approximate count of unique values that match
                  the query.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetCardinality</a>
                  action.</p>
                tags:
                  - Get
                  - Cardinality
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
            /effective-policies:
              POST:
                summary: GetEffectivePolicies
                description: >-
                  <p>Gets a list of the policies that have an effect on the
                  authorization behavior of the specified device when it
                  connects to the IoT device gateway.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetEffectivePolicies</a>
                  action.</p>
                tags:
                  - Get
                  - Effective
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
            /indexing/config:
              POST:
                summary: UpdateIndexingConfiguration
                description: >-
                  <p>Updates the search configuration.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateIndexingConfiguration</a>
                  action.</p>
                tags:
                  - Update
                  - Indexing
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
            /jobs/{jobId}/job-document:
              GET:
                summary: GetJobDocument
                description: >-
                  <p>Gets a job document.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetJobDocument</a>
                  action.</p>
                tags:
                  - Get
                  - Jobs
                  - Document
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
            /loggingOptions:
              POST:
                summary: SetLoggingOptions
                description: >-
                  <p>Sets the logging options.</p> <p>NOTE: use of this command
                  is not recommended. Use <code>SetV2LoggingOptions</code>
                  instead.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetLoggingOptions</a>
                  action.</p>
                tags:
                  - Sets
                  - Logging
                  - Options
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
            /package-configuration:
              PATCH:
                summary: UpdatePackageConfiguration
                description: >-
                  <p>Updates the software package configuration.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdatePackageConfiguration</a>
                  and <a
                  href="https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_passrole.html">iam:PassRole</a>
                  actions.</p>
                tags:
                  - Update
                  - Packages
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
            /indices/percentiles:
              POST:
                summary: GetPercentiles
                description: >-
                  <p>Groups the aggregated values that match the query into
                  percentile groupings. The default percentile groupings are:
                  1,5,25,50,75,95,99, although you can specify your own when you
                  call <code>GetPercentiles</code>. This function returns a
                  value for each percentile group specified (or the default
                  percentile groupings). The percentile group "1" contains the
                  aggregated field value that occurs in approximately one
                  percent of the values that match the query. The percentile
                  group "5" contains the aggregated field value that occurs in
                  approximately five percent of the values that match the query,
                  and so on. The result is an approximation, the more values
                  that match the query, the more accurate the percentile
                  values.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetPercentiles</a>
                  action.</p>
                tags:
                  - Get
                  - Percentiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
            /indices/statistics:
              POST:
                summary: GetStatistics
                description: >-
                  <p>Returns the count, average, sum, minimum, maximum, sum of
                  squares, variance, and standard deviation for the specified
                  aggregated field. If the aggregation field is of type
                  <code>String</code>, only the count statistic is returned.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">GetStatistics</a>
                  action.</p>
                tags:
                  - Get
                  - Statistics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
            /v2LoggingOptions:
              POST:
                summary: SetV2LoggingOptions
                description: >-
                  <p>Sets the logging options for the V2 logging service.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SetV2LoggingOptions</a>
                  action.</p>
                tags:
                  - Sets
                  - V2
                  - Logging
                  - Options
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
            /active-violations:
              GET:
                summary: ListActiveViolations
                description: >-
                  <p>Lists the active violations for a given Device Defender
                  security profile.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListActiveViolations</a>
                  action.</p>
                tags:
                  - Lists
                  - Active
                  - Violations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
            /attached-policies/{target}:
              POST:
                summary: ListAttachedPolicies
                description: >-
                  <p>Lists the policies attached to the specified thing
                  group.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAttachedPolicies</a>
                  action.</p>
                tags:
                  - Lists
                  - Attached
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
            /audit/findings:
              POST:
                summary: ListAuditFindings
                description: >-
                  <p>Lists the findings (results) of a Device Defender audit or
                  of the audits performed during a specified time period.
                  (Findings are retained for 90 days.)</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditFindings</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Findings
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
            /audit/mitigationactions/executions:
              GET:
                summary: ListAuditMitigationActionsExecutions
                description: >-
                  <p>Gets the status of audit mitigation action tasks that were
                  executed.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditMitigationActionsExecutions</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Mitigation
                  - Actions
                  - Executions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
            /audit/mitigationactions/tasks:
              GET:
                summary: ListAuditMitigationActionsTasks
                description: >-
                  <p>Gets a list of audit mitigation action tasks that match the
                  specified filters.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditMitigationActionsTasks</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
            /audit/suppressions/list:
              POST:
                summary: ListAuditSuppressions
                description: >-
                  <p> Lists your Device Defender audit listings. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuditSuppressions</a>
                  action.</p>
                tags:
                  - Lists
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
            /audit/tasks:
              POST:
                summary: StartOnDemandAuditTask
                description: >-
                  <p>Starts an on-demand Device Defender audit.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartOnDemandAuditTask</a>
                  action.</p>
                tags:
                  - Start
                  - 'On'
                  - Demand
                  - Audit
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
            /authorizers/:
              GET:
                summary: ListAuthorizers
                description: >-
                  <p>Lists the authorizers registered in your account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListAuthorizers</a>
                  action.</p>
                tags:
                  - Lists
                  - Authorizers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
            /billing-groups:
              GET:
                summary: ListBillingGroups
                description: >-
                  <p>Lists the billing groups you have created.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListBillingGroups</a>
                  action.</p>
                tags:
                  - Lists
                  - Billing
                  - Groups
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
            /cacertificates:
              GET:
                summary: ListCACertificates
                description: >-
                  <p>Lists the CA certificates registered for your Amazon Web
                  Services account.</p> <p>The results are paginated with a
                  default page size of 25. You can use the returned marker to
                  retrieve additional results.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCACertificates</a>
                  action.</p>
                tags:
                  - Lists
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
            /certificate-providers/:
              GET:
                summary: ListCertificateProviders
                description: >-
                  <p>Lists all your certificate providers in your Amazon Web
                  Services account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCertificateProviders</a>
                  action. </p>
                tags:
                  - Lists
                  - Certificates
                  - Providers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
            /certificates-by-ca/{caCertificateId}:
              GET:
                summary: ListCertificatesByCA
                description: >-
                  <p>List the device certificates signed by the specified CA
                  certificate.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCertificatesByCA</a>
                  action.</p>
                tags:
                  - Lists
                  - Certificates
                  - By
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
            /custom-metrics:
              GET:
                summary: ListCustomMetrics
                description: >-
                  <p> Lists your Device Defender detect custom metrics. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListCustomMetrics</a>
                  action.</p>
                tags:
                  - Lists
                  - Custom
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
            /detect/mitigationactions/executions:
              GET:
                summary: ListDetectMitigationActionsExecutions
                description: >-
                  <p> Lists mitigation actions executions for a Device Defender
                  ML Detect Security Profile. </p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDetectMitigationActionsExecutions</a>
                  action.</p>
                tags:
                  - Lists
                  - Detect
                  - Mitigation
                  - Actions
                  - Executions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /detect/mitigationactions/tasks:
              GET:
                summary: ListDetectMitigationActionsTasks
                description: >-
                  <p> List of Device Defender ML Detect mitigation actions
                  tasks. </p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDetectMitigationActionsTasks</a>
                  action.</p>
                tags:
                  - Lists
                  - Detect
                  - Mitigation
                  - Actions
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /dimensions:
              GET:
                summary: ListDimensions
                description: >-
                  <p>List the set of dimensions that are defined for your Amazon
                  Web Services accounts.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDimensions</a>
                  action.</p>
                tags:
                  - Lists
                  - Dimensions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /domainConfigurations:
              GET:
                summary: ListDomainConfigurations
                description: >-
                  <p>Gets a list of domain configurations for the user. This
                  list is sorted alphabetically by domain configuration
                  name.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListDomainConfigurations</a>
                  action.</p>
                tags:
                  - Lists
                  - Domains
                  - Configurations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
            /fleet-metrics:
              GET:
                summary: ListFleetMetrics
                description: >-
                  <p>Lists all your fleet metrics. </p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListFleetMetrics</a>
                  action.</p>
                tags:
                  - Lists
                  - Fleets
                  - Metrics
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
            /indices:
              GET:
                summary: ListIndices
                description: >-
                  <p>Lists the search indices.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListIndices</a>
                  action.</p>
                tags:
                  - Lists
                  - Indices
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
            /jobs/{jobId}/things:
              GET:
                summary: ListJobExecutionsForJob
                description: >-
                  <p>Lists the job executions for a job.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobExecutionsForJob</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Executions
                  - For
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /things/{thingName}/jobs:
              GET:
                summary: ListJobExecutionsForThing
                description: >-
                  <p>Lists the job executions for the specified thing.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobExecutionsForThing</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Executions
                  - For
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /job-templates:
              GET:
                summary: ListJobTemplates
                description: >-
                  <p>Returns a list of job templates.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobTemplates</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /jobs:
              GET:
                summary: ListJobs
                description: >-
                  <p>Lists jobs.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListJobs</a>
                  action.</p>
                tags:
                  - Lists
                  - Jobs
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
            /managed-job-templates:
              GET:
                summary: ListManagedJobTemplates
                description: <p>Returns a list of managed job templates.</p>
                tags:
                  - Lists
                  - Managed
                  - Jobs
                  - Templates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
            /metric-values:
              GET:
                summary: ListMetricValues
                description: >-
                  <p>Lists the values reported for an IoT Device Defender metric
                  (device-side metric, cloud-side metric, or custom metric) by
                  the given thing during the specified time period.</p>
                tags:
                  - Lists
                  - Metrics
                  - Values
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
            /mitigationactions/actions:
              GET:
                summary: ListMitigationActions
                description: >-
                  <p>Gets a list of all mitigation actions that match the
                  specified filter criteria.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListMitigationActions</a>
                  action.</p>
                tags:
                  - Lists
                  - Mitigation
                  - Actions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
            /otaUpdates:
              GET:
                summary: ListOTAUpdates
                description: >-
                  <p>Lists OTA updates.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListOTAUpdates</a>
                  action.</p>
                tags:
                  - Lists
                  - Updates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
            /certificates-out-going:
              GET:
                summary: ListOutgoingCertificates
                description: >-
                  <p>Lists certificates that are being transferred but not yet
                  accepted.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListOutgoingCertificates</a>
                  action.</p>
                tags:
                  - Lists
                  - Outgoing
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
            /packages/{packageName}/versions:
              GET:
                summary: ListPackageVersions
                description: >-
                  <p>Lists the software package versions associated to the
                  account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPackageVersions</a>
                  action.</p>
                tags:
                  - Lists
                  - Packages
                  - Versions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
            /packages:
              GET:
                summary: ListPackages
                description: >-
                  <p>Lists the software packages associated to the account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPackages</a>
                  action.</p>
                tags:
                  - Lists
                  - Packages
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
            /policies:
              GET:
                summary: ListPolicies
                description: >-
                  <p>Lists your policies.</p> <p>Requires permission to access
                  the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPolicies</a>
                  action.</p>
                tags:
                  - Lists
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
            /policy-principals:
              GET:
                summary: ListPolicyPrincipals
                description: >-
                  <p>Lists the principals associated with the specified
                  policy.</p> <p> <b>Note:</b> This action is deprecated and
                  works as expected for backward compatibility, but we won't add
                  enhancements. Use <a>ListTargetsForPolicy</a> instead.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPolicyPrincipals</a>
                  action.</p>
                tags:
                  - Lists
                  - Policies
                  - Principals
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
            /principal-policies:
              GET:
                summary: ListPrincipalPolicies
                description: >-
                  <p>Lists the policies attached to the specified principal. If
                  you use an Cognito identity, the ID must be in <a
                  href="https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/API_GetCredentialsForIdentity.html#API_GetCredentialsForIdentity_RequestSyntax">AmazonCognito
                  Identity format</a>.</p> <p> <b>Note:</b> This action is
                  deprecated and works as expected for backward compatibility,
                  but we won't add enhancements. Use <a>ListAttachedPolicies</a>
                  instead.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPrincipalPolicies</a>
                  action.</p>
                tags:
                  - Lists
                  - Principals
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
            /principals/things:
              GET:
                summary: ListPrincipalThings
                description: >-
                  <p>Lists the things associated with the specified principal. A
                  principal can be X.509 certificates, IAM users, groups, and
                  roles, Amazon Cognito identities or federated identities. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListPrincipalThings</a>
                  action.</p>
                tags:
                  - Lists
                  - Principals
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
            /audit/relatedResources:
              GET:
                summary: ListRelatedResourcesForAuditFinding
                description: >-
                  <p>The related resources of an Audit finding. The following
                  resources can be returned from calling this API:</p> <ul> <li>
                  <p>DEVICE_CERTIFICATE</p> </li> <li> <p>CA_CERTIFICATE</p>
                  </li> <li> <p>IOT_POLICY</p> </li> <li>
                  <p>COGNITO_IDENTITY_POOL</p> </li> <li> <p>CLIENT_ID</p> </li>
                  <li> <p>ACCOUNT_SETTINGS</p> </li> <li> <p>ROLE_ALIAS</p>
                  </li> <li> <p>IAM_ROLE</p> </li> <li>
                  <p>ISSUER_CERTIFICATE</p> </li> </ul> <note> <p>This API is
                  similar to DescribeAuditFinding's <a
                  href="https://docs.aws.amazon.com/iot/latest/apireference/API_DescribeAuditFinding.html">RelatedResources</a>
                  but provides pagination and is not limited to 10 resources.
                  When calling <a
                  href="https://docs.aws.amazon.com/iot/latest/apireference/API_DescribeAuditFinding.html">DescribeAuditFinding</a>
                  for the intermediate CA revoked for active device certificates
                  check, RelatedResources will not be populated. You must use
                  this API, ListRelatedResourcesForAuditFinding, to list the
                  certificates.</p> </note>
                tags:
                  - Lists
                  - Related
                  - Resources
                  - For
                  - Audit
                  - Findings
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
            /role-aliases:
              GET:
                summary: ListRoleAliases
                description: >-
                  <p>Lists the role aliases registered in your account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListRoleAliases</a>
                  action.</p>
                tags:
                  - Lists
                  - Roles
                  - Aliases
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
            /audit/scheduledaudits:
              GET:
                summary: ListScheduledAudits
                description: >-
                  <p>Lists all of your scheduled audits.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListScheduledAudits</a>
                  action.</p>
                tags:
                  - Lists
                  - Scheduled
                  - Audits
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
            /security-profiles:
              GET:
                summary: ListSecurityProfiles
                description: >-
                  <p>Lists the Device Defender security profiles you've created.
                  You can filter security profiles by dimension or custom
                  metric.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListSecurityProfiles</a>
                  action.</p> <note> <p> <code>dimensionName</code> and
                  <code>metricName</code> cannot be used in the same
                  request.</p> </note>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
            /security-profiles-for-target:
              GET:
                summary: ListSecurityProfilesForTarget
                description: >-
                  <p>Lists the Device Defender security profiles attached to a
                  target (thing group).</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListSecurityProfilesForTarget</a>
                  action.</p>
                tags:
                  - Lists
                  - Security
                  - Profiles
                  - For
                  - Target
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
            /streams:
              GET:
                summary: ListStreams
                description: >-
                  <p>Lists all of the streams in your Amazon Web Services
                  account.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListStreams</a>
                  action.</p>
                tags:
                  - Lists
                  - Streams
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
            /tags:
              POST:
                summary: TagResource
                description: >-
                  <p>Adds to or modifies the tags of the given resource. Tags
                  are metadata which can be used to manage a resource.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TagResource</a>
                  action.</p>
                tags:
                  - Tags
                  - Resources
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /policy-targets/{policyName}:
              POST:
                summary: ListTargetsForPolicy
                description: >-
                  <p>List targets for the specified policy.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListTargetsForPolicy</a>
                  action.</p>
                tags:
                  - Lists
                  - Targets
                  - For
                  - Policies
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /thing-groups:
              GET:
                summary: ListThingGroups
                description: >-
                  <p>List the thing groups in your account.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingGroups</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Groups
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /things/{thingName}/thing-groups:
              GET:
                summary: ListThingGroupsForThing
                description: >-
                  <p>List the thing groups to which the specified thing
                  belongs.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingGroupsForThing</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Groups
                  - For
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
            /thing-registration-tasks/{taskId}/reports:
              GET:
                summary: ListThingRegistrationTaskReports
                description: <p>Information about the thing registration tasks.</p>
                tags:
                  - Lists
                  - Things
                  - Registrations
                  - Tasks
                  - Reports
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
            /thing-registration-tasks:
              POST:
                summary: StartThingRegistrationTask
                description: >-
                  <p>Creates a bulk thing provisioning task.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StartThingRegistrationTask</a>
                  action.</p>
                tags:
                  - Start
                  - Things
                  - Registrations
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
            /thing-types:
              GET:
                summary: ListThingTypes
                description: >-
                  <p>Lists the existing thing types.</p> <p>Requires permission
                  to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingTypes</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - Types
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /things:
              POST:
                summary: RegisterThing
                description: >-
                  <p>Provisions a thing in the device registry. RegisterThing
                  calls other IoT control plane APIs. These calls might exceed
                  your account level <a
                  href="https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html#limits_iot">
                  IoT Throttling Limits</a> and cause throttle errors. Please
                  contact <a
                  href="https://console.aws.amazon.com/support/home">Amazon Web
                  Services Customer Support</a> to raise your throttling limits
                  if necessary.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RegisterThing</a>
                  action.</p>
                tags:
                  - Register
                  - Things
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /billing-groups/{billingGroupName}/things:
              GET:
                summary: ListThingsInBillingGroup
                description: >-
                  <p>Lists the things you have added to the given billing
                  group.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingsInBillingGroup</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - In
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /thing-groups/{thingGroupName}/things:
              GET:
                summary: ListThingsInThingGroup
                description: >-
                  <p>Lists the things in the specified group.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListThingsInThingGroup</a>
                  action.</p>
                tags:
                  - Lists
                  - Things
                  - In
                  - Things
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
            /rules:
              GET:
                summary: ListTopicRules
                description: >-
                  <p>Lists the rules for the specific topic.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListTopicRules</a>
                  action.</p>
                tags:
                  - Lists
                  - Topics
                  - Rules
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
            /violation-events:
              GET:
                summary: ListViolationEvents
                description: >-
                  <p>Lists the Device Defender security profile violations
                  discovered during the given time period. You can use filters
                  to limit the results to those alerts issued for a particular
                  security profile, behavior, or thing (device).</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ListViolationEvents</a>
                  action.</p>
                tags:
                  - Lists
                  - Violations
                  - Events
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
            /violations/verification-state/{violationId}:
              POST:
                summary: PutVerificationStateOnViolation
                description: >-
                  <p>Set a verification state and provide a description of that
                  verification state on a violation (detect alarm).</p>
                tags:
                  - Put
                  - Verification
                  - States
                  - 'On'
                  - Violations
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
            /cacertificate:
              POST:
                summary: RegisterCACertificate
                description: >-
                  <p>Registers a CA certificate with Amazon Web Services IoT
                  Core. There is no limit to the number of CA certificates you
                  can register in your Amazon Web Services account. You can
                  register up to 10 CA certificates with the same <code>CA
                  subject field</code> per Amazon Web Services account.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RegisterCACertificate</a>
                  action.</p>
                tags:
                  - Register
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
            /certificate/register:
              POST:
                summary: RegisterCertificate
                description: >-
                  <p>Registers a device certificate with IoT in the same <a
                  href="https://docs.aws.amazon.com/iot/latest/apireference/API_CertificateDescription.html#iot-Type-CertificateDescription-certificateMode">certificate
                  mode</a> as the signing CA. If you have more than one CA
                  certificate that has the same subject field, you must specify
                  the CA certificate that was used to sign the device
                  certificate being registered.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RegisterCertificate</a>
                  action.</p>
                tags:
                  - Register
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
            /certificate/register-no-ca:
              POST:
                summary: RegisterCertificateWithoutCA
                description: >-
                  <p>Register a certificate that does not have a certificate
                  authority (CA). For supported certificates, consult <a
                  href="https://docs.aws.amazon.com/iot/latest/developerguide/x509-client-certs.html#x509-cert-algorithms">
                  Certificate signing algorithms supported by IoT</a>. </p>
                tags:
                  - Register
                  - Certificates
                  - Without
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
            /reject-certificate-transfer/{certificateId}:
              PATCH:
                summary: RejectCertificateTransfer
                description: >-
                  <p>Rejects a pending certificate transfer. After IoT rejects a
                  certificate transfer, the certificate status changes from
                  <b>PENDING_TRANSFER</b> to <b>INACTIVE</b>.</p> <p>To check
                  for pending certificate transfers, call
                  <a>ListCertificates</a> to enumerate your certificates.</p>
                  <p>This operation can only be called by the transfer
                  destination. After it is called, the certificate will be
                  returned to the source's account in the INACTIVE state.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RejectCertificateTransfer</a>
                  action.</p>
                tags:
                  - Reject
                  - Certificates
                  - Transfers
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
            /billing-groups/removeThingFromBillingGroup:
              PUT:
                summary: RemoveThingFromBillingGroup
                description: >-
                  <p>Removes the given thing from the billing group.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RemoveThingFromBillingGroup</a>
                  action.</p> <note> <p>This call is asynchronous. It might take
                  several seconds for the detachment to propagate.</p> </note>
                tags:
                  - Removes
                  - Things
                  - From
                  - Billing
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
            /thing-groups/removeThingFromThingGroup:
              PUT:
                summary: RemoveThingFromThingGroup
                description: >-
                  <p>Remove the specified thing from the specified group.</p>
                  <p>You must specify either a <code>thingGroupArn</code> or a
                  <code>thingGroupName</code> to identify the thing group and
                  either a <code>thingArn</code> or a <code>thingName</code> to
                  identify the thing to remove from the thing group. </p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">RemoveThingFromThingGroup</a>
                  action.</p>
                tags:
                  - Removes
                  - Things
                  - From
                  - Group
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
            /indices/search:
              POST:
                summary: SearchIndex
                description: >-
                  <p>The query search index.</p> <p>Requires permission to
                  access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">SearchIndex</a>
                  action.</p>
                tags:
                  - Search
                  - Index
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
            /thing-registration-tasks/{taskId}/cancel:
              PUT:
                summary: StopThingRegistrationTask
                description: >-
                  <p>Cancels a bulk thing provisioning task.</p> <p>Requires
                  permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">StopThingRegistrationTask</a>
                  action.</p>
                tags:
                  - Stop
                  - Things
                  - Registrations
                  - Tasks
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
            /test-authorization:
              POST:
                summary: TestAuthorization
                description: >-
                  <p>Tests if a specified principal is authorized to perform an
                  IoT action on a specified resource. Use this to test and debug
                  the authorization behavior of devices that connect to the IoT
                  device gateway.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TestAuthorization</a>
                  action.</p>
                tags:
                  - Tests
                  - Authorization
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
            /authorizer/{authorizerName}/test:
              POST:
                summary: TestInvokeAuthorizer
                description: >-
                  <p>Tests a custom authorization behavior by invoking a
                  specified custom authorizer. Use this to test and debug the
                  custom authorization behavior of devices that connect to the
                  IoT device gateway.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TestInvokeAuthorizer</a>
                  action.</p>
                tags:
                  - Tests
                  - Invoke
                  - Authorizer
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
            /transfer-certificate/{certificateId}:
              PATCH:
                summary: TransferCertificate
                description: >-
                  <p>Transfers the specified certificate to the specified Amazon
                  Web Services account.</p> <p>Requires permission to access the
                  <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">TransferCertificate</a>
                  action.</p> <p>You can cancel the transfer until it is
                  acknowledged by the recipient.</p> <p>No notification is sent
                  to the transfer destination's account. It is up to the caller
                  to notify the transfer target.</p> <p>The certificate being
                  transferred must not be in the ACTIVE state. You can use the
                  <a>UpdateCertificate</a> action to deactivate it.</p> <p>The
                  certificate must not have any policies attached to it. You can
                  use the <a>DetachPolicy</a> action to detach them.</p>
                tags:
                  - Transfers
                  - Certificates
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
            /untag:
              POST:
                summary: UntagResource
                description: >-
                  <p>Removes the given tags (metadata) from the resource.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UntagResource</a>
                  action.</p>
                tags:
                  - Untag
                  - Resources
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
            /audit/suppressions/update:
              PATCH:
                summary: UpdateAuditSuppression
                description: <p> Updates a Device Defender audit suppression. </p>
                tags:
                  - Update
                  - Audit
                  - Suppressions
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
            /thing-groups/updateThingGroupsForThing:
              PUT:
                summary: UpdateThingGroupsForThing
                description: >-
                  <p>Updates the groups to which the thing belongs.</p>
                  <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">UpdateThingGroupsForThing</a>
                  action.</p>
                tags:
                  - Update
                  - Things
                  - Groups
                  - For
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
            /security-profile-behaviors/validate:
              POST:
                summary: ValidateSecurityProfileBehaviors
                description: >-
                  <p>Validates a Device Defender security profile behaviors
                  specification.</p> <p>Requires permission to access the <a
                  href="https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions">ValidateSecurityProfileBehaviors</a>
                  a
                tags:
                  - Validate
                  - Security
                  - Profiles
                  - Behaviors
                  - Identifiers
                  - Things
                  - To
                  - Billing
                  - Group
                  - Targets
                  - Names
                  - Profiles
                  - Principals
                  - Cancel
                  - Jobs
                  - Jobs
                  - Default
                  - Authorizer
                  - Tokens
                  - Audit
                  - Suppressions
                  - Create
                  - Certificates
                  - Providers
                  - Dimensions
                  - Configurations
                  - Domains
                  - Configurations
                  - Templates
                  - Keys
                  - And
                  - Certificates
                  - Updates
                  - Ota
                  - Update
                  - Versions
                  - Versions
                  - Provisioning
                  - Claim
                  - Templates
                  - Alias
                  - Types
                  - Destinations
                  - Delete
                  - Execution
                  - Numbers
                  - Policies
                  - Registration Codes
                  - ARN
                  - Logging
                  - Levels
                  - Deprecate
                  - Describe
                  - Endpoints
                  - Events
                  - Disable
                  - Enable
                  - Behavior
                  - Models
                  - Training
                  - Summaries
                  - Indices
                  - Buckets
                  - Cardinality
                  - Effective
                  - Policies
                  - Indexing
                  - Configurations
                  - Document
                  - Options
                  - Packages
                  - Percentiles
                  - Statistics
                  - Active
                  - Violations
                  - Attached
                  - Target
                  - Findings
                  - Mitigation Actions
                  - Executions
                  - Tasks
                  - Lists
                  - Authorizers
                  - Groups
                  - Certificates
                  - Providers
                  - Custom
                  - Metrics
                  - Detect
                  - Fleets
                  - Things
                  - Managed
                  - Metrics
                  - Values
                  - Actions
                  - Out
                  - Going
                  - Packages
                  - Principals
                  - Resources
                  - Roles
                  - Aliases
                  - Scheduled Audits
                  - Security
                  - Profiles
                  - For
                  - Streams
                  - Tags
                  - Reports
                  - Registrations
                  - Types
                  - Rules
                  - Violations
                  - Events
                  - Certificates
                  - Register
                  - 'No'
                  - Ca
                  - From
                  - Search
                  - Tests
                  - Authorization
                  - Untag
                  - Behaviors
                  - Validate
    overlays:
      - type: APIs.io Search
        url: overlays/iot-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot
  - aid: stripe:stripe-climate-api
    name: Stripe Climate API
    description: >-
      Stripe Climate is the easiest way to help promising permanent carbon
      removal technologies launch and scale. Join a growing group of ambitious
      businesses that are changing the course of carbon removal.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/climate
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/climate
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Climate API
          paths:
            /v1/climate/orders:
              get:
                description: >-
                  <p>Lists all Climate order objects. The orders are returned
                  sorted by creation date, with the

                  most recently created orders appearing first.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
              post:
                description: >-
                  <p>Creates a Climate order object for a given Climate product.
                  The order will be processed immediately

                  after creation and payment will be deducted your Stripe
                  balance.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
            /v1/climate/orders/{order}:
              get:
                description: >-
                  <p>Retrieves the details of a Climate order object with the
                  given ID.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
              post:
                description: >-
                  <p>Updates the specified order by setting the values of the
                  parameters passed.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
            /v1/climate/orders/{order}/cancel:
              post:
                description: >-
                  <p>Cancels a Climate order. You can cancel an order within 30
                  days of creation. Stripe refunds the

                  reservation <code>amount_subtotal</code>, but not the
                  <code>amount_fees</code> for user-triggered cancellations.
                  Frontier

                  might cancel reservations if suppliers fail to deliver. If
                  Frontier cancels the reservation, Stripe

                  provides 90 days advance notice and refunds the
                  <code>amount_total</code>.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
            /v1/climate/products:
              get:
                description: <p>Lists all available Climate product objects.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
            /v1/climate/products/{product}:
              get:
                description: >-
                  <p>Retrieves the details of a Climate product with the given
                  ID.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
            /v1/climate/reservations:
              get:
                description: >-
                  <p>Lists all Climate order objects. The orders are returned
                  sorted by creation date, with the

                  most recently created orders appearing first.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
              post:
                description: >-
                  <p>Creates a Climate order object for a given Climate product.
                  The order will be processed immediately

                  after creation and payment will be deducted your Stripe
                  balance.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
            /v1/climate/reservations/{order}:
              get:
                description: >-
                  <p>Retrieves the details of a Climate order object with the
                  given ID.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
              post:
                description: >-
                  <p>Updates the specified order by setting the values of the
                  parameters passed.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
            /v1/climate/reservations/{order}/cancel:
              post:
                description: >-
                  <p>Cancels a Climate order. You can cancel an order within 30
                  days of creation. Stripe refunds the

                  reservation <code>amount_subtotal</code>, but not the
                  <code>amount_fees</code> for user-triggered cancellations.
                  Frontier

                  might cancel reservations if suppliers fail to deliver. If
                  Frontier cancels the reservation, Stripe

                  provides 90 days advance notice and refunds the
                  <code>amount_total</code>.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
            /v1/climate/reservations/{order}/confirm:
              post:
                description: >-
                  <p>Confirms a Climate order. When you confirm your order, we
                  immediately deduct the funds from your

                  Stripe balance.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
                  - Confirm
            /v1/climate/suppliers:
              get:
                description: <p>Lists all available Climate supplier objects.</p>
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
                  - Confirm
                  - Suppliers
            /v1/climate/suppliers/{supplier}:
              get:
                description: <p>Retrieves a Climate supplier o
                tags:
                  - V1
                  - Climate
                  - Orders
                  - Order
                  - Cancel
                  - Products
                  - Product
                  - Reservations
                  - Confirm
                  - Suppliers
                  - Suppli
    overlays:
      - type: APIs.io Search
        url: overlays/climate-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/climate-openapi-api-evangelist-ratings.yml
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
  - aid: stripe:stripe-setup-api
    name: Stripe Setup API
    description: >-
      Use the Setup Intents API to set up a payment method for future payments.
      It’s similar to a payment, but no charge is created. Set up a payment
      method for future payments now.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/payments/setup-intents
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/payments/setup-intents
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Setup API
          paths:
            /v1/setup_attempts:
              get:
                description: >-
                  <p>Returns a list of SetupAttempts that associate with a
                  provided SetupIntent.</p>
                tags:
                  - V1
                  - Setup_attempts
            /v1/setup_intents:
              get:
                description: <p>Returns a list of SetupIntents.</p>
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
              post:
                description: >-
                  <p>Creates a SetupIntent object.</p>


                  <p>After you create the SetupIntent, attach a payment method
                  and <a href="/docs/api/setup_intents/confirm">confirm</a>

                  it to collect any required permissions to charge the payment
                  method later.</p>
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
            /v1/setup_intents/{intent}:
              get:
                description: >-
                  <p>Retrieves the details of a SetupIntent that has previously
                  been created. </p>


                  <p>Client-side retrieval using a publishable key is allowed
                  when the <code>client_secret</code> is provided in the query
                  string. </p>


                  <p>When retrieved with a publishable key, only a subset of
                  properties will be returned. Please refer to the <a
                  href="#setup_intent_object">SetupIntent</a> object reference
                  for more details.</p>
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
                  - Intent
              post:
                description: <p>Updates a SetupIntent object.</p>
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
                  - Intent
            /v1/setup_intents/{intent}/cancel:
              post:
                description: >-
                  <p>You can cancel a SetupIntent object when it’s in one of
                  these statuses: <code>requires_payment_method</code>,
                  <code>requires_confirmation</code>, or
                  <code>requires_action</code>. </p>


                  <p>After you cancel it, setup is abandoned and any operations
                  on the SetupIntent fail with an error.</p>
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
                  - Intent
                  - Cancel
            /v1/setup_intents/{intent}/confirm:
              post:
                description: >-
                  <p>Confirm that your customer intends to set up the current or

                  provided payment method. For example, you would confirm a
                  SetupIntent

                  when a customer hits the “Save” button on a payment method
                  management

                  page on your website.</p>


                  <p>If the selected payment method does not require any
                  additional

                  steps from the customer, the SetupIntent will transition to
                  the

                  <code>succeeded</code> status.</p>


                  <p>Otherwise, it will transition to the
                  <code>requires_action</code> status and

                  suggest additional actions via <code>next_action</code>. If
                  setup fails,

                  the SetupIntent will transition to the

                  <code>requires_payment_method</code> status or the
                  <code>canceled</code> status if the

                  confirmation limit is reached.</p>
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
                  - Intent
                  - Cancel
                  - Confirm
            /v1/setup_intents/{intent}/verify_microdeposits:
              post:
                description: <p>Verifies microdeposits on a SetupIntent o
                tags:
                  - V1
                  - Setup_attempts
                  - Setup_intents
                  - Intent
                  - Cancel
                  - Confirm
                  - Verify_microdeposi
    overlays:
      - type: APIs.io Search
        url: overlays/setup-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/setup-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---