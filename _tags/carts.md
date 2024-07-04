---
name: Carts
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/carts.png
url: https://example.com/apis/carts.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Carts
apis:
  - aid: bigcommerce:abandoned-carts
    name: Abandoned Carts
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
            version: ''
            title: Abandoned Carts
          tags:
            - name: Abandoned Carts
            - name: Abandoned Cart Settings
            - name: Abandoned Carts Settings
          paths:
            /abandoned-carts/settings:
              get:
                summary: Get Global Abandoned Cart Settings
                description: Returns the global abandoned cart settings of a store.
                tags:
                  - Get
                  - Global
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
              put:
                summary: Update Global Abandoned Cart Settings
                description: Updates the global abandoned cart settings of a store.
                tags:
                  - Update
                  - Global
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
              parameters:
                - null
            /abandoned-carts/settings/channels/{channel_id}:
              get:
                summary: Get Channel Abandoned Cart Settings
                description: >-
                  Returns the per-channel overrides for the abandoned cart
                  settings of a store.
                tags:
                  - Get
                  - Channel
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Abandoned Cart Settings
                description: >-
                  Updates the per-channel overrides for the abandoned cart
                  settings of a store.


                  #### OAuth Scopes

                  | UI Name                                      | Permission |
                  Parameter                                     |

                  |-||--|     

                  | Information & Settings                       | modify     |
                  `store_v2_information`                        |
                tags:
                  - Update
                  - Channel
                  - Abandoned
                  - Cart
                  - Settings
                  - Abandoned
                  - Carts
                  - Settings
                  - Channels
                  - Channel_id
              parameters:
                - null
                - null
            /abandoned-carts/{token}:
              get:
                summary: Get an Abandoned Cart
                description: >-
                  Returns the `cart_id` corresponding to the abandoned cart
                  `{token}` passed in.


                  **Usage Notes**:

                  * `{token}` is the token in the query string of the abandoned
                  cart link found in abandoned cart email notifications to
                  shoppers
                tags:
                  - Get
                  - An
                  - Abandoned
                  - Cart
                  - Abandoned
                  - Carts
                  - Settings
                  - Channels
                  - Channel_id
                  - Token
              parameters:
                - null
                - null
    overlays:
      - type: APIs.io Search
        url: overlays/abandoned-carts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/abandoned-carts-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:storefront-carts
    name: Storefront Carts
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
            title: Storefront Carts
          tags:
            - name: Cart
            - name: Cart Items
            - name: Cart Currency
          paths:
            /carts:
              get:
                tags:
                  - Get
                  - Cart
                  - Carts
                summary: Get a Cart
                description: >-
                  Returns a *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
              post:
                tags:
                  - Create
                  - Cart
                  - Carts
                summary: Create a Cart
                description: >-
                  Creates a *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /carts/{cartId}:
              delete:
                tags:
                  - Delete
                  - Cart
                  - Carts
                  - Id
                summary: Delete a Cart
                description: >-
                  Deletes a *Cart*. Once a *Cart* has been deleted it can not be
                  recovered.



                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /carts/{cartId}/items:
              post:
                tags:
                  - Add
                  - Cart
                  - Line
                  - Items
                  - Carts
                  - Id
                  - Items
                summary: Add Cart Line Items
                description: >-
                  Adds a line items to the *Cart*.


                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
            /carts/{cartId}/items/{itemId}:
              put:
                tags:
                  - Update
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Item
                summary: Update Cart Line Item
                description: >-
                  Updates a *Cart* line item. Updates an existing, single line
                  item quantity and the price of custom items in a cart.


                  If a modified product or variant needs to be changed or
                  updated, you can remove and re-add the product to the cart
                  with the correct variants using the [Delete Cart Line
                  Item](/docs/rest-storefront/carts/cart-items#delete-cart-line-item)
                  and the [Add Cart Line
                  Items](/docs/rest-storefront/carts/cart-items#add-cart-line-items)
                  endpoints. You can also use carts mutations that are part of
                  the [GraphQL Storefront
                  API](/docs/storefront/cart-checkout/guide/graphql-storefront).



                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint. 

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
              delete:
                tags:
                  - Delete
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Item
                summary: Delete Cart Line Item
                description: >-
                  Deletes a *Cart* line item.


                  Removing the last `line_item` in the *Cart* deletes the
                  *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /carts/{cartId}/currency:
              post:
                tags:
                  - Update
                  - Cart
                  - Currency
                  - Carts
                  - Id
                  - Items
                  - Item
                  - Currency
                summary: Update Cart Currency
                description: >-
                  Update currency of the *Cart*. 

                  Promotions and gift certificates that don't apply to the new
                  currency will be removed from your cart.

                  You cannot update the cart currency if the draft order cart or
                  the cart contains a manual discount.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this
    overlays:
      - type: APIs.io Search
        url: overlays/storefront-carts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storefront-carts-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:carts
    name: Carts
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
            title: Carts
            version: ''
          tags:
            - name: Carts (Single)
            - name: Items
            - name: Redirects
            - name: Settings
            - name: Metafields
            - name: Batch metafields
          paths:
            /carts:
              parameters:
                - null
              post:
                description: >-
                  Creates a **Cart**. 


                  **Required Fields**


                  |Field|Details|

                  |-|-|

                  |`line_item`|Specifies a line item.| 

                  |`custom_items`|Specifies a custom item. Only required if
                  adding a custom item to the cart.|

                  |`gift_certificates`|Specifies a gift certificate. Only
                  required if adding a gift certificate to the cart.|


                  **Usage Notes**


                  * A **cart** `id` (UUID) is returned in the response.

                  * A **cart** `id` is the same as a **checkout** `id`.

                  * A cart can be created by adding an existing **catalog item**
                  or a **custom item**.

                  * Carts are valid for **30 days** from the **last
                  modification** (this includes creating the cart or editing the
                  cart).

                  * If a product has modifiers, use the `option_selections`
                  array to describe the **modifier** selection(s).

                  * The format and data type of a cart’s `option_value` are
                  defined by the `value_data` object of a product’s [variant
                  option
                  value](/docs/rest-catalog/product-variant-options/values),
                  [modifier value](/docs/rest-catalog/product-modifiers/values),
                  or a combination of both.

                  * Redirect URLs can only be generated from carts that were
                  created using the **REST Management API**. 

                  * To get cart `redirect_urls` in the response, append the
                  following query parameter to the request URL:
                  `include=redirect_urls`. Redirect URLs point to either a
                  shared checkout domain or a channel-specific domain, depending
                  on the storefront configuration.

                  * To restore a cart that was created by a shopper or through a
                  Storefront API, first recreate the cart using the **REST
                  Management API**.

                  * To get cart `promotions` in the response, append the
                  following query parameter to the request URL:
                  `include=promotions.banners`.
                tags:
                  - Create
                  - Cart
                  - Carts
                summary: Create a Cart
            /carts/{cartId}/items:
              parameters:
                - null
                - null
                - null
              post:
                description: >-
                  Adds line item to the *Cart*.


                  **Usage Notes**


                  To add a custom item use `custom_items`. 


                  Overriding a product’s `list_price` will make that item
                  ineligible for V3 product level promotions.


                  If a product has modifiers, omit the `variant_id` and instead
                  use the `option_selections` array to describe both the
                  **variant** and the **modifier** selections.


                  Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
                tags:
                  - Add
                  - Cart
                  - Line
                  - Items
                  - Carts
                  - Id
                  - Items
                summary: Add Cart Line Items
            /carts/{cartId}/redirect_urls:
              parameters:
                - null
                - null
                - null
              post:
                description: >-
                  Creates a **Cart** redirect URL for redirecting a shopper to
                  an already created cart using the `cartId`.


                  **Usage Notes**


                  * Redirect URLs can also be created with **Create a Cart**
                  requests by appending `include=redirect_urls`.

                  * A **Carts** redirect URL may only be used once.

                  * Redirect URLs point to either a shared checkout domain or a
                  channel-specific domain, depending on the storefront
                  configuration.

                  * Once a redirect URL has been visited, it will be invalidated
                  and cannot be used again. 

                  * If your application requires URLs to be visited more than
                  once, consider generating a fresh one each time you need to
                  restore a cart, and redirecting to the URL from your own
                  application.

                  * Redirect URLs can be generated only from carts that were
                  created using the **REST Management API**. 

                  * To restore a cart that was created on the storefront, either
                  by a shopper or a Storefront API, first recreate the cart
                  using the **REST Management API**.

                  * When redirecting the shopper, you can add a set of
                  `query_params` to the URL. The `query_params` feature allows
                  passing additional information to the redirect URL.
                tags:
                  - Create
                  - Cart
                  - Redirect
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                summary: Create Cart Redirect URL
            /carts/{cartId}/items/{itemId}:
              parameters:
                - null
                - null
                - null
              put:
                description: >-
                  Updates an existing, single line item in the *Cart*. 


                  **Notes**


                  Currently, only updating `list_price` and `quantity` are
                  supported. Updating a product’s `list_price` will make that
                  item ineligible for V3 product-level promotions. 


                  If the product has modifiers, omit the `variant_id` and
                  instead use the `option_selections` array to describe both the
                  **variant** and the **modifier** selections.


                  If a variant needs to be changed or updated, the product will
                  need to be removed and re-added to the cart with the correct
                  variants using the **Add Cart Line Items** endpoint.


                  `custom_items` cannot be updated via the API at this time. To
                  update your cart, add a new updated custom item and delete the
                  outdated one. If your cart contains only one line item,
                  perform the add operation before the delete operation.


                  Deleting all line items from the cart will invalidate the
                  cart. 


                  Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
                tags:
                  - Update
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Update Cart Line Item
              delete:
                description: >-
                  Deletes a *Cart* line item. 


                  **Notes**


                  Removing the last `line_item` in the *Cart* deletes the
                  *Cart*.
                tags:
                  - Delete
                  - Cart
                  - Line
                  - Item
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Delete Cart Line Item
            /carts/{cartId}:
              parameters:
                - null
                - null
              get:
                description: Returns a storeʼs *Cart*.
                tags:
                  - Get
                  - Cart
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Get a Cart
              put:
                description: >-
                  Updates a *Cartʼs* `customer_id`.


                  **Notes**


                  Changing the *Cart* `customer_id` will remove any promotions
                  or shipping calculations on the *Cart*. These are tied to the
                  customer depending on cart conditions and any customer
                  groups. 
                tags:
                  - Update
                  - Customer
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Update Customer ID
              delete:
                description: >-
                  Deletes a *Cart*. Once a *Cart* has been deleted it can’t be
                  recovered.
                tags:
                  - Delete
                  - Cart
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                summary: Delete a Cart
            /carts/settings:
              parameters:
                - null
              get:
                summary: Get Global Cart Settings
                description: Returns the global cart settings of a store.
                tags:
                  - Get
                  - Global
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
              put:
                summary: Update Global Cart Settings
                description: Update the global cart settings of a store.
                tags:
                  - Update
                  - Global
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
            /carts/settings/channels/{channel_id}:
              parameters:
                - null
                - null
              get:
                summary: Get Channel Cart Settings
                description: >-
                  Returns the per-channel overrides for the cart settings of a
                  store.
                tags:
                  - Get
                  - Channel
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
              put:
                summary: Update Channel Cart Settings
                description: >-
                  Update the per-channel overrides for the cart settings of a
                  store.
                tags:
                  - Update
                  - Channel
                  - Cart
                  - Settings
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
            /carts/{cart_id}/metafields:
              parameters:
                - null
                - null
              get:
                summary: Get Cart Metafields
                tags:
                  - Get
                  - Cart
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                description: Get a cart's metafields.
              post:
                summary: Create a Cart Metafield
                tags:
                  - Create
                  - Cart
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                description: >
                  Create a cart `Metafield`. 


                  If you create an order from a Cart, you can continue
                  referencing the Cart Metafields even if you delete the
                  original Cart. Use the `cart_id` field on the Order to
                  construct the Cart Metafield endpoint. 
            /carts/{cart_id}/metafields/{metafield_id}:
              get:
                summary: Get a Cart Metafield
                tags:
                  - Get
                  - Cart
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Gets a cart metafield.
              put:
                summary: Update a Cart Metafield
                tags:
                  - Update
                  - Cart
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: |
                  Update a `Metafield`, by `cart_id`.
              delete:
                summary: Delete a Metafield
                tags:
                  - Delete
                  - Metafield
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: |
                  Deletes a `Metafield`.
              parameters:
                - null
                - null
                - null
            /carts/metafields:
              get:
                summary: Get All Cart Metafields
                tags:
                  - Get
                  - All
                  - Cart
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Get all cart metafields.
              post:
                summary: Create multiple Metafields
                tags:
                  - Create
                  - Multiple
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              put:
                summary: Update multiple Metafields
                tags:
                  - Update
                  - Multiple
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Create multiple metafields.
              delete:
                summary: Delete All Metafields
                tags:
                  - Delete
                  - All
                  - Metafields
                  - Carts
                  - Id
                  - Items
                  - Redirect_urls
                  - Item
                  - Settings
                  - Channels
                  - Channel_id
                  - Cart_id
                  - Metafields
                  - Metafield_id
                description: Delete all cart
    overlays:
      - type: APIs.io Search
        url: overlays/carts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/carts-openapi-api-evangelist-ratings.yml
  - aid: bigcommerce:storefront-checkouts
    name: Storefront Checkouts
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
            title: Storefront Checkouts
            version: ''
          tags:
            - name: Checkout
            - name: Checkout Billing Address
            - name: Checkout Cart Items
            - name: Checkout Consignments
            - name: Checkout Coupons
            - name: Checkout Gift Certificates
            - name: Checkout Spam Protection
            - name: Checkout Store Credit
          paths:
            /checkouts/{checkoutId}:
              get:
                tags:
                  - Get
                  - Checkout
                  - Id
                summary: Get a Checkout
                description: >-
                  Returns a *Checkout*.


                  The cart ID and checkout ID are the same.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
              put:
                tags:
                  - Update
                  - Customer
                  - Messages
                  - Id
                summary: Update Customer Messages
                description: >-
                  Updates *Checkout* customer messages.


                  **Limits**


                  * 2000 character limit


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/carts/{cartId}/items/{itemId}:
              put:
                tags:
                  - Update
                  - Line
                  - Item
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                summary: Update a Line Item
                description: >-
                  Updates a *Checkout Line Item*. Updates an existing, single
                  line item in the cart.


                  If a variant needs to be changed or updated, the product will
                  need to be removed and re-added to the cart with the correct
                  variants using the [Add Cart Line
                  Items](/docs/rest-storefront/carts/cart-items#add-cart-line-items)
                  endpoint or the [GraphQL Storefront
                  API](/docs/storefront/cart-checkout/guide/graphql-storefront).


                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
              delete:
                tags:
                  - Delete
                  - Line
                  - Item
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                summary: Delete a Line Item
                description: >-
                  Deletes a *Line Item* from the *Cart*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/billing-address:
              post:
                tags:
                  - Add
                  - Checkout
                  - Billing
                  - Address
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                summary: Add Checkout Billing Address
                description: >-
                  Adds a billing address to an existing *Checkout*.


                  **Required Fields**

                  * country_code



                  > #### Note

                  > * The `email` property is only required if the customer is a
                  guest shopper. Otherwise, it is set automatically.

                  > * Sending `email` property as a payload in POST request
                  triggers the abandoned cart notification process.

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/billing-address/{addressId}:
              put:
                tags:
                  - Update
                  - Checkout
                  - Billing
                  - Address
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                summary: Update Checkout Billing Address
                description: >-
                  Updates an existing billing address on *Checkout*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/consignments:
              post:
                tags:
                  - Create
                  - Consignment
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                summary: Create a Consignment
                description: >
                  Adds a new *Consignment* to *Checkout*.


                  Perform the following two steps to define the fulfillment of
                  the items in the cart.
                    ### For **shipping** consignments:
                      1. Add a new Consignment to Checkout.
                          * Send a `POST` request to `/consignments` with each shipping address, line item IDs, and quantities. Each address can have its own line item IDs.
                          * Provide a full valid customer address before placing the order. If provided, the order placement will succeed. 
                          * As part of the request URL make sure to add `include=consignments.availableShippingOptions` to return the available shipping options based on the items, the address, and the shipping location. This will return `availableShippingOptions` in the response.

                        * Required Fields:
                          * `shipping_address` (deprecated) or `address`
                          * `lineItems`
                      2. Update the Consignment with Shipping Options using the [REST Storefront API](/checkouts/checkout-consignments#update-a-consignment), the [REST Management API](/docs/rest-management/checkouts/checkout-consignments#update-checkout-consignment) or the [GraphQL Storefront API](/docs/storefront/cart-checkout/guide/graphql-storefront).
                            
                    ### For **pickup** consignments:
                      1. Create a new consignment object. 
                        - Send a `POST` request to `/consignments` with line item IDs and quantities.
                        - Provide a `pickupMethodId`. This is the `id` of the Pickup Method provided in the response body of the Storefront Pickup Options API.
                        - Required Fields:
                            * `pickupOption`
                            * `lineItems`

                  To learn more about creating a Checkout Consignment, see the
                  [Carts and Checkouts
                  Tutorial](/docs/storefront/cart-checkout/guide/rest-storefront).


                  > #### Notes

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
            /checkouts/{checkoutId}/consignments/{consignmentId}:
              put:
                tags:
                  - Update
                  - Consignment
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                summary: Update a Consignment
                description: >-
                  Updates an existing consignment. An update is either one of
                  the following:


                  1. Updates the consignment address and/or line items.

                  2. Selects a specific fulfillment option.


                  ### Update the consignment address and line items

                  For this type of update, the payload is the same as when
                  creating a new consignment.         Update each *Consignment*
                  `shippingOptionId` (shipping address and line items) with the
                  `availableShippingOption > id` from the POST `/consignment`
                  response. 


                  **Note:**

                  Updating a consignment could invalidate the value for
                  `selectedShippingOption` and `selectedPickupOption`.


                  ### Select a specific fulfillment option

                  Before placing an order, each consignment must have a
                  `selectedShippingOption` or a `selectedPickupOption`.


                  If the consignment already has a pick-up option selected and a
                  shipping option is provided, the pick-up option will be
                  deselected and the shipping option will be selected instead
                  (and vice versa). The `PUT` request will fail if it contains a
                  shipping option ID and a pickup option ID.


                  Required Fields:

                  * `shippingOptionId` or `pickupOptionId`

                  * `lineItems`


                  To learn more about creating a Checkout Consignment see
                  [Checkout Consignment
                  API](/docs/storefront/cart-checkout/guide/consignments).


                  > #### Notes

                  > * You cannot pass both an `address` and a `shippingOptionId`
                  because the shipping option may not be available for the new
                  address 

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  

                  > * Please note that this API endpoint is not concurrent safe,
                  meaning multiple simultaneous requests could result in
                  unexpected and inconsistent results.
              delete:
                tags:
                  - Delete
                  - Consignment
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                summary: Delete a Consignment
                description: >-
                  Removes an existing *Consignment* from *Checkout*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/gift-certificates:
              post:
                tags:
                  - Add
                  - Gift
                  - Certificate
                  - To
                  - Checkout
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                summary: Add Gift Certificate to Checkout
                description: >-
                  Adds a *Gift Certificate Code* to *Checkout*.


                  > #### Note

                  > * *Gift Certificates* are treated as a payment methods.

                  > * You are not able to purchase a gift certificate with a
                  gift certificate.

                  > * The rate limit is 20/hour (only for unique
                  gift-certificate codes).

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/gift-certificates/{giftCertificateCode}:
              delete:
                tags:
                  - Delete
                  - Gift
                  - Certificate
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                summary: Delete Gift Certificate
                description: >-
                  Deletes an existing *Gift Certificate*.


                  This removes the *Gift Certificate* payment method.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/coupons:
              post:
                tags:
                  - Add
                  - Coupon
                  - To
                  - Checkout
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                summary: Add Coupon to Checkout
                description: >-
                  Adds a *Coupon Code* to *Checkout*.


                  **Required Fields**

                  * couponCode


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/coupons/{couponCode}:
              delete:
                tags:
                  - Delete
                  - Checkout
                  - Coupon
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                summary: Delete Checkout Coupon
                description: >
                  Deletes a *Coupon Code* from *Checkout*.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/store-credit:
              post:
                tags:
                  - Add
                  - Store
                  - Credit
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                  - Store
                  - Credit
                summary: Add Store Credit
                description: >-
                  Applies any available store credit to a checkout. As on the
                  storefront, all available store credit will be used (up to the
                  value of the order) and no amount need be specified.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.
              delete:
                tags:
                  - Remove
                  - Store
                  - Credit
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                  - Store
                  - Credit
                summary: Remove Store Credit
                description: >-
                  Removes store credit from a checkout.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this endpoint.  
            /checkouts/{checkoutId}/spam-protection:
              post:
                tags:
                  - Checkout
                  - Spam
                  - Protection
                  - Id
                  - Carts
                  - Cart
                  - Items
                  - Item
                  - Billing
                  - Address
                  - Consignments
                  - Consignment
                  - Gift
                  - Certificates
                  - Certificate
                  - Code
                  - Coupons
                  - Coupon
                  - Store
                  - Credit
                  - Spam
                  - Protection
                summary: Checkout Spam Protection
                description: >-
                  Verifies if checkout is created by human.


                  > #### Note

                  > * Substitute your storefront domain for
                  `yourstore.example.com`. 

                  > * The Send a Test Request feature is not currently supported
                  for this
    overlays:
      - type: APIs.io Search
        url: overlays/storefront-checkouts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storefront-checkouts-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---