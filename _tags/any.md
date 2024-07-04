---
name: Any
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/any.png
url: https://example.com/apis/any.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Any
apis:
  - name: Relay Delivery
    description: >-
      Through this API and hooks you are able to send delivery jobs to any valid
      address. Additionally, you are able to request quotes for pricing and
      duration estimates before creating a delivery job. Restaurants are not
      billed and instead the Platform is billed.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.relay.delivery/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://docs.relay.delivery/api/v2.html
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Relay Delivery
            description: ''
          tags:
            - name: Orders
              description: Manage delivery and pickup orders.
            - name: Quotes
              description: >-
                Manage delivery estimates and pricing before initiating a
                delivery.
          paths:
            /order:
              post:
                tags:
                  - Create
                  - New
                  - Delivery
                  - Or
                  - Pickup
                  - Order.
                  - Order
                summary: Create a new delivery or pickup order.
                description: ''
            /order/{orderKey}:
              patch:
                tags:
                  - Make
                  - Changes
                  - To
                  - An
                  - Active
                  - Order.
                  - Order
                  - Key
                summary: Make changes to an active order.
                description: >-
                  Some fields of the order may be updated. See
                  /schemas/platform-order-update-request.html
              get:
                tags:
                  - Fetch
                  - An
                  - Order.
                  - Order
                  - Key
                summary: Fetch an order.
                description: >-
                  Review order details and hooks. Polling this method is not
                  expected. You should rely on the webhooks to recieve updates.
            /quote:
              post:
                tags:
                  - Request
                  - New
                  - Quote
                  - Order
                  - Key
                  - Quote
                summary: Request a new quote
                description: ''
            /quote/{quoteKey}:
              get:
                tags:
                  - Fetch
                  - Previously
                  - Created
                  - Quote.
                  - Order
                  - Key
                  - Quote
                summary: Fetch a previously created quote.
                description: >-
                  If you created a quote a in the past and you want to check if
                  the quote is still valid then you can attempt to fetch it by
                  the quote key. If the quote is no longer valid then it will
                  not be found. If you are using your quotes right away then
                  there is no need to call this route.
            /delivery-zone:
              post:
                tags:
                  - Retrieve
                  - The
                  - Delivery
                  - Zone
                  - For
                  - Any
                  - Address
                  - Order
                  - Key
                  - Quote
                  - Delivery
                  - Zone
                summary: Retrieve the delivery zone for any address
                description: >-
                  Relay's maximum possible operating zone for a specific
                  address. Orders outside of this range will never be accepted.
            /order/ready:
              post:
                tags:
                  - Toggle
                  - The
                  - Ready
                  - Status
                  - Of
                  - An
                  - Order.
                  - Order
                  - Key
                  - Quote
                  - Delivery
                  - Zone
                  - Ready
                summary: Toggle the ready status of an order.
                description: >-
                  If you have an event for when an order is ready to be picked
                  up then you can use this route to dramatically improve the
                  quality of service your orders receive on the Relay Platform.
                  Be sure to set `requireReadyEvent` to true when creating the
                  order if you intend to use this method.
            /order/void:
              post:
                tags:
                  - Void/cancel
                  - An
                  - Order
                  - Order
                  - Key
                  - Quote
                  - Delivery
                  - Zone
                  - Ready
                  - Void
                summary: Void/cancel an Order
                description: >-
                  Cancel an order when a customer no longer wants an order.
                  Voiding an order should be extremely rare and excessive
                  voiding is
    overlays:
      - type: APIs.io Search
        url: overlays/relay-delivery-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/relay-delivery-openapi-api-evangelist-ratings.yml
    aid: relay-delivery:relay-delivery
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---