---
name: Chunks
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/chunks.png
url: https://example.com/apis/chunks.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Chunks
apis:
  - name: backupstorage
    description: The frontend service for Cryo Storage.
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
            title: backupstorage
          paths:
            /backup-jobs/{jobId}/object/{objectName}:
              PUT:
                summary: StartObject
                description: Start upload containing one or many chunks.
                tags:
                  - Start
                  - Objects
                  - Identifiers
                  - Objects
                  - Names
            /restore-jobs/{jobId}/chunk/{chunkToken}:
              GET:
                summary: GetChunk
                description: Gets the specified object's chunk.
                tags:
                  - Get
                  - Chunks
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
            /restore-jobs/{jobId}/object/{objectToken}/metadata:
              GET:
                summary: GetObjectMetadata
                description: Get metadata associated with an Object.
                tags:
                  - Get
                  - Objects
                  - Metadata
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
                  - Metadata
            /restore-jobs/{jobId}/chunks/{objectToken}/list:
              GET:
                summary: ListChunks
                description: List chunks in a given Object
                tags:
                  - Lists
                  - Chunks
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
                  - Metadata
                  - Chunks
                  - Lists
            /restore-jobs/{jobId}/objects/list:
              GET:
                summary: ListObjects
                description: List all Objects in a given Backup.
                tags:
                  - Lists
                  - Objects
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
                  - Metadata
                  - Chunks
                  - Lists
                  - Objects
            /backup-jobs/{jobId}/object/{uploadId}/complete:
              PUT:
                summary: NotifyObjectComplete
                description: Complete upload
                tags:
                  - Notify
                  - Objects
                  - Complete
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
                  - Metadata
                  - Chunks
                  - Lists
                  - Objects
                  - Uploads
                  - Complete
            /backup-jobs/{jobId}/chunk/{uploadId}/{chunkIndex}:
              PUT:
                summary: PutChunk
                description: Upload chunk.
                tags:
                  - Put
                  - Chunks
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
                  - Metadata
                  - Chunks
                  - Lists
                  - Objects
                  - Uploads
                  - Complete
                  - Index
            /backup-jobs/{jobId}/object/{objectName}/put-object:
              PUT:
                summary: PutObject
                description: >-
                  Upload object that can store object metadata String and data
                  blob in single API call using inline ch
                tags:
                  - Put
                  - Objects
                  - Identifiers
                  - Objects
                  - Names
                  - Chunks
                  - Tokens
                  - Metadata
                  - Chunks
                  - Lists
                  - Objects
                  - Uploads
                  - Complete
                  - Index
                  - P
    overlays:
      - type: APIs.io Search
        url: overlays/backupstorage-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/backupstorage-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:backupstorage
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---