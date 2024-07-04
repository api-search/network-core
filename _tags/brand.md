---
name: Brand
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/brand.png
url: https://example.com/apis/brand.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Brand
apis:
  - aid: bigcommerce:catalog-brands
    name: Catalog - Brands
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
            title: Catalog - Brands
            version: ''
          tags:
            - name: Brands
            - name: Images
            - name: Metafields
            - name: Batch metafields
          paths:
            /catalog/brands:
              get:
                tags:
                  - Get
                  - All
                  - Brands
                  - Catalog
                  - Brands
                summary: Get All Brands
                description: >-
                  Returns a list of *Brands*. Optional filter parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Brand
                  - Catalog
                  - Brands
                summary: Create a Brand
                description: |-
                  Creates a *Brand*.

                  **Required Fields**
                  - name

                  **Read-Only Fields**
                  - id

                  **Limits**
                  - 30,000 brands per store limit
              delete:
                tags:
                  - Delete
                  - Brands
                  - Catalog
                  - Brands
                summary: Delete Brands
                description: |-
                  To delete brand objects, you must include a filter.

                  **Required Fields**
                   - name
              parameters:
                - null
            /catalog/brands/{brand_id}:
              get:
                tags:
                  - Get
                  - Brand
                  - Catalog
                  - Brands
                  - Brand_id
                summary: Get a Brand
                description: >-
                  Returns a single *Brand*. Optional filter parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Brand
                  - Catalog
                  - Brands
                  - Brand_id
                summary: Update a Brand
                description: |-
                  Updates a *Brand*.

                  **Required Fields**
                  - None

                  **Read-Only Fields**
                  - id

                  To update a *Brand Image*, send a request with an `image_url`.
              delete:
                tags:
                  - Delete
                  - Brand
                  - Catalog
                  - Brands
                  - Brand_id
                summary: Delete a Brand
                description: Deletes a *Brand*.
              parameters:
                - null
                - null
            /catalog/brands/{brand_id}/metafields:
              get:
                tags:
                  - Get
                  - Brand
                  - Metafields
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                summary: Get Brand Metafields
                description: >-
                  Returns a list of *Brand Metafields*. Optional filter
                  parameters can be passed in. 
              post:
                tags:
                  - Create
                  - Brand
                  - Metafield
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                summary: Create a Brand Metafield
                description: >-
                  Creates a *Brand Metafield*.


                  **Required Fields**

                  - permission_set

                  - namespace

                  - key

                  - value


                  **Read-Only Fields**

                  - id


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, or brand is 250 per client
                  ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
              parameters:
                - null
                - null
            /catalog/brands/{brand_id}/metafields/{metafield_id}:
              get:
                tags:
                  - Get
                  - Brand
                  - Metafields
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                summary: Get a Brand Metafields
                description: >-
                  Returns a *Brand Metafield*. Optional filter parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Brand
                  - Metafield
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                summary: Update a Brand Metafield
                description: "Updates a *Brand Metafield*.\n\n**Required Fields**  \n* none\n\n**Read-Only Fields**\n* id\n* These fields can only be modified by the app (API credentials) that created the metafield:\n\t* namespace\n\t* key\n\t* permission_set\n\n**Usage Notes**\n* Attempting to modify `namespace`, `key`, and `permission_set` fields using a client ID different from the one used to create those metafields will result in a 403 error message.\n* The maxiumum number of metafields allowed on each order, product, category, variant, or brand is 250 per client ID. For more information, see [Platform Limits](https://support.bigcommerce.com/s/article/Platform-Limits) in the Help Center."
              delete:
                tags:
                  - Delete
                  - Brand
                  - Metafield
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                summary: Delete a Brand Metafield
                description: Deletes a *Brand Metafield*.
              parameters:
                - null
                - null
                - null
            /catalog/brands/{brand_id}/image:
              post:
                tags:
                  - Create
                  - Brand
                  - Image
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Create a Brand Image
                description: >-
                  Creates a *Brand Image*.


                  **Required Fields**

                  - image_file: Form posts are the only accepted upload option.


                  **Read-Only Fields**

                  - id


                  Only one image at a time can be created. To update a *Brand
                  Image*, use the [Update a
                  brand](/docs/rest-catalog/brands#update-a-brand) endpoint and
                  an `image_url`.
              delete:
                tags:
                  - Delete
                  - Brand
                  - Image
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Delete a Brand Image
                description: Deletes a *Brand Image*.
              parameters:
                - null
                - null
            /catalog/brands/metafields:
              get:
                summary: Get All Brand Metafields
                tags:
                  - Get
                  - All
                  - Brand
                  - Metafields
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                  - Image
                description: Get all brand metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                  - Image
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                  - Image
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Catalog
                  - Brands
                  - Brand_id
                  - Metafields
                  - Metafield_id
                  - Image
                description: Delete all brand
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-brands-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-brands-openapi-api-evangelist-ratings.yml
  - aid: twilio:twilio-messaging-api
    name: Twilio Messaging API
    description: >-
      Send and receive messages via SMS, MMS, WhatsApp, Facebook Messenger, and
      more through our Messaging and Conversations APIs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/en-us/ahoy
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/en-us/messaging
      - type: Pricing
        url: https://www.twilio.com/en-us/sms/pricing/us
      - type: OpenAPI
        data:
          info:
            title: Twilio - Messaging
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v1/Services/{ServiceSid}/AlphaSenders:
              description: >-
                A Messaging Service resource to add, fetch or remove an Alpha
                Sender ID from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
            /v1/Services/{ServiceSid}/AlphaSenders/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove an Alpha
                Sender ID from a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
            /v1/a2p/BrandRegistrations/{BrandRegistrationSid}/SmsOtp:
              description: >-
                A Messaging Service resource to retry OTP verification for Sole
                Proprietor Brand Registrations.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations/{Sid}:
              description: >-
                A Messaging Service resource to add and fetch Brand
                Registrations.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations:
              description: >-
                A Messaging Service resource to add and fetch Brand
                Registrations.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
            /v1/a2p/BrandRegistrations/{BrandSid}/Vettings:
              description: A Messaging Service resource to add and get Brand Vettings.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
            /v1/a2p/BrandRegistrations/{BrandSid}/Vettings/{BrandVettingSid}:
              description: A Messaging Service resource to add and get Brand Vettings.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
            /v1/Services/{MessagingServiceSid}/ChannelSenders:
              description: >-
                A Messaging Service resource to read, fetch all Channel Senders
                associated with a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
            /v1/Services/{MessagingServiceSid}/ChannelSenders/{Sid}:
              description: >-
                A Messaging Service resource to read, fetch all Channel Senders
                associated with a Messaging Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
            /v1/Deactivations:
              description: >-
                A Deactivation resource to retrieve a list of United States
                phone numbers that have been deactivated by mobile carriers on a
                specific date.
              get:
                description: >-
                  Fetch a list of all United States numbers that have been
                  deactivated on a specific date.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
            /v1/LinkShortening/Domains/{DomainSid}/Certificate:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
            /v1/LinkShortening/Domains/{DomainSid}/Config:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
            /v1/LinkShortening/MessagingService/{MessagingServiceSid}/DomainConfig:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
            /v1/Services/PreregisteredUsa2p:
              description: >-
                Resource to associate preregistered campaign with Messaging
                Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/LinkShortening/Domains/{DomainSid}/MessagingServices/{MessagingServiceSid}:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/LinkShortening/MessagingServices/{MessagingServiceSid}/Domain:
              description: 'TODO: Resource-level docs'
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
            /v1/Services/{ServiceSid}/PhoneNumbers:
              description: >-
                A Messaging Service resource to add, fetch or remove phone
                numbers from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{ServiceSid}/PhoneNumbers/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove phone
                numbers from a Messaging Service.
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services:
              description: >-
                A Messaging Service resource to create, fetch, update, delete or
                add/remove senders from Messaging Services.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{Sid}:
              description: >-
                A Messaging Service resource to create, fetch, update, delete or
                add/remove senders from Messaging Services.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
            /v1/Services/{ServiceSid}/ShortCodes:
              description: >-
                A Messaging Service resource to add, fetch or remove short code
                numbers from a Messaging Service.
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
            /v1/Services/{ServiceSid}/ShortCodes/{Sid}:
              description: >-
                A Messaging Service resource to add, fetch or remove short code
                numbers from a Messaging Service.
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
            /v1/Tollfree/Verifications/{Sid}:
              description: A Messaging resource to add and fetch Tollfree Verifications.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
            /v1/Tollfree/Verifications:
              description: A Messaging resource to add and fetch Tollfree Verifications.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p:
              description: >-
                A service for (fetch/create/delete) A2P Campaign for a Messaging
                Service
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p/{Sid}:
              description: >-
                A service for (fetch/create/delete) A2P Campaign for a Messaging
                Service
              delete:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
            /v1/Services/{MessagingServiceSid}/Compliance/Usa2p/Usecases:
              description: >-
                Messaging Service Use Case resource. Fetch possible use cases
                for service. The Use Cases API returns an empty list if there is
                an issue with the customer's A2P brand registration. This Brand
                cannot register any campaign use cases. Customers are requested
                to contact support with their A2P brand information.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
                  - Usecases
            /v1/Services/Usecases:
              description: >-
                Use Case resource. Fetch possible use cases for a Messaging
                Service.
              get:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Alpha
                  - Senders
                  - Brand
                  - Registrations
                  - Registration
                  - Sms
                  - Otp
                  - Vettings
                  - Vetting
                  - Messaging
                  - Channel
                  - Deactivations
                  - Link
                  - Shortening
                  - Domains
                  - Domain
                  - Certificate
                  - Config
                  - Preregistered
                  - Usa2p
                  - Phone
                  - Numbers
                  - Short
                  - Codes
                  - Tollfree
                  - Verifications
                  - Compliance
                  - Usecases
          tags:
            - name: MessagingV1AlphaSender
            - name: MessagingV1BrandRegistration
            - name: MessagingV1BrandRegistrationOtp
            - name: MessagingV1BrandVetting
            - name: MessagingV1ChannelSender
            - name: MessagingV1Deactivations
            - name: MessagingV1DomainCerts
            - name: MessagingV1DomainConfig
            - name: MessagingV1DomainConfigMessagingService
            - name: MessagingV1ExternalCampaign
            - name: MessagingV1LinkshorteningMessagingService
            - name: MessagingV1LinkshorteningMessagingServiceDomainAssociation
            - name: MessagingV1PhoneNumber
            - name: MessagingV1Service
            - name: MessagingV1ShortCode
            - name: MessagingV1TollfreeVerification
            - name: MessagingV1UsAppToPerson
            - name: MessagingV1UsAppToPersonUsecase
            - name: MessagingV1Usecase
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/messaging-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/messaging-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---