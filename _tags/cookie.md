---
name: Cookie
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cookie.png
url: https://example.com/apis/cookie.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cookie
apis:
  - aid: bigcommerce:storefront-cookie-consent
    name: Storefront Cookie Consent
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
          openapi: 3.0.1
          info:
            title: Storefront Cookie Consent
          tags:
            - name: Consent
          paths:
            /consent:
              post:
                summary: Set Cookie Consent Preferences
                tags:
                  - Set
                  - Cookie
                  - Consent
                  - Preferences
                  - Consent
                description: >
                  Sets the status of a customer's consent to allow data
                  collection by cookies and scripts according to the following
                  consent categories:


                    2. Analytics — These cookies provide statistical information on site usage so the store owner can improve the website over time.  
                    3. Functional — These cookies enable enhanced functionality, such as videos and live chat. If a shopper does not allow these, then some or all of these functions may not work properly. 
                    4. Targeting; Advertising — These cookies allow merchants to create profiles or personalize content to enhance users' shopping experience.
                    
                    
                  This endpoint only works if the cookie consent feature is
                  enabled. It is assumed the shopper has not consented to
                  anything until a value is explicitly set. The request body
                  must be populated with a complete set of allowed and denied
                  categories.


                  Once set, consent preferences will be saved as a cookie for
                  guest shoppers. Consent preferences will be persisted to a
                  shopper's account to be used for future sessions once they
                  have logged in. Consent preferences can also be managed using
                  the [Update customer
                  consent](/docs/rest-management/customers/customer-consent#update-customer-consent)
                  endpoint.   


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 
              parameters: nu
    overlays:
      - type: APIs.io Search
        url: overlays/storefront-cookie-consent-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storefront-cookie-consent-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---