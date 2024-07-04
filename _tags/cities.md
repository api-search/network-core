---
name: Cities
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cities.png
url: https://example.com/apis/cities.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cities
apis:
  - aid: amadeus:city-search
    name: City Search
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developers.amadeus.com
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developers.amadeus.com
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: City Search
          paths:
            /reference-data/locations/cities:
              get:
                summary: GET Cities by keyword
                tags:
                  - Cities
                  - By
                  - Keywords
                  - References
                  - Data
                  - Locations
                  - Cities
                description: null
    overlays:
      - type: APIs.io Search
        url: overlays/city-search-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/city-search-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---