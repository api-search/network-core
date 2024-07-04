---
name: Chart Templates
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/chart-templates.png
url: https://example.com/apis/chart-templates.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Chart Templates
apis:
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