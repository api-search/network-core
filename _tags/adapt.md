---
name: Adapt
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/adapt.png
url: https://example.com/apis/adapt.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Adapt
apis:
  - name: textract
    description: >-
      <p>Amazon Textract detects and analyzes text in documents and converts it
      into machine-readable text. This is the API reference documentation for
      Amazon Textract.</p>
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
            title: textract
          paths:
            /:
              POST:
                summary: UpdateAdapter
                description: >-
                  <p>Update the configuration for an adapter. FeatureTypes
                  configurations cannot be updated. At least one new parameter
                  must be specified as an arg
                tags:
                  - Update
                  - Adapt
    overlays:
      - type: APIs.io Search
        url: overlays/textract-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/textract-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:textract
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---