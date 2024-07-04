---
name: Catalog
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/catalog.png
url: https://example.com/apis/catalog.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Catalog
apis:
  - name: outposts
    description: >-
      <p>Amazon Web Services Outposts is a fully managed service that extends
      Amazon Web Services infrastructure, APIs, and tools to customer premises.
      By providing local access to Amazon Web Services managed infrastructure,
      Amazon Web Services Outposts enables customers to build and run
      applications on premises using the same programming interfaces as in
      Amazon Web Services Regions, while using local compute and storage
      resources for lower latency and local data processing needs.</p>
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
            title: outposts
          paths:
            /orders/{OrderId}/cancel:
              POST:
                summary: CancelOrder
                description: <p>Cancels the specified order for an Outpost.</p>
                tags:
                  - Cancel
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
            /orders:
              POST:
                summary: CreateOrder
                description: <p>Creates an order for an Outpost.</p>
                tags:
                  - Create
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
            /outposts:
              GET:
                summary: ListOutposts
                description: >-
                  <p>Lists the Outposts for your Amazon Web Services
                  account.</p> <p>Use filters to return specific results. If you
                  specify multiple filters, the results include only the
                  resources that match all of the specified filters. For a
                  filter where you can specify multiple values, the results
                  include items that match any of the values that you specify
                  for the filter.</p>
                tags:
                  - Lists
                  - Outposts
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
            /sites:
              GET:
                summary: ListSites
                description: >-
                  <p>Lists the Outpost sites for your Amazon Web Services
                  account. Use filters to return specific results.</p> <p>Use
                  filters to return specific results. If you specify multiple
                  filters, the results include only the resources that match all
                  of the specified filters. For a filter where you can specify
                  multiple values, the results include items that match any of
                  the values that you specify for the filter.</p>
                tags:
                  - Lists
                  - Sites
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
            /outposts/{OutpostId}:
              PATCH:
                summary: UpdateOutpost
                description: <p> Updates an Outpost. </p>
                tags:
                  - Update
                  - Outposts
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
            /sites/{SiteId}:
              PATCH:
                summary: UpdateSite
                description: <p>Updates the specified site.</p>
                tags:
                  - Update
                  - Sites
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
            /catalog/item/{CatalogItemId}:
              GET:
                summary: GetCatalogItem
                description: <p>Gets information about the specified catalog item.</p>
                tags:
                  - Get
                  - Catalog
                  - Items
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
            /connections/{ConnectionId}:
              GET:
                summary: GetConnection
                description: >-
                  <note> <p> Amazon Web Services uses this action to install
                  Outpost servers.</p> </note> <p> Gets information about the
                  specified connection. </p> <p> Use CloudTrail to monitor this
                  action or Amazon Web Services managed policy for Amazon Web
                  Services Outposts to secure it. For more information, see <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/security-iam-awsmanpol.html">
                  Amazon Web Services managed policies for Amazon Web Services
                  Outposts</a> and <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/logging-using-cloudtrail.html">
                  Logging Amazon Web Services Outposts API calls with Amazon Web
                  Services CloudTrail</a> in the <i>Amazon Web Services Outposts
                  User Guide</i>. </p>
                tags:
                  - Get
                  - Connections
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
            /orders/{OrderId}:
              GET:
                summary: GetOrder
                description: <p>Gets information about the specified order.</p>
                tags:
                  - Get
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
            /outposts/{OutpostId}/instanceTypes:
              GET:
                summary: GetOutpostInstanceTypes
                description: <p>Gets the instance types for the specified Outpost.</p>
                tags:
                  - Get
                  - Outposts
                  - Instances
                  - Types
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
            /sites/{SiteId}/address:
              PUT:
                summary: UpdateSiteAddress
                description: >-
                  <p>Updates the address of the specified site.</p> <p>You can't
                  update a site address if there is an order in progress. You
                  must wait for the order to complete or cancel the order.</p>
                  <p>You can update the operating address before you place an
                  order at the site, or after all Outposts that belong to the
                  site have been deactivated.</p>
                tags:
                  - Update
                  - Sites
                  - Addresses
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
            /outposts/{OutpostId}/assets:
              GET:
                summary: ListAssets
                description: >-
                  <p>Lists the hardware assets for the specified Outpost.</p>
                  <p>Use filters to return specific results. If you specify
                  multiple filters, the results include only the resources that
                  match all of the specified filters. For a filter where you can
                  specify multiple values, the results include items that match
                  any of the values that you specify for the filter.</p>
                tags:
                  - Lists
                  - Assets
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
            /catalog/items:
              GET:
                summary: ListCatalogItems
                description: >-
                  <p>Lists the items in the catalog.</p> <p>Use filters to
                  return specific results. If you specify multiple filters, the
                  results include only the resources that match all of the
                  specified filters. For a filter where you can specify multiple
                  values, the results include items that match any of the values
                  that you specify for the filter.</p>
                tags:
                  - Lists
                  - Catalog
                  - Items
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
            /list-orders:
              GET:
                summary: ListOrders
                description: >-
                  <p>Lists the Outpost orders for your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Orders
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes tags from the specified resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
                  - Resources
                  - ARN
            /connections:
              POST:
                summary: StartConnection
                description: >-
                  <note> <p> Amazon Web Services uses this action to install
                  Outpost servers.</p> </note> <p> Starts the connection
                  required for Outpost server installation. </p> <p> Use
                  CloudTrail to monitor this action or Amazon Web Services
                  managed policy for Amazon Web Services Outposts to secure it.
                  For more information, see <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/security-iam-awsmanpol.html">
                  Amazon Web Services managed policies for Amazon Web Services
                  Outposts</a> and <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/logging-using-cloudtrail.html">
                  Logging Amazon Web Services Outposts API calls with Amazon Web
                  Services CloudTrail</a> in the <i>Amazon Web Services Outposts
                  User Guide</i>. </p>
                tags:
                  - Start
                  - Connections
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
                  - Resources
                  - ARN
                  - Connections
            /sites/{SiteId}/rackPhysicalProperties:
              PATCH:
                summary: UpdateSiteRackPhysicalProperties
                description: >-
                  <p>Update the physical and logistical details for a rack at a
                  site. For more information about hardware requirements for
                  racks, see <a
                  href="https://docs.aws.amazon.com/outposts/latest/userguide/outposts-requirements.html#checklist">Network
                  readiness checklist</a> in the Amazon Web Services Outposts
                  User Guide. </p> <p>To update a rack at a site with an order
                  of <code>IN_PROGRESS</code>, you must wait for the order to
                  complete or cancel the 
                tags:
                  - Update
                  - Sites
                  - Rack
                  - Physical
                  - Properties
                  - Orders
                  - Identifiers
                  - Cancel
                  - Orders
                  - Outposts
                  - Sites
                  - Outposts
                  - Sites
                  - Catalog
                  - Items
                  - Connections
                  - Instances
                  - Types
                  - Addresses
                  - Assets
                  - Items
                  - Lists
                  - Resources
                  - ARN
                  - Connections
                  - Rack
                  - Physical
                  - Properties
    overlays:
      - type: APIs.io Search
        url: overlays/outposts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/outposts-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:outposts
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
  - aid: bigcommerce:catalog-categories
    name: Catalog - Categories
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
            title: Catalog - Categories
            version: ''
          tags:
            - name: Batch metafields
            - name: Metafields
            - name: Images
            - name: Sort Order
            - name: Categories (deprecated)
          paths:
            /catalog/categories:
              get:
                tags:
                  - Get
                  - All
                  - Categories
                  - Catalog
                  - Categories
                summary: Get All Categories
                description: >-
                  When possible, use the [Catalog Trees - Get all
                  categories](/docs/rest-catalog/category-trees/categories#get-all-categories)
                  endpoint instead.


                  Returns a list of *Categories*. Optional filter parameters can
                  be passed in.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              post:
                tags:
                  - Create
                  - Category
                  - Catalog
                  - Categories
                summary: Create a Category
                description: "When possible, use the [Category Trees - Create categories](/docs/rest-catalog/category-trees/categories#create-categories) endpoint instead.\n\nCreates a *Category*.\n\nUse this endpoint when an API only works with categories of a default BigCommerce storefront (`channel_id=1`). \n\nUse the [Create categories](/docs/rest-catalog/category-trees/categories#create-categories) endpoint when an API works with categories across different category trees that belong to different storefront channels.\n\n**Required Fields**:\n- `parent_id`: \n\t- To create a child category, set the `parent_id` to the parent category.\n\t- To create a top level category, set the `parent_id` to `0`.\n- `name`\n\n**Read-Only Fields**:\n- `id`\n\n**Limits**:\n- 16,000 categories per store limit.\n- 1,000 categories per product limit.\n- 50 characters category name length.\n- 8 levels of category depth limit.\n- 65,642 characters category description length limit.\n\n **Note:**\n The default rate limit for this endpoint is 40 concurrent requests.\n"
              delete:
                tags:
                  - Delete
                  - Categories
                  - Catalog
                  - Categories
                summary: Delete Categories
                description: >-
                  When possible, use the [Category Trees - Delete
                  categories](/docs/rest-catalog/category-trees/categories#delete-categories)
                  endpoint instead.


                  Deletes *Category* objects. At least one filter parameter is
                  required to perform the `DELETE` operation.


                  **Usage Notes**


                  - Sending a `DELETE`request without specifying a filter
                  parameter will result in a `422` error. 

                  - Sending a `DELETE` request for a category that contains
                  products will result in a `422` error. Move products to a new
                  category by sending a `PUT` request to the
                  `/catalog/products/{product_id}` endpoint before deleting a
                  category.
              parameters:
                - null
            /catalog/categories/{category_id}:
              get:
                tags:
                  - Get
                  - Category
                  - Catalog
                  - Categories
                  - Category_id
                summary: Get a Category
                description: >-
                  When possible, use the [Catalog Trees - Get all
                  categories](/docs/rest-catalog/category-trees/categories#get-all-categories)
                  endpoint instead. You can provide a category identifier using
                  query parameters to retrieve a single category.


                  Returns a single *Category*. Optional parameters can be passed
                  in.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              put:
                tags:
                  - Update
                  - Category
                  - Catalog
                  - Categories
                  - Category_id
                summary: Update a Category
                description: >-
                  When possible, use the [Catalog Trees - Update
                  categories](/docs/rest-catalog/category-trees/categories#update-categories)
                  endpoint instead.


                  Updates a *Category*.


                  **Required Fields**

                  * none


                  **Read-Only Fields**

                  - id


                  **Note:** 

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              delete:
                tags:
                  - Delete
                  - Category
                  - Catalog
                  - Categories
                  - Category_id
                summary: Delete a Category
                description: >-
                  When possible, use the [Category Trees - Delete
                  categories](/docs/rest-catalog/category-trees/categories#delete-categories)
                  endpoint instead. You can provide a category identifier using
                  query parameters to delete a single category.


                  Deletes a *Category*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
                - null
            /catalog/categories/{category_id}/metafields:
              get:
                tags:
                  - Get
                  - Category
                  - Metafields
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                summary: Get Category Metafields
                description: >-
                  Returns a list of *Metafields* on a *Category*. Optional
                  filter parameters can be passed in.
              post:
                tags:
                  - Create
                  - Category
                  - Metafield
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                summary: Create a Category Metafield
                description: >-
                  Creates a *Category Metafield*.


                  **Required Fields:**

                  - permission_set

                  - namespace

                  - key

                  - value


                  **Read-Only Fields**

                  - id


                  **Note:** The maximum number of metafields allowed on each
                  order, product, category, variant, or brand is 250 per client
                  ID. For more information, see [Platform Limits (Help
                  Center)](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
              parameters:
                - null
                - null
            /catalog/categories/{category_id}/metafields/{metafield_id}:
              get:
                tags:
                  - Get
                  - Category
                  - Metafield
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                summary: Get a Category Metafield
                description: >-
                  Returns a single *Category Metafield*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Category
                  - Metafield
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                summary: Update a Category Metafield
                description: "Updates a *Category Metafield*.\n\n**Required Fields**\n* none\n\n**Read-Only Fields**\n* id\n* These fields can only be modified by the app (API credentials) that created the metafield:\n\t* namespace\n\t* key\n\t* permission_set\n\n**Usage Notes**\n* Attempting to modify `namespace`, `key`, and `permission_set` fields using a client ID different from the one used to create those metafields will result in a 403 error message. "
              delete:
                tags:
                  - Delete
                  - Category
                  - Metafield
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                summary: Delete a Category Metafield
                description: Deletes a *Category Metafield*.
              parameters:
                - null
                - null
                - null
            /catalog/categories/{category_id}/image:
              post:
                tags:
                  - Create
                  - Category
                  - Image
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Create a Category Image
                description: >-
                  Create a *Category Image*.

                   **Required Fields**
                  - image_file: Form posts are the only accepted upload option.


                  Only one image at a time can be created.

                  Limit image size to 1MB.

                  To update a *Category Image*, use the [Update
                  categories](/docs/rest-catalog/category-trees/categories#update-categories)
                  endpoint and an `image_url`.
              delete:
                tags:
                  - Delete
                  - Category
                  - Image
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Delete a Category Image
                description: Deletes a *Category Image*.
              parameters:
                - null
                - null
            /catalog/categories/{category_id}/products/sort-order:
              get:
                tags:
                  - Get
                  - Product
                  - Sort
                  - Order
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                  - Products
                  - Sort
                  - Order
                summary: Get Product Sort Order
                description: >-
                  Returns a list of products and their sort order for a specific
                  category.


                  **Usage Notes**

                  * Data pairs are displayed in ascending order based on
                  products' `sort_order` values.

                  * `null` values are allowed for products without specified
                  `sort_order` values.

                  * Products with `sort_order` value of `null` will be displayed
                  after products with valid numerical values.

                  * The priorities for determining product sort order on a
                  storefront are the following:
                    - Priority 1: Manually specified sort order on Category Level (API).
                    - Priority 2: Manually specified sort order on Product (Global) Level (UI/API).
                    - Priority 3: Default sorting by Product ID (newly added products go first) (UI/API).
              put:
                tags:
                  - Update
                  - Product
                  - Sort
                  - Order
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                  - Products
                  - Sort
                  - Order
                summary: Update Product Sort Order
                description: Updates sort order of products within a specific category.
              parameters:
                - null
                - null
            /catalog/categories/metafields:
              get:
                summary: Get All Category Metafields
                tags:
                  - Get
                  - All
                  - Category
                  - Metafields
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                  - Products
                  - Sort
                  - Order
                description: Get all category metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                  - Products
                  - Sort
                  - Order
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                  - Products
                  - Sort
                  - Order
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Catalog
                  - Categories
                  - Category_id
                  - Metafields
                  - Metafield_id
                  - Image
                  - Products
                  - Sort
                  - Order
                description: Delete all category
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-categories-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-categories-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:catalog-category-trees
    name: Catalog - Category Trees
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
            title: Catalog - Category Trees
            version: ''
          tags:
            - name: Category Trees
            - name: Categories
          paths:
            /catalog/trees/categories:
              get:
                summary: Get All Categories
                description: |-
                  Returns a list of categories. 

                  To get a specific category in a tree, provide a category ID.
                tags:
                  - Get
                  - All
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              post:
                summary: Create Categories
                description: |-
                  Creates new categories. 

                  Creating a category requires:
                   - `name`
                   - `tree_id` or `parent_id` 
                tags:
                  - Create
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              put:
                summary: Update Categories
                description: |-
                  Updates existing categories. 

                   To update a specific category in a tree, provide a category id.
                tags:
                  - Update
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              delete:
                summary: Delete Categories
                description: >-
                  Deletes categories. 


                  To delete a specific category in a tree, provide a category
                  ID.
                tags:
                  - Delete
                  - Categories
                  - Catalog
                  - Trees
                  - Categories
              parameters:
                - null
            /catalog/trees:
              get:
                summary: Get All Category Trees
                description: Returns a list of *Category Trees*.
                tags:
                  - Get
                  - All
                  - Category
                  - Trees
                  - Catalog
                  - Trees
                  - Categories
              put:
                summary: Upsert Category Trees
                description: >
                  Upserts *Category Trees*. 


                  This single endpoint updates and creates category trees. If a
                  tree object contains an ID, it is processed as an update
                  operation using that ID. If you do not provide an ID, a new
                  tree is created. The category tree `name` field is required to
                  create trees, but is not required on the update.


                  **Usage Notes**

                  * `channel_id` is required to create a *Category Tree*. You
                  can assign one `channel_id` to one category tree.
                tags:
                  - Upsert
                  - Category
                  - Trees
                  - Catalog
                  - Trees
                  - Categories
              delete:
                summary: Delete Category Trees
                description: >-
                  Deletes *Category Trees*. A filter must be supplied with the
                  endpoint.
                tags:
                  - Delete
                  - Category
                  - Trees
                  - Catalog
                  - Trees
                  - Categories
              parameters:
                - null
            /catalog/trees/{tree_id}/categories:
              get:
                summary: Get a Category Tree
                description: Returns a *Category Tree*.
                tags:
                  - Get
                  - Category
                  - Tree
                  - Catalog
                  - Trees
                  - Categories
                  - Tree_id
              parameters:
                - null
                - null
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-category-trees-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-category-trees-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:catalog-product-modifiers
    name: Catalog - Product Modifiers
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
            title: Catalog - Product Modifiers
            version: ''
          tags:
            - name: Product Modifiers
            - name: Values
            - name: Images
          paths:
            /catalog/products/{product_id}/modifiers:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Modifiers
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                summary: Get All Product Modifiers
                description: >-
                  Returns a list of all *Product Modifiers*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Modifier
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                summary: Create a Product Modifier
                description: >-
                  Creates a *Product Modifier*.


                  **Required Fields**

                  * `required`

                  * `display_name`

                  * `type`


                  **Read-Only Fields**

                  * `id`


                  **Notes**

                  It takes two separate requests to create a new checkbox
                  modifier with option values. Perform a request to create a
                  modifier, then perform a second request to update option
                  values.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/modifiers/{modifier_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Modifier
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                summary: Get a Product Modifier
                description: >-
                  Returns a single *Product Modifier*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Modifier
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                summary: Update a Product Modifier
                description: Updates a *Product Modifier*.
              delete:
                tags:
                  - Delete
                  - Product
                  - Modifier
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                summary: Delete a Product Modifier
                description: Deletes a *Product Modifier*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/modifiers/{modifier_id}/values:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Modifier
                  - Values
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                  - Values
                summary: Get All Product Modifier Values
                description: >-
                  Returns a list of all product *Modifier Values*. Optional
                  parameters can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Modifier
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                  - Values
                summary: Create Product Modifier Value
                description: |-
                  Creates a *Modifier Value*.

                  **Required Fields**
                  * label
                  * sort_order

                  **Read-Only Fields**
                  * id
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/modifiers/{modifier_id}/values/{value_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Modifier
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                  - Values
                  - Value_id
                summary: Get a Product Modifier Value
                description: >-
                  Returns a single *Modifier Value*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Modifier
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                  - Values
                  - Value_id
                summary: Update a Product Modifier Value
                description: |-
                  Updates a *Modifier Value*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Modifier
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                  - Values
                  - Value_id
                summary: Delete Product Modifier Value
                description: Deletes a *Modifier Value*.
              parameters:
                - null
                - null
                - null
                - null
            /catalog/products/{product_id}/modifiers/{modifier_id}/values/{value_id}/image:
              post:
                tags:
                  - Create
                  - Product
                  - Modifier
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Modifiers
                  - Modifier_id
                  - Values
                  - Value_id
                  - Image
                summary: Create Product Modifier Image
                description: >-
                  Creates a *Modifier Image*.


                  The image will show on the storefront when the value is
                  selected.

                   **Required Fields**
                  - image_file: Form posts are the only accepted upload option.
              parameters:
                - null
                - null
                - null
                - null
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-product-modifiers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-product-modifiers-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:catalog-product-variant-options
    name: Catalog - Product Variant Options
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
            title: Catalog - Product Variant Options
            version: ''
          tags:
            - name: Product Variant Options
            - name: Values
          paths:
            /catalog/products/{product_id}/options:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Variant
                  - Options
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                summary: Get All Product Variant Options
                description: >-
                  Returns a list of product *Variant Options*. Optional
                  parameters can be passed in. 
              post:
                tags:
                  - Create
                  - Product
                  - Variant
                  - Option
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                summary: Create a Product Variant Option
                description: >-
                  Creates a *Variant Option*.


                  **Required Fields**

                  * display_name

                  * type

                  * option_values


                  **Read-Only Fields**

                  * id


                  **Limits**

                  * 255 characters option name length.


                  **Notes**


                  * Only one variant option at a time can be created; individual
                  variant options will contain an array of multiple values.

                  * There are several examples listed below that create options,
                  but the SKUs are not updated and they are not a variant on the
                  product. Variant SKUs must be created with a separate request.

                  * Variant options will show on the storefront as an option
                  that can be selected by the customer. A request like this
                  could be used to add new choices to a variant that has already
                  been created.

                  * If more than one variant needs to be created, use the
                  [Create a
                  Product](/docs/rest-catalog/products#create-a-product)
                  endpoint.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/options/{option_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Variant
                  - Option
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                summary: Get a Product Variant Option
                description: >-
                  Returns a single *Variant Option*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Variant
                  - Option
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                summary: Update a Product Variant Option
                description: |-
                  Updates a *Variant Option*.

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Variant
                  - Option
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                summary: Delete a Product Variant Option
                description: Deletes a *Variant Option*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/options/{option_id}/values:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Variant
                  - Option
                  - Values
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                  - Values
                summary: Get All Product Variant Option Values
                description: >-
                  Returns a list of all *Variant Option Values*. Optional
                  parameters can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Variant
                  - Option
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                  - Values
                summary: Create a Product Variant Option Value
                description: |-
                  Creates a *Variant Option Value*.

                  **Required Fields**
                  * label
                  * sort_order

                  **Read-Only Fields**
                  * id

                  **Limits**
                  * 250 option values per option limit.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/options/{option_id}/values/{value_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Variant
                  - Option
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                  - Values
                  - Value_id
                summary: Get a Product Variant Option Value
                description: >-
                  Returns a single *Variant Option Value*. Optional parameters
                  can be passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Variant
                  - Option
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                  - Values
                  - Value_id
                summary: Update a Product Variant Option Value
                description: |-
                  Updates a *Variant Option Value*.

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Variant
                  - Option
                  - Value
                  - Catalog
                  - Products
                  - Product_id
                  - Options
                  - Option_id
                  - Values
                  - Value_id
                summary: Delete a Product Variant Option Value
                description: Deletes a *Variant Option Value*.
              parameters:
                - null
                - null
                - null
                - null
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-product-variant-options-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/catalog-product-variant-options-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:catalog-product-variants
    name: Catalog - Product Variants
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
            title: Catalog - Product Variants
            version: ''
          tags:
            - name: Batch metafields
            - name: Product Variants
            - name: Variants (Batch)
            - name: Metafields
            - name: Images
          paths:
            /catalog/products/{product_id}/variants:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Variants
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                summary: Get All Product Variants
                description: >-
                  Returns a list of product *Variants*. Optional parameters can
                  be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Variant
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                summary: Create a Product Variant
                description: >-
                  Creates a *Product Variant*.


                  **Required Fields**

                  * sku

                  * option_values


                  **Read-Only Fields**

                  * id


                  **Limits**

                  * 600 SKUs per product limit.

                  * 255 characters SKU length limit.


                  Variants need to be created one at a time using this endpoint.
                  To use a variant array, create products, and variants in the
                  same call use the [Create
                  Products](/docs/rest-catalog/products#create-a-product)
                  endpoint during the initial product creation.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/variants/{variant_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Variant
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                summary: Get a Product Variant
                description: >-
                  Returns a single product *Variant*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Variant
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                summary: Update a Product Variant
                description: Updates a product *Variant*.
              delete:
                tags:
                  - Delete
                  - Product
                  - Variant
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                summary: Delete a Product Variant
                description: Deletes a product *Variant*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/variants/{variant_id}/metafields:
              get:
                tags:
                  - Get
                  - Product
                  - Variant
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                summary: Get Product Variant Metafields
                description: >-
                  Returns a list of product variant *Metafields*. Optional
                  parameters can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Variant
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                summary: Create a Product Variant Metafield
                description: >-
                  Creates a product variant *Metafield*.


                  **Required Fields:**

                  * permission_set

                  * namespace

                  * key

                  * value


                  **Read-Only Fields**

                  * id


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, or brand is 250 per client
                  ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/variants/{variant_id}/metafields/{metafield_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Variant
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                summary: Get a Product Variant Metafields
                description: >-
                  Returns a single product variant *Metafield*. Optional
                  parameters can be passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Variant
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                summary: Update Product Variant Metafields
                description: "Updates a product variant *Metafield*.\n\n**Required Fields:**\n* none\n\n**Read-Only Fields**\n* id\n* These fields can only be modified by the app (API credentials) that created the metafield:\n\t* namespace\n\t* key\n\t* permission_set\n\n**Usage Notes**\n* Attempting to modify `namespace`, `key`, and `permission_set` fields using a client ID different from the one used to create those metafields will result in a 403 error message. "
              delete:
                tags:
                  - Delete
                  - Product
                  - Variant
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                summary: Delete a Product Variant Metafield
                description: Deletes a product variant *Metafield*.
              parameters:
                - null
                - null
                - null
                - null
            /catalog/products/{product_id}/variants/{variant_id}/image:
              post:
                tags:
                  - Create
                  - Product
                  - Variant
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Create a Product Variant Image
                description: >-
                  Creates a *Variant Image*.


                  Only one image can be explicitly associated with a Variant. If
                  the Variant already has an associated image, overwrites the
                  existing Variant Image.


                  The image displays on the storefront when the Variant is
                  selected.

                   **Required Fields**
                  - image_file: Form posts. Files larger than 1 MB are not
                  accepted

                  - image_url: Any publicly available URL
              parameters:
                - null
                - null
                - null
            /catalog/variants:
              get:
                tags:
                  - Get
                  - All
                  - Variants
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Get All Variants
                description: >-
                  Returns a list of all variants in your catalog. Optional
                  parameters can be passed in.
              put:
                tags:
                  - Update
                  - Variants
                  - Batch)
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                  - Image
                summary: Update Variants (Batch)
                description: >-
                  Updates a batch of `variant` objects. Currently the limit is
                  50 variants however this is subject to change.


                  **Required Fields**


                  To update an existing variant:

                  * id (variant ID)


                  To create a new variant:

                  * product_id

                  * sku

                  * option_values
                    - id (option_value ID - Example: 146)
                    - option_id (Option ID - Example: 151)
              parameters:
                - null
            /catalog/variants/metafields:
              get:
                summary: Get All Product Variant Metafields
                tags:
                  - Get
                  - All
                  - Product
                  - Variant
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                  - Image
                description: Get all variant metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
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
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
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
                  - Products
                  - Product_id
                  - Variants
                  - Variant_id
                  - Metafields
                  - Metafield_id
                  - Image
                description: Delete all variant
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-product-variants-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-product-variants-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:catalog-products
    name: Catalog - Products
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
            title: Catalog - Products
            version: ''
          tags:
            - name: Batch metafields
            - name: Products
            - name: Bulk Pricing Rules
            - name: Complex Rules
            - name: Custom Fields
            - name: Images
            - name: Metafields
            - name: Reviews
            - name: Videos
            - name: Channel Assignments
            - name: Category Assignments
            - name: Summary
          paths:
            /catalog/products:
              get:
                tags:
                  - Get
                  - All
                  - Products
                  - Catalog
                  - Products
                summary: Get All Products
                description: >-
                  Returns a list of **Products**. Optional filter parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Products
                  - Batch)
                  - Catalog
                  - Products
                summary: Update Products (Batch)
                description: >-
                  Updates products in batches. Batches are limited to 10
                  products.


                  **Required Fields**

                  * `id` - product `id` is required for batch updates to
                  products.


                  **Read-Only Fields**

                  - `id`

                  - `date_created`

                  - `date_modified`

                  - `calculated_price`

                  - `base_variant_id`
              post:
                tags:
                  - Create
                  - Product
                  - Catalog
                  - Products
                summary: Create a Product
                description: >-
                  Creates a *Product*. Only one product can be created at a
                  time; however, you can create multiple product variants using
                  the `variants` array.


                  **Required Fields:**

                  - `name`

                  - `type`

                  - `weight`

                  - `price`


                  **Read-Only Fields**

                  - `id`

                  - `date_created`

                  - `date_modified`

                  - `calculated_price`

                  - `base_variant_id`


                  **Limits**

                  - 250 characters product name length.

                  - A product can have up to 1000 images. Each image file or
                  image uploaded by URL can be up to 8 MB.


                  **Usage Notes**

                  * You can create multiple product variants using the
                  `variants` array.

                  * This endpoint accepts a `video` array. To create a product
                  video that accepts a `video` object, see [Create a Product
                  Video](/docs/rest-catalog/products/videos#create-a-product-video)
                  for information.
              delete:
                tags:
                  - Delete
                  - Products
                  - Catalog
                  - Products
                summary: Delete Products
                description: >-
                  To delete *Product* objects, you must include a filter. This
                  prevents inadvertently deleting all *Product* objects in a
                  store.


                  > #### Note

                  > The maximum number of products you can delete at one time is
                  250.


                  **Example**:

                  To delete products with IDs 1,2 and 3, use `DELETE
                  /v3/catalog/products?id:in=1,2,3`.
              parameters:
                - null
            /catalog/products/{product_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Get a Product
                description: >-
                  Returns a single *Product*. Optional parameters can be passed
                  in.
              put:
                tags:
                  - Update
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Update a Product
                description: >
                  Updates a *Product*.


                  **Limits**

                  - A product can have up to 1000 images. Each image file or
                  image uploaded by URL can be up to 8 MB.


                  **Read-Only Fields**

                  - id

                  - date_created

                  - date_modified

                  - calculated_price

                  - base_variant_id
              delete:
                tags:
                  - Delete
                  - Product
                  - Catalog
                  - Products
                  - Product_id
                summary: Delete a Product
                description: Deletes a *Product*.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/images:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Images
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                summary: Get All Product Images
                description: >-
                  Returns a list of *Product Images*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                summary: Create a Product Image
                description: >-
                  Creates a *Product Image*.

                   **Required Fields**
                  - `image_file`, or

                  - `image_url`


                  **Usage Notes**

                  - `image_url` - `255` character limit

                  - For file uploads, use the `multipart/form-data` media type.

                  - You can create only one image at a time. A product can have
                  up to 1000 images.

                  - Supported image file types are BMP, GIF, JPEG, PNG, WBMP,
                  XBM, and WEBP.

                  - Each image file or image uploaded by URL can be up to 8 MB.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/images/{image_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Get a Product Image
                description: >-
                  Returns a single *Product Image*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Update a Product Image
                description: >-
                  Updates a *Product Image*.


                  **Usage Notes**

                  - `image_url` - `255` character limit

                  - Each image file or image uploaded by URL can be up to 8 MB.

                  - For file uploads, send a POST request using the
                  `multipart/form-data` media type
              delete:
                tags:
                  - Delete
                  - Product
                  - Image
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                summary: Delete a Product Image
                description: Deletes a *Product Image*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/videos:
              get:
                tags:
                  - Get
                  - All
                  - Product
                  - Videos
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                summary: Get All Product Videos
                description: >-
                  Returns a list of *Product Videos*. Optional parameters can be
                  passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                summary: Create a Product Video
                description: |-
                  Creates a *Product Video*.

                  **Required Fields**
                  * video_id

                  **Read-Only Fields**
                  * id

                  Publicly accessible URLs are valid parameters.
                  Videos must be loaded through YouTube at this time.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/videos/{id}:
              get:
                tags:
                  - Get
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Get a Product Video
                description: >-
                  Returns a single *Product Video*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Update a Product Video
                description: |-
                  Updates a *Product Video.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Video
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                summary: Delete a Product Video
                description: Deletes a *Product Video*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/complex-rules:
              get:
                tags:
                  - Get
                  - Complex
                  - Rules
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                summary: Get Complex Rules
                description: >-
                  Returns a list of all product *Complex Rules*. Optional
                  parameters may be passed in.
              post:
                tags:
                  - Create
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                summary: Create a Complex Rule
                description: |-
                  Creates a product *Complex Rule*.

                  **Required Fields**
                  - modifier_id
                  - modifier_value_id
                  - variant_id

                  **Read-Only Fields**
                  - complex_rule_id
                  - conditions_id
                  - rule_id
                  - combination_id
                  - id
              parameters:
                - null
                - null
            /catalog/products/{product_id}/complex-rules/{complex_rule_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Get a Product Complex Rule
                description: >-
                  Returns a single *Complex Rule*. Optional parameters can be
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Update a Product Complex Rule
                description: |-
                  Updates a *Complex Rule*.

                  **Required Fields**:
                  - none

                  **Read-Only Fields**:
                  - complex_rule_id
                  - conditions_id
                  - rule_id
                  - combination_id
                  - id
              delete:
                tags:
                  - Delete
                  - Product
                  - Complex
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                summary: Delete a Product Complex Rule
                description: Deletes a product *Complex Rule*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/custom-fields:
              get:
                tags:
                  - Get
                  - Product
                  - Custom
                  - Fields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                summary: Get Product Custom Fields
                description: >-
                  Returns a list of product *Custom Fields*. You can pass in
                  optional parameters.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              post:
                tags:
                  - Create
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                summary: Create a Product Custom Field
                description: >-
                  Creates a *Custom Field*.


                  **Required Fields:**

                  - name

                  - value


                  **Name-Value Pair Uniqueness**

                  - Every name-value pair must be unique inside a product.


                  **Read-Only:**

                  - id


                  **Limits**

                  - 200 custom fields per product limit.

                  - 250 characters per custom field limit.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
            /catalog/products/{product_id}/custom-fields/{custom_field_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Get a Product Custom Field
                description: >
                  Returns a *Custom Field*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              put:
                tags:
                  - Update
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Update a Product Custom Field
                description: |-
                  Updates a *Custom Field*.

                  **Required Fields**
                  - none

                  **Name-Value Pair Uniqueness**
                  - Every name-value pair must be unique inside a product.

                  **Read-Only**
                  - id

                   **Limits**
                  - 200 custom fields per product limit.
                  - 250 characters per custom field limit.
                  - 40 concurrent requests default rate limit.
              delete:
                tags:
                  - Delete
                  - Product
                  - Custom
                  - Field
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                summary: Delete a Product Custom Field
                description: >-
                  Deletes a product *Custom Field*.


                  **Note:**

                  The default rate limit for this endpoint is 40 concurrent
                  requests.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/bulk-pricing-rules/{bulk_pricing_rule_id}:
              get:
                tags:
                  - Get
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Get a Bulk Pricing Rule
                description: >-
                  Returns a single *Bulk Pricing Rule*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Update a Bulk Pricing Rule
                description: |-
                  Updates a *Bulk Pricing Rule*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  - id
              delete:
                tags:
                  - Delete
                  - Bulk
                  - Pricing
                  - Rule
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                summary: Delete a Bulk Pricing Rule
                description: Deletes a *Bulk Pricing Rule*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/metafields:
              get:
                tags:
                  - Get
                  - Product
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                summary: Get Product Metafields
                description: >-
                  Returns a list of *Product Metafields*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                summary: Create a Product Metafield
                description: >-
                  Creates a *Product Metafield*.


                  **Required Fields:**

                  * permission_set

                  * namespace

                  * key

                  * value


                  **Note:** The maxiumum number of metafields allowed on each
                  order, product, category, variant, or brand is 250 per client
                  ID. For more information, see [Platform
                  Limits](https://support.bigcommerce.com/s/article/Platform-Limits)
                  in the Help Center.
              parameters:
                - null
                - null
            /catalog/products/{product_id}/metafields/{metafield_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Get a Product Metafield
                description: >-
                  Returns a single *Product Metafield*. Optional parameters can
                  be passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Update a Product Metafield
                description: "Updates a *Product Metafield*.\n\n**Required Fields**\n* none\n\n**Read-Only Fields**\n* id\n* These fields can only be modified using the API account that created the metafield:\n\t* `namespace`\n\t* `key`\n\t* `permission_set`\n\t* `value`\n\n**Usage Notes**\n* Attempting to modify the `namespace`, `key`, `permission_set`, or `value` field using an API account different from the one used to create those metafields will result in a `403` error message. "
              delete:
                tags:
                  - Delete
                  - Product
                  - Metafield
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                summary: Delete a Product Metafield
                description: Deletes a *Product Metafield*.
              parameters:
                - null
                - null
                - null
            /catalog/products/{product_id}/reviews:
              get:
                tags:
                  - Get
                  - Product
                  - Reviews
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                summary: Get Product Reviews
                description: >-
                  Returns a list of all *Product Reviews*. Optional parameters
                  can be passed in.
              post:
                tags:
                  - Create
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                summary: Create a Product Review
                description: |-
                  Creates a *Product Review*.

                  **Required Fields**
                  - title
                  - date_reviewed

                  **Read-Only Fields**
                  * id
              parameters:
                - null
                - null
            /catalog/products/{product_id}/reviews/{review_id}:
              get:
                tags:
                  - Get
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Get a Product Review
                description: >-
                  Returns a single *Product Review*. Optional parameters maybe
                  passed in.
              put:
                tags:
                  - Update
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Update a Product Review
                description: |-
                  Updates a *Product Review*.

                  **Required Fields**
                  * none

                  **Read-Only Fields**
                  * id
              delete:
                tags:
                  - Delete
                  - Product
                  - Review
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                summary: Delete a Product Review
                description: Deletes a *Product Review*.
              parameters:
                - null
                - null
                - null
            /catalog/products/channel-assignments:
              get:
                summary: Get Products Channel Assignments
                description: Returns a list of products channel assignments.
                tags:
                  - Get
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              put:
                summary: Create Products Channel Assignments
                description: Creates products channel assignments.
                tags:
                  - Create
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              delete:
                summary: Delete Products Channel Assignments
                description: >-
                  Delete products channel assignments. A filter must be
                  supplied.
                tags:
                  - Delete
                  - Products
                  - Channel
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
              parameters:
                - null
            /catalog/products/category-assignments:
              get:
                summary: Get Products Category Assignments
                description: Returns a list of products category assignments.
                tags:
                  - Get
                  - Products
                  - Category
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              put:
                summary: Create Products Category Assignments.
                description: Creates products category assignments.
                tags:
                  - Create
                  - Products
                  - Category
                  - Assignments.
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              delete:
                summary: Delete Products Category Assignments
                description: >-
                  Deletes products category assignments. A filter must be
                  supplied.
                tags:
                  - Delete
                  - Products
                  - Category
                  - Assignments
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
              parameters:
                - null
            /catalog/summary:
              get:
                tags:
                  - Get
                  - Catalog
                  - Summary
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                summary: Get a Catalog Summary
                description: >-
                  Returns a lightweight inventory summary from the BigCommerce
                  Catalog.


                  The inventory summary includes:

                  * "inventory_count"

                  * "variant_count"

                  * "inventory_value"

                  * "highest_variant_price"

                  * "average_variant_price"

                  * "lowest_variant_price"

                  * "oldest_variant_date"

                  * "newest_variant_date"

                  * "primary_category_id"

                  * "primary_category_name"
              parameters:
                - null
            /catalog/products/metafields:
              get:
                summary: Get All Product Metafields
                tags:
                  - Get
                  - All
                  - Product
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Get all product metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Update multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Catalog
                  - Products
                  - Product_id
                  - Images
                  - Image_id
                  - Videos
                  - Id
                  - Complex
                  - Rules
                  - Complex_rule_id
                  - Custom
                  - Fields
                  - Custom_field_id
                  - Bulk
                  - Pricing
                  - Bulk_pricing_rule_id
                  - Metafields
                  - Metafield_id
                  - Reviews
                  - Review_id
                  - Channel
                  - Assignments
                  - Category
                  - Summary
                description: Delete all product
    overlays:
      - type: APIs.io Search
        url: overlays/catalog-products-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/catalog-products-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:settings
    name: Settings
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
            title: Settings V3
          tags:
            - name: Email Statuses
            - name: Search Filters
            - name: Store Locale
            - name: Storefront Category
            - name: Storefront Robotstxt
            - name: Storefront Search
            - name: Storefront Security
            - name: Storefront SEO
            - name: Storefront Status
            - name: Analytics
            - name: Catalog
            - name: Inventory
            - name: Inventory Notifications
            - name: Logo
            - name: Logo Image
            - name: Favicon Image
            - name: Store Profile
            - name: Storefront Product
            - name: Units of Measurement
          paths:
            /settings/analytics:
              parameters:
                - null
              get:
                summary: Get All Web Analytics Providers
                description: Returns a list of web analytics providers.
                tags:
                  - Get
                  - All
                  - Web
                  - Analytics
                  - Providers
                  - Settings
                  - Analytics
            /settings/analytics/{id}:
              parameters:
                - null
                - null
              get:
                summary: Get a Web Analytics Provider
                description: >-
                  Returns a single web analytics provider data for a default
                  channel.
                tags:
                  - Get
                  - Web
                  - Analytics
                  - Provider
                  - Settings
                  - Analytics
                  - Id
              put:
                summary: Update a Web Analytics Provider
                description: >-
                  Updates a single web analytics provider data for a default
                  channel.
                tags:
                  - Update
                  - Web
                  - Analytics
                  - Provider
                  - Settings
                  - Analytics
                  - Id
            /settings/catalog:
              parameters:
                - null
              get:
                summary: Get Catalog Settings
                description: |-
                  Returns catalog settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Catalog
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
              put:
                summary: Update Catalog Settings
                description: |-
                  Updates catalog settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Catalog
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
            /settings/email-statuses:
              parameters:
                - null
              get:
                summary: Get Transactional Email Settings
                description: >-
                  Get global transactional email settings or channel specific
                  overrides by `channel_id`.
                tags:
                  - Get
                  - Transactional
                  - Email
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
              put:
                summary: Update Transactional Email Settings
                description: >-
                  Update global transactional email settings or create channel
                  specific overrides by `channel_id`.
                tags:
                  - Update
                  - Transactional
                  - Email
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
            /settings/favicon/image:
              parameters:
                - null
              post:
                summary: Create Favicon Image
                description: >-
                  Uploads an image file to use as the storefront favicon.
                  Supported MIME types include GIF, JPEG, and PNG. 

                    - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only.
                tags:
                  - Create
                  - Favicon
                  - Image
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
            /settings/inventory/notifications:
              parameters:
                - null
              get:
                summary: Get Inventory Notifications Settings
                description: >-
                  Returns inventory notification settings. 

                  * `channel_id` can be used as a query parameter to get
                  inventory notification settings per channel. If omitted, you
                  will interact with the global setting only.
                tags:
                  - Get
                  - Inventory
                  - Notifications
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
              put:
                summary: Update Inventory Notifications Settings
                description: >-
                  Updates inventory notification settings. 

                  * `channel_id` can be used as a query parameter to get
                  inventory notification settings per channel. If omitted, you
                  will interact with the global setting only. 

                  * Supplying `null` settings values per channel will delete
                  overrides per given channel and values will be inherited from
                  global level. 

                  * Partial updates are not supported within the given endpoint.
                  In order to delete overrides per channel, `null` should be
                  supplied for all the settings within the given endpoint.
                tags:
                  - Update
                  - Inventory
                  - Notifications
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
            /settings/logo:
              parameters:
                - null
              get:
                summary: Get Store Logo Settings
                description: |-
                  Returns store logo settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Store
                  - Logo
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
              put:
                summary: Update Store Logo Settings
                description: >-
                  Updates the logo type and logo text for a textual logo. To
                  upload new images, use the dedicated image POST endpoints.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Store
                  - Logo
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
            /settings/logo/image:
              parameters:
                - null
              post:
                summary: Create Logo Image
                description: >-
                  Uploads an image file to use as the storefront logo. Supported
                  MIME types include GIF, JPEG, and PNG. 

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only.
                tags:
                  - Create
                  - Logo
                  - Image
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
            /settings/search/filters:
              get:
                summary: Get Enabled Filters
                description: >-
                  Returns a list of enabled default [Product
                  Filtering](https://support.bigcommerce.com/s/article/Product-Filtering-Settings)
                  filters. These filters will be used if a store does not have
                  contextual overrides.
                tags:
                  - Get
                  - Enabled
                  - Filters
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
              put:
                summary: Update Enabled Filters
                description: >-
                  Updates enabled default [Product
                  Filtering](https://support.bigcommerce.com/s/article/Product-Filtering-Settings)
                  filters.
                tags:
                  - Update
                  - Enabled
                  - Filters
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
            /settings/search/filters/available:
              parameters:
                - null
              get:
                summary: Get Available Filters
                description: >-
                  Returns a list of filters available to power [Product
                  Filtering](https://support.bigcommerce.com/s/article/Product-Filtering-Settings).
                tags:
                  - Get
                  - Available
                  - Filters
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
            /settings/search/filters/contexts:
              parameters:
                - null
              get:
                summary: Get Contextual Filters
                description: >-
                  Returns a list of contextual filters enabled for a particular
                  channel or category.


                  **Usage Notes**


                  Contextual filters allow you to configure the enabled filters
                  per channel or category, so that shoppers can filter by the
                  most relevant criteria.


                  The order of the returned filters will match the sort order of
                  the filters on the storefront.
                tags:
                  - Get
                  - Contextual
                  - Filters
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
              put:
                summary: Upsert Contextual Filters
                description: >-
                  Upserts contextual filters for a particular channel or
                  category.


                  **Usage Notes**


                  Contextual filters allow you to configure the enabled filters
                  per channel or category, so that shoppers can filter by the
                  most relevant criteria.


                  You can change the order of the filters on the live site by
                  changing the order of the filters you send.
                tags:
                  - Upsert
                  - Contextual
                  - Filters
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
            /settings/store/locale:
              get:
                summary: Get Locale Settings
                description: Returns global locale settings.
                tags:
                  - Get
                  - Locale
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
              put:
                summary: Update Locale Settings
                description: Updates global locale settings.
                tags:
                  - Update
                  - Locale
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
            /settings/store/profile:
              parameters:
                - null
              get:
                summary: Get Store Profile Settings
                description: |-
                  Returns store profile settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Store
                  - Profile
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
              put:
                summary: Update Store Profile Settings
                description: |-
                  Updates store profile settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Store
                  - Profile
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
            /settings/storefront/category:
              parameters:
                - null
              get:
                summary: Get Storefront Category Settings
                description: |-
                  Returns category settings.

                   - Channel ID can be used as a query parameter for getting channel-specific settings. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Storefront
                  - Category
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
              put:
                summary: Update Storefront Category Settings
                description: |-
                  Updates category settings.

                   - Channel ID can be used as a query parameter for updating channel-specific settings. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Storefront
                  - Category
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
            /settings/storefront/product:
              parameters:
                - null
              get:
                summary: Get Storefront Product Settings
                description: |-
                  Returns product settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Storefront
                  - Product
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
              put:
                summary: Update Storefront Product Settings
                description: |-
                  Updates product settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Storefront
                  - Product
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
            /settings/storefront/robotstxt:
              parameters:
                - null
              get:
                summary: Get Robots.txt Settings
                description: |-
                  Returns Robots.txt settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Robots.txt
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
              put:
                summary: Update Robots.txt Settings
                description: |-
                  Updates Robots.txt settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Robots.txt
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
            /settings/storefront/search:
              parameters:
                - null
              get:
                summary: Get Storefront Search Settings
                description: |-
                  Returns search settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Storefront
                  - Search
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
              put:
                summary: Update Storefront Search Settings
                description: |-
                  Updates search settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Storefront
                  - Search
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
            /settings/storefront/security:
              parameters:
                - null
              get:
                summary: Get Storefront Security Settings
                description: |-
                  Returns security settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Storefront
                  - Security
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
              put:
                summary: Update Storefront Security Settings
                description: |-
                  Updates security settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Storefront
                  - Security
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
            /settings/storefront/seo:
              parameters:
                - null
              get:
                summary: Get Storefront SEO Settings
                description: |-
                  Returns SEO settings.

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Storefront
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
              put:
                summary: Update Storefront SEO Settings
                description: |-
                  Updates SEO settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Storefront
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
            /settings/storefront/status:
              parameters:
                - null
              get:
                summary: Get Storefront Status
                description: |-
                  Returns storefront status-related settings. 

                   - Channel ID can be used as a query parameter for getting channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` indicates that a particular field has not been overridden on a channel level when channel level settings are requested and values are inherited from global level.
                tags:
                  - Get
                  - Storefront
                  - Status
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
                  - Status
              put:
                summary: Update Storefront Status
                description: |-
                  Updates storefront status-related settings.

                   - Channel ID can be used as a query parameter for updating channel-specific setting. If omitted, you will interact with the global setting only. 

                   - `null` should be supplied to delete overrides per given channel and to inherit values from global level. Partial updates are not supported and all settings should be supplied with `null` value in order to delete overrides per channel.
                tags:
                  - Update
                  - Storefront
                  - Status
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
                  - Status
            /settings/inventory:
              parameters:
                - null
              get:
                summary: Get Inventory Settings
                tags:
                  - Get
                  - Inventory
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
                  - Status
                description: Get Inventory Settings
              put:
                summary: Update Inventory Settings
                tags:
                  - Update
                  - Inventory
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
                  - Status
                description: Update inventory settings
            /settings/store/units-of-measurement:
              get:
                summary: Get Units of Measurement Settings
                description: >-
                  Get settings for [units of
                  measurements](https://support.bigcommerce.com/s/article/Store-Settings?language=en_US#physical).
                tags:
                  - Get
                  - Units
                  - Of
                  - Measurement
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
                  - Status
                  - Units
                  - Of
                  - Measurement
              put:
                summary: Update Units of Measurement Settings
                description: >-
                  Update settings for [units of
                  measurements](https://support.bigcommerce.com/s/article/Store-Settings?language=en_US#physical).


                  The endpoint does not support partial updates. Provide all
                  fields to update global or channel-level settings.


                  Create channel-level settings, or overrides for a channel,
                  using the `channel_id`  query parameter. 


                  To delete overrides for a channel, supply `null` as a value
                  for all fields. A channel then inherits global values.


                  The endpoint does not support 'null' as a value for
                  global-level settings.
                tags:
                  - Update
                  - Units
                  - Of
                  - Measurement
                  - Settings
                  - Settings
                  - Analytics
                  - Id
                  - Catalog
                  - Email
                  - Statuses
                  - Favicon
                  - Image
                  - Inventory
                  - Notifications
                  - Logo
                  - Search
                  - Filters
                  - Available
                  - Contexts
                  - Store
                  - Locale
                  - Profile
                  - Storefront
                  - Category
                  - Product
                  - Robotstxt
                  - Security
                  - Seo
                  - Status
                  - Units
                  - Of
                  - Measureme
    overlays:
      - type: APIs.io Search
        url: overlays/settings-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/settings-openapi-api-evangelist-ratings.yml
  - name: FactSet Chart Generation Service
    description: >-
      An API for getting chart images in the form of png or jpg based on various
      parameters like ticker, benchmark, currency, frequency, start and end date
      etc.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/chart-generation-service
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/chart-generation-service#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/chart-generation-service#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/chart-generation-service#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/chart-generation-service#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/chart-generation-service#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Chart Generation Service
          paths:
            /v1/catalog/categories:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Chart
                  - Categories
                  - V1
                  - Catalog
                  - Categories
                summary: Get a list of chart categories
            /v1/catalog/charts:
              get:
                tags:
                  - Get
                  - List
                  - Of
                  - Chart
                  - Templates
                  - That
                  - Can
                  - Be
                  - Used
                  - For
                  - Getting
                  - The
                  - Image
                  - From
                  - Service.
                  - V1
                  - Catalog
                  - Categories
                  - Charts
                summary: >-
                  Get a list of chart templates that can be used for getting the
                  image from the service.
                description: >-
                  You can get all the charts present or can just get the
                  information by categories. The response includes the name of
                  the chart, description, tags and any additional input specific
                  to that chart. Use the information from this response to
                  determine what charts you want and get its image from /images
                  endpoint. Additionally you can also get back a auto generated
                  PDF for the categories you requested for.
            /v1/image:
              get:
                tags:
                  - Get
                  - Chart
                  - Image
                  - Back
                  - In
                  - V1
                  - Catalog
                  - Categories
                  - Charts
                  - Image
                summary: Get chart image back
    overlays:
      - type: APIs.io Search
        url: overlays/ chart-generation-service-openapi-search.yml
      - type: APIs.io Search
        url: overlays/chart-generation-service-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chart-generation-service-openapi-api-evangelist-ratings.yml
    aid: factset:factset-chart-generation-service
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---