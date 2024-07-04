---
name: Alerting
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/alerting.png
url: https://example.com/apis/alerting.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Alerting
apis:
  - name: FactSet Real-Time Price Alerting API
    description: >-
      Basic Price Alerting deals with generation of alerts based on current
      price data. Users can define an upper or lower limit and choose on which
      price type those limit conditions apply.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/real-time-price-alerting-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/real-time-price-alerting-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Price Alerting API For Digital Portals
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /alerting/prices/basic/alert/get:
              get:
                tags:
                  - Details
                  - Of
                  - An
                  - Alert.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                description: >-
                  Details of an alert. The details include the trigger
                  definition at the time of alert creation.
                summary: Details of an alert.
            /alerting/prices/basic/alert/list:
              get:
                tags:
                  - List
                  - Of
                  - Alerts.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                  - List
                description: List of alerts in descending order of creation.
                summary: List of alerts.
            /alerting/prices/basic/trigger/get:
              get:
                tags:
                  - Details
                  - Of
                  - Trigger.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                  - List
                  - Trigger
                description: Details of a trigger.
                summary: Details of a trigger.
            /alerting/prices/basic/trigger/list:
              post:
                tags:
                  - List
                  - Of
                  - Triggers.
                  - Alerting
                  - Prices
                  - Basic
                  - Alert
                  - Get
                  - List
                  - Trigger
                description: >-
                  Returns a list of triggers sorted in descending order of
                  creation.
                summary: List of triggers.
          tags:
            - name: alerting
              description: alerting endpoints
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/
          x-interface-version: 2
          x-documenter-version: 6.3.9
          x-api-version: null
    overlays:
      - type: APIs.io Search
        url: overlays/real-time-price-alerting-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/real-time-price-alerting-openapi-api-evangelist-ratings.yml
    aid: factset:factset-real-time-price-alerting-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---