---
name: Capital Structure
description: Needs a description.
image: >-
  https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/capital-structure.png
url: https://example.com/apis/capital-structure.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Capital Structure
apis:
  - name: FactSet Capital Structure Report Builder API
    description: >-
      Curated data from multiple sources for comprehensive capital analysis
      reports
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/capital-structure-report-builder-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/capital-structure-report-builder-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.3
          info:
            title: FactSet Capital Structure Report Builder API
            description: ''
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          externalDocs:
            description: Read more about STACH 2.0's row organized schema
            url: https://factset.github.io/stachschema/#/v2/RowOrganized
          tags:
            - name: Capital Structure
          paths:
            /dcs-detail:
              get:
                tags:
                  - Debt
                  - Capital
                  - Structure
                  - S)
                  - Dcs
                  - Detail
                summary: Debt Capital Structure (DCS)
            /source-of-capital:
              get:
                tags:
                  - Source
                  - Of
                  - Capital
                  - Dcs
                  - Detail
                  - Source
                  - Of
                  - Capital
                summary: Source of Capital
            /dcs-summary:
              get:
                tags:
                  - Debt
                  - Capital
                  - Struc
                  - Dcs
                  - Detail
                  - Source
                  - Of
                  - Capital
                  - Summary
                summary: Debt Capital Str
    overlays:
      - type: APIs.io Search
        url: overlays/capital-structure-report-builder-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/capital-structure-report-builder-openapi-api-evangelist-ratings.yml
    aid: factset:factset-capital-structure-report-builder-api
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---