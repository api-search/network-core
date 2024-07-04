---
name: Cascade
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/cascade.png
url: https://example.com/apis/cascade.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Cascade
apis:
  - aid: box:box-metadata-cascade-policies-api
    name: Box Metadata Cascade Policies API
    description: Needs a description
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.box.com/
    baseURL: https://api.example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.box.com/
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: Box Metadata Cascade Policies API
          paths:
            /metadata_cascade_policies:
              get:
                summary: List metadata cascade policies
                tags:
                  - List
                  - Metadata
                  - Cascade
                  - Policies
                  - Metadata_cascade_policies
                description: >-
                  Retrieves a list of all the metadata cascade policies

                  that are applied to a given folder. This can not be used on
                  the root

                  folder with ID `0`.
              post:
                summary: Create metadata cascade policy
                tags:
                  - Create
                  - Metadata
                  - Cascade
                  - Policy
                  - Metadata_cascade_policies
                description: >-
                  Creates a new metadata cascade policy that applies a given

                  metadata template to a given folder and automatically

                  cascades it down to any files within that folder.


                  In order for the policy to be applied a metadata instance must
                  first

                  be applied to the folder the policy is to be applied to.
            /metadata_cascade_policies/{metadata_cascade_policy_id}:
              get:
                summary: Get metadata cascade policy
                tags:
                  - Get
                  - Metadata
                  - Cascade
                  - Policy
                  - Metadata_cascade_policies
                  - Metadata_cascade_policy_id
                description: >-
                  Retrieve a specific metadata cascade policy assigned to a
                  folder.
              delete:
                summary: Remove metadata cascade policy
                tags:
                  - Remove
                  - Metadata
                  - Cascade
                  - Policy
                  - Metadata_cascade_policies
                  - Metadata_cascade_policy_id
                description: Deletes a metadata cascade policy.
            /metadata_cascade_policies/{metadata_cascade_policy_id}/apply:
              post:
                summary: Force-apply metadata cascade policy to folder
                tags:
                  - Force-apply
                  - Metadata
                  - Cascade
                  - Policy
                  - To
                  - Folder
                  - Metadata_cascade_policies
                  - Metadata_cascade_policy_id
                  - Apply
                description: >-
                  Force the metadata on a folder with a metadata cascade policy
                  to be applied to

                  all of its children. This can be used after creating a new
                  cascade policy to

                  enforce the metadata to be cascaded down to all existing files
                  within 
    overlays:
      - type: APIs.io Search
        url: overlays/metadata-cascade-policies-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/metadata-cascade-policies-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---