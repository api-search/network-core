---
name: Climate
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/climate.png
url: https://example.com/apis/climate.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Climate
apis:
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
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---