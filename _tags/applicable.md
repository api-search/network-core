---
name: Applicable
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/applicable.png
url: https://example.com/apis/applicable.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Applicable
apis:
  - name: Adyen Disputes API
    description: >-
      You can use the Disputes API to automate the dispute handling process so
      that you can respond to disputes and chargebacks as soon as they are
      initiated. The Disputes API lets you retrieve defense reasons, supply and
      delete defense documents, and accept or defend disputes.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.adyen.com/risk-management/disputes-api
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.adyen.com/risk-management/disputes-api
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            x-publicVersion: true
            title: Disputes API
          tags:
            - name: General
          paths:
            /acceptDispute:
              post:
                tags:
                  - Accept
                  - Disputes
                  - Disputes
                summary: Accept a dispute
                description: Accepts a specific dispute.
            /defendDispute:
              post:
                tags:
                  - Defend
                  - Disputes
                  - Disputes
                summary: Defend a dispute
                description: Defends a specific dispute.
            /deleteDisputeDefenseDocument:
              post:
                tags:
                  - Delete
                  - Defense
                  - Document
                  - Disputes
                  - Defense
                  - Document
                summary: Delete a defense document
                description: >-
                  Deletes a specific dispute defense document that was supplied
                  earlier.
            /retrieveApplicableDefenseReasons:
              post:
                tags:
                  - Get
                  - Applicable
                  - Defense
                  - Reasons
                  - Disputes
                  - Defense
                  - Document
                  - Applicable
                  - Reasons
                summary: Get applicable defense reasons
                description: >-
                  Returns a list of all applicable defense reasons to defend a
                  specific dispute.
            /supplyDefenseDocument:
              post:
                tags:
                  - Supply
                  - Defense
                  - Document
                  - Disputes
                  - Defense
                  - Document
                  - Applicable
                  - Reasons
                summary: Supply a defense document
                description: Supplies a
    overlays:
      - type: APIs.io Search
        url: overlays/disputes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/disputes-openapi-api-evangelist-ratings.yml
    aid: adyen:adyen-disputes-api
  - name: FactSet Content Feeds Data Dictionary
    description: >-
      Browse data items and definitions available through FactSet's off platform
      product offerings.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/content-feeds-data-dictionary
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/content-feeds-data-dictionary#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: CTS Data Dictionary API
          paths:
            /navigator/products:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Products
                  - For
                  - Navigator.
                  - Navigator
                  - Products
                summary: Get the list of products for Navigator.
            /navigator/data_items/{Product_id}:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Data
                  - Items
                  - Associated
                  - With
                  - Product
                  - For
                  - Navigator.
                  - Navigator
                  - Products
                  - Product_id
                summary: >-
                  Get the list of data items associated with a product for
                  Navigator.
            /navigator/sources/{DataItem_id}:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Sources
                  - Where
                  - The
                  - Specified
                  - Data
                  - Item
                  - Can
                  - Be
                  - Found,
                  - For
                  - Each
                  - Delivery
                  - Method,
                  - Filtered
                  - To
                  - Appearances
                  - Given
                  - Within
                  - Product.
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                summary: >-
                  Get a list of sources where the specified data item can be
                  found, for each delivery method, filtered to the appearances
                  of the given data item within the specified product.
            /navigator/sources:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Sources
                  - By
                  - Delivery
                  - Method
                  - For
                  - The
                  - Given
                  - Product_id
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                summary: >-
                  Get a list of sources by delivery method for the given
                  product_id
            /navigator/table_fields/{Table_id}:
              get:
                tags:
                  - Get
                  - The
                  - List
                  - Of
                  - Fields
                  - Associated
                  - With
                  - Table
                  - For
                  - Navigator,
                  - And
                  - Code
                  - Information
                  - Specified
                  - Data
                  - Item,
                  - If
                  - Applicable.
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                  - Table_id
                summary: >-
                  Get the list of fields associated with a table for Navigator,
                  and the code information for the specified data item, if
                  applicable.
            /navigator/basic_search:
              post:
                tags:
                  - Returns
                  - The
                  - Data
                  - Items
                  - (along
                  - With
                  - Products
                  - They
                  - Belong
                  - To)
                  - That
                  - Contain
                  - At
                  - Least
                  - One
                  - Of
                  - Search
                  - Terms
                  - As
                  - Substring
                  - Either
                  - Their
                  - Na
                  - Navigator
                  - Products
                  - Product_id
                  - Data
                  - Item_id
                  - Sources
                  - Table_id
                  - Basic_search
                summary: >-
                  Returns the data items (along with the products they belong
                  to) that contain at least one of the search terms as a
                  substring of either their
    overlays:
      - type: APIs.io Search
        url: overlays/content-feeds-data-dictionary-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/content-feeds-data-dictionary-openapi-api-evangelist-ratings.yml
    aid: factset:factset-content-feeds-data-dictionary
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---