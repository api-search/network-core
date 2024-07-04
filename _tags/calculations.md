---
name: Calculations
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/calculations.png
url: https://example.com/apis/calculations.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Calculations
apis:
  - name: Factset PA Engine API
    description: >-
      Through the PA Engine API, request analytics for multi-asset class
      performance, attribution, and risk, including the flexibility of choosing
      your portfolio, benchmark, return period, and more.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/pa-engine-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/pa-engine-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/pa-engine-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/pa-engine-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/pa-engine-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/pa-engine-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: PA Engine API
            description: Allow clients to fetch Analytics through APIs.
            contact:
              name: FactSet Research Systems
              url: https://developer.factset.com/contact
              email: api@factset.com
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
            version: 3.14.1
          servers:
            - url: https://api.factset.com
          paths:
            /analytics/lookups/v3/accounts/{path}:
              get:
                tags:
                  - Accounts
                summary: Get accounts and sub-directories in a directory
                description: >-
                  This endpoint looks up all ACCT and ACTM files and
                  sub-directories in a given directory.
                operationId: getAccounts
                parameters:
                  - name: path
                    in: path
                    description: The directory to get the accounts and sub-directories in
                    required: true
                    schema:
                      type: string
                      description: The directory to get the accounts and sub-directories in
                      example: 'Client:'
                responses:
                  '200':
                    description: >-
                      Expected response, returns a list of accounts and
                      directories
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/AccountDirectoriesRoot'
                  '400':
                    description: Invalid query parameter or value provided
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Path not found
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header.  Header needs to be set to
                      application/json
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in some time
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/columns:
              get:
                tags:
                  - Columns
                summary: Get PA columns
                description: >-
                  This endpoint lists all the PA columns that can be applied to
                  a calculation.
                operationId: getPAColumns
                parameters:
                  - name: name
                    in: query
                    description: Column name
                    schema:
                      type: string
                      description: Column name
                      default: ''
                      example: Security Name
                  - name: category
                    in: query
                    description: Column category
                    schema:
                      type: string
                      description: Column category
                      default: ''
                  - name: directory
                    in: query
                    description: The directory to get the columns in
                    schema:
                      type: string
                      description: The directory to get the columns in
                      default: ''
                      example: Client
                responses:
                  '200':
                    description: Expected response, returns a list of PA columns
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Age:
                        description: >-
                          Standard HTTP header. Header will specify the age of
                          columns list cached response.
                        schema:
                          type: integer
                          description: >-
                            Standard HTTP header. Header will specify the age of
                            columns list cached response.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ColumnSummaryRoot'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/columns/{id}:
              get:
                tags:
                  - Columns
                summary: Get PA column settings
                description: This endpoint returns the default settings of a PA column.
                operationId: getPAColumnById
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a column
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a column
                      example: >-
                        2DBD317E3C235BC96E2FF8CA36CE036AF2F7F55525479B524AE78FD7D6BBC4A7
                responses:
                  '200':
                    description: Expected response, returns settings of a PA column.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Age:
                        description: >-
                          Standard HTTP header. Header will specify the age of
                          columns list cached response.
                        schema:
                          type: integer
                          description: >-
                            Standard HTTP header. Header will specify the age of
                            columns list cached response.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ColumnRoot'
                  '400':
                    description: Invalid column Id.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Column not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/columnstatistics:
              get:
                tags:
                  - ColumnStatistics
                summary: Get PA column statistics
                description: >-
                  This endpoint lists all the column statistics that can be
                  applied to a PA column.
                operationId: getPAColumnStatistics
                responses:
                  '200':
                    description: Expected response, returns a list of PA column statistics
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ColumnStatisticRoot'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/components:
              get:
                tags:
                  - Components
                summary: Get PA components
                description: >-
                  This endpoint returns the list of PA components in a given PA
                  document.
                operationId: getPAComponents
                parameters:
                  - name: document
                    in: query
                    description: Document Name
                    required: true
                    schema:
                      type: string
                      description: Document Name
                      example: PA3_DOCUMENTS:DEFAULT
                responses:
                  '200':
                    description: Expected response, returns a list of PA components.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ComponentSummaryRoot'
                  '400':
                    description: >-
                      Invalid query parameter provided or Invalid PA document
                      name.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Document not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/components/{id}:
              get:
                tags:
                  - Components
                summary: Get PA component by id
                description: This endpoint returns the default settings of a PA component.
                operationId: getPAComponentById
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a PA component
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a PA component
                      example: >-
                        801B800245E468A52AEBEC4BE31CFF5AF82F371DAEF5F158AC2E98C2FA324B46
                responses:
                  '200':
                    description: >-
                      Expected response, returns the default settings of a PA
                      component.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/PAComponentRoot'
                  '400':
                    description: Invalid PA component id.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Component not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/lookups/v3/currencies:
              get:
                tags:
                  - Currencies
                summary: Get currencies
                description: >-
                  This endpoint lists all the currencies that can be applied to
                  any calculation.
                operationId: getCurrencies
                responses:
                  '200':
                    description: Expected response, returns a list of currencies.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CurrencyRoot'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/dates:
              get:
                tags:
                  - Dates
                summary: Convert PA dates to absolute format
                description: >-
                  This endpoint converts the given start and end dates in
                  FactSet date format to yyyymmdd format for a PA calculation.
                  For more information on FactSet date format, please refer to
                  the PA Engine API documentation under the 'API Documentation'
                  section in the developer portal.
                operationId: convertPADatesToAbsoluteFormat
                parameters:
                  - name: startdate
                    in: query
                    description: Start Date
                    schema:
                      type: string
                      description: Start Date
                      example: '-3AY'
                  - name: enddate
                    in: query
                    description: End Date
                    required: true
                    schema:
                      type: string
                      description: End Date
                      example: '-1AY'
                  - name: componentid
                    in: query
                    description: Component Id
                    required: true
                    schema:
                      type: string
                      description: Component Id
                      example: >-
                        801B800245E468A52AEBEC4BE31CFF5AF82F371DAEF5F158AC2E98C2FA324B46
                  - name: account
                    in: query
                    description: Account ( Account Name ending with .ACCT or .ACTM )
                    required: true
                    schema:
                      type: string
                      description: Account ( Account Name ending with .ACCT or .ACTM )
                      example: Client:/Folder1/Folder2/AccountName.ACCT
                responses:
                  '200':
                    description: >-
                      Expected response, returns the converted dates in yyyymmdd
                      format.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/DateParametersSummaryRoot'
                  '400':
                    description: Invalid query parameter or value is provided.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Document or account not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/documents/{path}:
              get:
                tags:
                  - Documents
                summary: Get PA3 documents and sub-directories in a directory
                description: >-
                  This endpoint looks up all PA3 documents and sub-directories
                  in a given directory.
                operationId: getPA3Documents
                parameters:
                  - name: path
                    in: path
                    description: The directory to get the documents and sub-directories in
                    required: true
                    schema:
                      type: string
                      description: >-
                        The directory to get the documents and sub-directories
                        in
                      example: 'Client:'
                responses:
                  '200':
                    description: >-
                      Expected response, returns a list of PA3 documents and
                      directories
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/DocumentDirectoriesRoot'
                  '400':
                    description: Invalid query parameter or value provided
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Path not found
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header.  Header needs to be set to
                      application/json
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in some time
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/frequencies:
              get:
                tags:
                  - Frequencies
                summary: Get PA frequencies
                description: >-
                  This endpoint lists all the frequencies that can be applied to
                  a PA calculation.
                operationId: getPAFrequencies
                responses:
                  '200':
                    description: Expected response, returns a list of PA frequencies.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/FrequencyRoot'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/groups:
              get:
                tags:
                  - Groups
                summary: Get PA groups
                description: >-
                  This endpoint lists all the PA groups that can be applied to a
                  PA calculation.
                operationId: getPAGroups
                responses:
                  '200':
                    description: Expected response, returns a list of PA groups
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Age:
                        description: >-
                          Standard HTTP header. Header will specify the age of
                          groupings list cached response.
                        schema:
                          type: integer
                          description: >-
                            Standard HTTP header. Header will specify the age of
                            groupings list cached response.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/GroupRoot'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/grouping-frequencies:
              get:
                tags:
                  - Groups
                summary: Get PA grouping frequencies
                description: >-
                  This endpoint lists all the PA grouping frequencies that can
                  be applied to a PA calculation.
                operationId: getPAGroupingFrequencies
                responses:
                  '200':
                    description: >-
                      Expected response, returns a list of PA grouping
                      frequencies
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/FrequencyRoot'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/linked-templates:
              post:
                tags:
                  - LinkedPATemplates
                summary: Create a linked PA template
                description: "This endpoint creates a template from an **existing portfolio analysis tile**, allowing the user to replicate and fetch reports settings.\r\n\r\nRemarks:\r\n\r\n*   Mandatory fields are required to be passed in POST requests and Optional fields are not necessary. \r\n    If no mandatory fields are passed, then we can use the template as a component and skip the component creation.\r\n    \r\n*   Mandatory, optional and locked fields can be  \"accounts\", \"benchmarks\", \"groups\", \"columns\", \"datasources\", \"dates\", \"currencyisocode\" and \"componentdetail\".\r\n\r\n*   We cannot override the Locked fields when creating the Component.\r\n\r\n*   Mandatory and locked strings are mutually exclusive.\r\n\r\n*   Multi-horizon frequencies are not supported through this endpoint."
                operationId: createLinkedPATemplates
                requestBody:
                  description: Request Parameters
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/LinkedPATemplateParametersRoot'
                      example:
                        data:
                          directory: Personal:LinkedPATemplates/
                          parentComponentId: >-
                            801B800245E468A52AEBEC4BE31CFF5AF82F371DAEF5F158AC2E98C2FA324B46
                          description: >-
                            This is a linked PA template that only returns
                            security level data
                          content:
                            mandatory:
                              - accounts
                              - benchmarks
                            optional:
                              - groups
                              - columns
                            locked:
                              - componentdetail
                  required: true
                responses:
                  '201':
                    description: >-
                      Expected response, created a template linked to a PA3
                      tile.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/LinkedPATemplatePostSummaryRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Component not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - LinkedPATemplates
                summary: Get linked PA templates
                description: >-
                  This endpoint returns the list of linked PA templates in given
                  path.
                operationId: getLinkedPATemplates
                parameters:
                  - name: directory
                    in: query
                    description: Get linked PA templates in path.
                    schema:
                      type: string
                      description: Get linked PA templates in path.
                      example: Personal:LinkedPATemplates/
                  - name: documentDirectory
                    in: query
                    description: Get linked PA templates for documents in document path
                    schema:
                      type: string
                      description: Get linked PA templates for documents in document path
                  - name: documentName
                    in: query
                    description: Get linked PA templates for documents by document name
                    schema:
                      type: string
                      description: Get linked PA templates for documents by document name
                responses:
                  '200':
                    description: >-
                      Expected response, returns a list of templates linked to
                      PA3 tile.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/LinkedPATemplateSummaryRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Document not found
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/linked-templates/{id}:
              put:
                tags:
                  - LinkedPATemplates
                summary: Update a linked PA template
                description: "This endpoint allows the user to change the request body and description from an existing template.\r\n\r\nRemarks:\r\n\r\n*   Mandatory fields are required to be passed in POST requests and Optional fields are not necessary. \r\n    If no mandatory fields are passed, then we can use the template as a component and skip the component creation.\r\n    \r\n*   Mandatory, optional and locked fields can be  \"accounts\", \"benchmarks\", \"groups\", \"columns\", \"datasources\", \"dates\", \"currencyisocode\" and \"componentdetail\".\r\n\r\n*   We cannot override the Locked fields when creating the Component.\r\n\r\n*   Mandatory and locked strings are mutually exclusive.\r\n\r\n*   Multi-horizon frequencies are not supported through this endpoint."
                operationId: updateLinkedPATemplates
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a linked PA template
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a linked PA template
                      example: '01234567890123456789012345678901'
                requestBody:
                  description: Request Parameters
                  content:
                    application/json:
                      schema:
                        $ref: >-
                          #/components/schemas/LinkedPATemplateUpdateParametersRoot
                      example:
                        data:
                          parentComponentId: >-
                            801B800245E468A52AEBEC4BE31CFF5AF82F371DAEF5F158AC2E98C2FA324B46
                          description: >-
                            This is a linked PA template that only returns
                            security level data
                          content:
                            mandatory:
                              - accounts
                              - benchmarks
                            optional:
                              - groups
                              - columns
                            locked:
                              - componentdetail
                  required: true
                responses:
                  '200':
                    description: >-
                      Expected response, updated a template linked to a PA3
                      tile.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/LinkedPATemplatePostSummaryRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template or component not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              delete:
                tags:
                  - LinkedPATemplates
                summary: Delete a linked PA template.
                description: This endpoint deletes an existing linked PA template.
                operationId: deleteLinkedPATemplates
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a linked PA template
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a linked PA template
                      example: '01234567890123456789012345678901'
                responses:
                  '204':
                    description: >-
                      Expected response, deleted the linked PA template
                      successfully.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - LinkedPATemplates
                summary: Get linked PA template by id
                description: This endpoint fetches the linked PA template settings.
                operationId: getLinkedPATemplatesById
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a linked PA template
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a linked PA template
                      example: '01234567890123456789012345678901'
                responses:
                  '200':
                    description: Expected response, linked PA template details.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/LinkedPATemplateRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/calculations:
              post:
                tags:
                  - PACalculations
                summary: Create and Run PA calculation
                description: "This endpoint runs the PA calculation specified in the POST body parameters.\r\nIt can take one or more calculation units as input.\r\n\r\nRemarks:\r\n\r\n*\tAny settings in POST body will act as a one-time override over the settings saved in the PA template.\r\n\r\n*   Account identifiers must have .ACCT or .ACTM extension or BENCH: prefix. Holdings mode can be optionally set for every account. \r\n    Possible values for holdings mode are B&H (Buy and Hold), TBR (Transaction based returns), OMS (Order Management System), \r\n    VLT (Vaulted returns) or EXT (External Returns Data). Default holdings mode value is B&H. \r\n\r\n*   If we are overriding the grouping with a frequency, we will be overriding the grouping saved to the original component and also overriding \r\n    the default frequency of the Beginning of Period to whatever we pass in the request body.\r\n    \r\n*   If we are overriding gouping frequency without overriding the group id it will not be applied to the default groupings saved to the original component.\r\n\r\n*   Componentdetail supports securities, groups, groupsall, and totals levels of granularity. However, if no value is passed, the default value is 'securities'.\r\n    Additionally, while 'groupsall' returns all the group levels in the PA component,\r\n    setting componentdetail to 'groups' only returns the expanded or collapsed group levels within the PA component."
                operationId: postAndCalculate
                parameters:
                  - name: X-FactSet-Api-Long-Running-Deadline
                    in: header
                    description: >-
                      Long running deadline in seconds when only one unit is
                      passed in the POST body.
                    schema:
                      type: integer
                  - name: Cache-Control
                    in: header
                    description: Standard HTTP header.  Accepts max-stale.
                    schema:
                      type: string
                requestBody:
                  description: Calculation Parameters
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/PACalculationParametersRoot'
                      example:
                        data:
                          '1':
                            componentid: >-
                              801B800245E468A52AEBEC4BE31CFF5AF82F371DAEF5F158AC2E98C2FA324B46
                            accounts:
                              - id: BENCH:DJII
                                holdingsmode: B&H
                            benchmarks:
                              - id: BENCH:SP50
                                holdingsmode: B&H
                            dates:
                              startdate: '20210101'
                              enddate: '20210331'
                              frequency: Monthly
                            currencyisocode: USD
                          '2':
                            componentid: >-
                              67077F67610EC30675E240A614661176C792A8997C78C9B9D64F738C01F18893
                            accounts:
                              - id: BENCH:SP100EQ
                                holdingsmode: B&H
                            benchmarks:
                              - id: BENCH:SP50
                                holdingsmode: B&H
                            dates:
                              frequency: Single
                              enddate: '0'
                            currencyisocode: USD
                        meta:
                          stachContentorganization: SimplifiedRow
                          format: JsonStach
                responses:
                  '200':
                    description: >-
                      Expected response, if the calculation has one unit and is
                      completed with an error.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                  '201':
                    description: >-
                      Expected response if the calculation has one unit and is
                      completed in a short span, returns JSON in the format
                      specified in the Calculation parameters.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ObjectRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ObjectRoot'
                  '202':
                    description: >-
                      Expected response, contains the poll URL in the Location
                      header.
                    headers:
                      Location:
                        description: URL to poll for the resulting calculation
                        schema:
                          type: string
                          description: URL to poll for the resulting calculation
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                  '400':
                    description: Invalid calculation parameters.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: One or more calculation settings were unavailable.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '415':
                    description: >-
                      Missing/Invalid Content-Type header. Header needs to be
                      set to application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Cancel older requests using Cancel
                      Calculation endpoint or wait for older requests to
                      finish/expire.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - PACalculations
                summary: Get all calculations
                description: This endpoints returns all calculation requests.
                operationId: getAllCalculations
                parameters:
                  - name: pageNumber
                    in: query
                    schema:
                      type: integer
                      format: int32
                      default: 1
                responses:
                  '200':
                    description: List of calculation requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationsSummaryRoot'
                  '400':
                    description: Invalid page number.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: No calculation found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/calculations/{id}:
              put:
                tags:
                  - PACalculations
                summary: Create or Update PA calculation and run it.
                description: "This endpoint updates and run the PA calculation specified in the PUT body parameters. This also allows creating new PA calculations with custom ids.\r\nIt can take one or more calculation units as input.\r\n\r\nRemarks:\r\n\r\n*\tAny settings in PUT body will act as a one-time override over the settings saved in the PA template.\r\n\r\n*   Account identifiers must have .ACCT or .ACTM extension or BENCH: prefix. Holdings mode can be optionally set for every account. \r\n    Possible values for holdings mode are B&H (Buy and Hold), TBR (Transaction based returns), OMS (Order Management System), \r\n    VLT (Vaulted returns) or EXT (External Returns Data). Default holdings mode value is B&H.\r\n\r\n*   If we are overriding the grouping with a frequency, we will be overriding the grouping saved to the original component and also overriding \r\n    the default frequency of the Beginning of Period to whatever we pass in the request body.\r\n    \r\n*   If we are overriding gouping frequency without overriding the group id it will not be applied to the default groupings saved to the original component.\r\n\r\n*   Componentdetail supports securities, groups, groupsall, and totals levels of granularity. However, if no value is passed, the default value is 'securities'.\r\n    Additionally, while 'groupsall' returns all the group levels in the PA component,\r\n    setting componentdetail to 'groups' only returns the expanded or collapsed group levels within the PA component."
                operationId: putAndCalculate
                parameters:
                  - name: id
                    in: path
                    description: >-
                      from url, provided from the location header in the Create
                      and Run PA calculation endpoint
                    required: true
                    schema:
                      type: string
                      description: >-
                        from url, provided from the location header in the
                        Create and Run PA calculation endpoint
                  - name: X-FactSet-Api-Long-Running-Deadline
                    in: header
                    description: >-
                      Long running deadline in seconds when only one unit is
                      passed in the PUT body.
                    schema:
                      type: integer
                  - name: Cache-Control
                    in: header
                    description: Standard HTTP header.  Accepts max-stale.
                    schema:
                      type: string
                requestBody:
                  description: Calculation Parameters
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/PACalculationParametersRoot'
                      example:
                        data:
                          '1':
                            componentid: >-
                              801B800245E468A52AEBEC4BE31CFF5AF82F371DAEF5F158AC2E98C2FA324B46
                            accounts:
                              - id: BENCH:DJII
                                holdingsmode: B&H
                            benchmarks:
                              - id: BENCH:SP50
                                holdingsmode: B&H
                            dates:
                              startdate: '20210101'
                              enddate: '20210231'
                              frequency: Monthly
                            currencyisocode: USD
                          '2':
                            componentid: >-
                              67077F67610EC30675E240A614661176C792A8997C78C9B9D64F738C01F18893
                            accounts:
                              - id: BENCH:SP100EQ
                                holdingsmode: B&H
                            benchmarks:
                              - id: BENCH:SP50
                                holdingsmode: B&H
                            dates:
                              frequency: Single
                              enddate: '0'
                            currencyisocode: USD
                        meta:
                          stachContentorganization: SimplifiedRow
                          format: JsonStach
                responses:
                  '200':
                    description: >-
                      Expected response, if the calculation has one unit and is
                      completed with an error.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                  '201':
                    description: >-
                      Expected response if the calculation has one unit and is
                      completed in a short span, returns JSON in the format
                      specified in the Calculation parameters.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ObjectRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ObjectRoot'
                  '202':
                    description: >-
                      Expected response, contains the poll URL in the Location
                      header.
                    headers:
                      Location:
                        description: URL to poll for the resulting calculation
                        schema:
                          type: string
                          description: URL to poll for the resulting calculation
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                  '400':
                    description: Invalid Calculation Parameters.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: One or more calculation settings were unavailable.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '409':
                    description: Duplicate calculation exists with same parameters.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '415':
                    description: >-
                      Missing/Invalid Content-Type header. Header needs to be
                      set to application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Cancel older requests using Cancel
                      Calculation endpoint or wait for older requests to
                      finish/expire.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - PACalculations
                summary: Get PA calculation parameters by id
                description: >-
                  This is the endpoint that returns the calculation parameters
                  passed for a calculation.
                operationId: getCalculationParameters
                parameters:
                  - name: id
                    in: path
                    description: >-
                      from url, provided from the location header in the Create
                      and Run PA calculation endpoint
                    required: true
                    schema:
                      type: string
                      description: >-
                        from url, provided from the location header in the
                        Create and Run PA calculation endpoint
                responses:
                  '200':
                    description: Expected response, returns the PA calculation parameters.
                    headers:
                      Content-Encoding:
                        description: >-
                          Standard HTTP header. Header value based on
                          Accept-Encoding Request header.
                        schema:
                          type: string
                          description: >-
                            Standard HTTP header. Header value based on
                            Accept-Encoding Request header.
                      Content-Type:
                        description: Standard HTTP header.
                        schema:
                          type: string
                          description: Standard HTTP header.
                      Transfer-Encoding:
                        description: >-
                          Standard HTTP header. Header value will be set to
                          Chunked if Accept-Encoding header is specified.
                        schema:
                          type: string
                          description: >-
                            Standard HTTP header. Header value will be set to
                            Chunked if Accept-Encoding header is specified.
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/PACalculationParametersRoot'
                  '400':
                    description: Invalid identifier provided.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Calculation id not found
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              delete:
                tags:
                  - PACalculations
                summary: Cancel PA calculation by id
                description: >-
                  This is the endpoint to cancel a previously submitted
                  calculation.
                operationId: cancelCalculationById
                parameters:
                  - name: id
                    in: path
                    description: >-
                      from url, provided from the location header in the Create
                      and Run PA calculation endpoint
                    required: true
                    schema:
                      type: string
                      description: >-
                        from url, provided from the location header in the
                        Create and Run PA calculation endpoint
                responses:
                  '204':
                    description: Expected response, calculation was canceled successfully.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '400':
                    description: Invalid identifier provided.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: >-
                      There was no request for the calculation identifier
                      provided, or the request was already canceled for the
                      provided identifier.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/calculations/{id}/status:
              get:
                tags:
                  - PACalculations
                summary: Get PA calculation status by id
                description: "This is the endpoint to check on the progress of a previously requested calculation.\r\nIf the calculation has finished computing, the location header will point to the result url.\r\nOtherwise, the calculation is still running and the X-FactSet-Api-PickUp-Progress header will contain a progress percentage."
                operationId: getCalculationStatusById
                parameters:
                  - name: id
                    in: path
                    description: >-
                      from url, provided from the location header in the Create
                      and Run PA calculation endpoint
                    required: true
                    schema:
                      type: string
                      description: >-
                        from url, provided from the location header in the
                        Create and Run PA calculation endpoint
                responses:
                  '200':
                    description: Expected response once calculation is completed.
                    headers:
                      Content-Encoding:
                        description: >-
                          Standard HTTP header. Header value based on
                          Accept-Encoding Request header.
                        schema:
                          type: string
                          description: >-
                            Standard HTTP header. Header value based on
                            Accept-Encoding Request header.
                      Content-Type:
                        description: Standard HTTP header.
                        schema:
                          type: string
                          description: Standard HTTP header.
                      Transfer-Encoding:
                        description: >-
                          Standard HTTP header. Header value will be set to
                          Chunked if Accept-Encoding header is specified.
                        schema:
                          type: string
                          description: >-
                            Standard HTTP header. Header value will be set to
                            Chunked if Accept-Encoding header is specified.
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                  '202':
                    description: >-
                      Expected response returned if the calculation is not yet
                      completed, should contain X-FactSet-Api-PickUp-Progress
                      header.
                    headers:
                      X-FactSet-Api-PickUp-Progress:
                        description: FactSet's progress header.
                        schema:
                          type: string
                          description: FactSet's progress header.
                      Cache-Control:
                        description: >-
                          Standard HTTP header. Header will specify max-age in
                          seconds. Polling can be adjusted based on the max-age
                          value.
                        schema:
                          type: integer
                          description: >-
                            Standard HTTP header. Header will specify max-age in
                            seconds. Polling can be adjusted based on the
                            max-age value.
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/CalculationStatusRoot'
                  '400':
                    description: Invalid identifier provided.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: >-
                      Calculation was already returned, provided id was not a
                      requested calculation, or the calculation was cancelled
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/calculations/{id}/units/{unitId}/result:
              get:
                tags:
                  - PACalculations
                summary: Get PA calculation result by id
                description: "This is the endpoint to get the result of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON."
                operationId: getCalculationUnitResultById
                parameters:
                  - name: id
                    in: path
                    description: >-
                      from url, provided from the location header in the Get PA
                      calculation status by id endpoint
                    required: true
                    schema:
                      type: string
                      description: >-
                        from url, provided from the location header in the Get
                        PA calculation status by id endpoint
                  - name: unitId
                    in: path
                    description: >-
                      from url, provided from the location header in the Get PA
                      calculation status by id endpoint
                    required: true
                    schema:
                      type: string
                      description: >-
                        from url, provided from the location header in the Get
                        PA calculation status by id endpoint
                responses:
                  '200':
                    description: >-
                      Expected response once calculation is completed, returns
                      JSON in the format specified in the Calculation
                      parameters.
                    headers:
                      Content-Encoding:
                        description: >-
                          Standard HTTP header. Header value based on
                          Accept-Encoding Request header.
                        schema:
                          type: string
                          description: >-
                            Standard HTTP header. Header value based on
                            Accept-Encoding Request header.
                      Content-Type:
                        description: Standard HTTP header.
                        schema:
                          type: string
                          description: Standard HTTP header.
                      Transfer-Encoding:
                        description: >-
                          Standard HTTP header. Header value will be set to
                          Chunked if Accept-Encoding header is specified.
                        schema:
                          type: string
                          description: >-
                            Standard HTTP header. Header value will be set to
                            Chunked if Accept-Encoding header is specified.
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ObjectRoot'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ObjectRoot'
                  '400':
                    description: Invalid identifier provided.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: >-
                      Calculation was already returned, provided id was not a
                      requested calculation, or the calculation was cancelled
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                      application/x-protobuf:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/pricing-sources:
              get:
                tags:
                  - PricingSources
                summary: Get PA pricing sources
                description: >-
                  This endpoint lists all the PA pricing sources that can be
                  applied to a PA calculation.
                operationId: getPAPricingSources
                parameters:
                  - name: name
                    in: query
                    description: PA pricing sources name
                    schema:
                      type: string
                      description: PA pricing sources name
                      default: ''
                  - name: category
                    in: query
                    description: PA pricing sources category
                    schema:
                      type: string
                      description: PA pricing sources category
                      default: ''
                  - name: directory
                    in: query
                    description: The directory to get the PA pricing sources in
                    schema:
                      type: string
                      description: The directory to get the PA pricing sources in
                      default: ''
                responses:
                  '200':
                    description: Expected response, returns a list of PA pricing sources
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Age:
                        description: >-
                          Standard HTTP header. Header will specify the age of
                          pricing sources list cached response.
                        schema:
                          type: integer
                          description: >-
                            Standard HTTP header. Header will specify the age of
                            pricing sources list cached response.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/PAPricingSourceRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Pricing sources not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/templated-components:
              post:
                tags:
                  - TemplatedPAComponents
                summary: Create templated PA component
                description: "This endpoint creates new component based off of linked PA template or unlinked PA template.\r\n\r\nRemarks:\r\n\r\n*   Any settings in the POST body will act as a one-time override over the settings saved in the PA template.\r\n\r\n*   Account identifiers must have .ACCT or .ACTM extension or BENCH: prefix. Holdings mode can be optionally set for every account. \r\n    Possible values for holdings mode are B&H (Buy and Hold), TBR (Transaction based returns), OMS (Order Management System), \r\n    VLT (Vaulted returns) or EXT (External Returns Data). Default holdings mode value is B&H.\r\n\r\n*   Multi-horizon frequencies are not supported through this endpoint.\r\n\r\n*   Componentdetail supports securities, groups, groupsall, and totals levels of granularity. However, if no value is passed, the default value is 'securities'.\r\n    Additionally, while 'groupsall' returns all the group levels in the PA component,\r\n    setting componentdetail to 'groups' only returns the expanded or collapsed group levels within the PA component.\r\n\r\n*   If we are overriding the grouping with a frequency, we will be overriding the grouping saved to the original component and also overriding \r\n    the default frequency of the Beginning of Period to whatever we pass in the request body.\r\n    \r\n*   If we are overriding gouping frequency without overriding the group id it will not be applied to the default groupings saved to the original component."
                operationId: createTemplatedPAComponents
                requestBody:
                  description: Request Parameters
                  content:
                    application/json:
                      schema:
                        $ref: >-
                          #/components/schemas/TemplatedPAComponentParametersRoot
                      example:
                        data:
                          directory: Personal:TemplatedPAComponents/
                          parentTemplateId: '01234567890123456789012345678901'
                          description: This is a templated PA component
                          componentData:
                            accounts:
                              - id: SPN:SP50
                                holdingsmode: B&H
                              - id: MSCI_USA:984000
                                holdingsmode: B&H
                            benchmarks:
                              - id: SPN:SP50
                                holdingsmode: B&H
                              - id: DJGX:AMERICAS
                                holdingsmode: B&H
                            groups:
                              - id: >-
                                  5BCFFD17598FAEBD88EB4934EFB5FEF53849867D607ECEF232CD42D3369BBBCA
                                frequency: BeginningOfPeriod
                            columns:
                              - id: >-
                                  BD1720474AB8A80BDD79777F5B9CA594F4151C0554E30F9C916BA73BFAFC1FE0
                                statistics:
                                  - eb9d6d91416e4224bacadc261787e56f
                            datasources:
                              portfoliopricingsources:
                                - id: >-
                                    39A1C0C7BD46731552B29D913804EC5F3ED91E6B991AF298DEC88CCA2A9FC6B3
                              benchmarkpricingsources:
                                - id: >-
                                    9BB2A3142C450AF54A7486C1D37A210A64474B2499A1E4A30E19801B9FC55E8C
                              useportfoliopricingsourcesforbenchmark: false
                            currencyisocode: USD
                            componentdetail: GROUPS
                  required: true
                responses:
                  '201':
                    description: >-
                      Expected response, templated PA component created
                      successfully.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/TemplatedPAComponentPostSummaryRoot
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - TemplatedPAComponents
                summary: Get templated PA components in path
                description: >-
                  This endpoint returns the list of templated PA components in
                  path.
                operationId: getTemplatedPAComponentsInPath
                parameters:
                  - name: directory
                    in: query
                    description: Get templated PA components in path
                    required: true
                    schema:
                      type: string
                      description: Get templated PA components in path
                      example: Personal:TemplatedPAComponents/
                responses:
                  '200':
                    description: Expected response, returns a list templated PA components.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/TemplatedPAComponentSummaryRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/templated-components/{id}:
              put:
                tags:
                  - TemplatedPAComponents
                summary: Update templated PA component
                description: "This endpoint allows the user to change the request body from an existing templated PA component.\r\n\r\nRemarks:\r\n\r\n*   Any settings in the POST body will act as a one-time override over the settings saved in the PA template.\r\n\r\n*   Account identifiers must have .ACCT or .ACTM extension or BENCH: prefix. Holdings mode can be optionally set for every account. \r\n    Possible values for holdings mode are B&H (Buy and Hold), TBR (Transaction based returns), OMS (Order Management System), \r\n    VLT (Vaulted returns) or EXT (External Returns Data). Default holdings mode value is B&H. \r\n\r\n*   Multi-horizon frequencies are not supported through this endpoint.\r\n\r\n*   Componentdetail supports securities, groups, groupsall, and totals levels of granularity. However, if no value is passed, the default value is 'securities'.\r\n    Additionally, while 'groupsall' returns all the group levels in the PA component,\r\n    setting componentdetail to 'groups' only returns the expanded or collapsed group levels within the PA component.\r\n\r\n*   If we are overriding the grouping with a frequency, we will be overriding the grouping saved to the original component and also overriding \r\n    the default frequency of the Beginning of Period to whatever we pass in the request body.\r\n    \r\n*   If we are overriding gouping frequency without overriding the group id it will not be applied to the default groupings saved to the original component."
                operationId: updateTemplatedPAComponents
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a templated PA component
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a templated PA component
                      example: '01234567890123456789012345678901'
                requestBody:
                  description: Request Parameters
                  content:
                    application/json:
                      schema:
                        $ref: >-
                          #/components/schemas/TemplatedPAComponentUpdateParametersRoot
                      example:
                        data:
                          parentTemplateId: '01234567890123456789012345678901'
                          description: This is a templated PA component
                          componentData:
                            accounts:
                              - id: SPN:SP50
                                holdingsmode: B&H
                              - id: MSCI_USA:984000
                                holdingsmode: B&H
                            benchmarks:
                              - id: SPN:SP50
                                holdingsmode: B&H
                              - id: DJGX:AMERICAS
                                holdingsmode: B&H
                            groups:
                              - id: >-
                                  5BCFFD17598FAEBD88EB4934EFB5FEF53849867D607ECEF232CD42D3369BBBCA
                                frequency: BeginningOfPeriod
                            columns:
                              - id: >-
                                  BD1720474AB8A80BDD79777F5B9CA594F4151C0554E30F9C916BA73BFAFC1FE0
                                statistics:
                                  - eb9d6d91416e4224bacadc261787e56f
                            datasources:
                              portfoliopricingsources:
                                - id: >-
                                    39A1C0C7BD46731552B29D913804EC5F3ED91E6B991AF298DEC88CCA2A9FC6B3
                              benchmarkpricingsources:
                                - id: >-
                                    9BB2A3142C450AF54A7486C1D37A210A64474B2499A1E4A30E19801B9FC55E8C
                              useportfoliopricingsourcesforbenchmark: false
                            currencyisocode: USD
                            componentdetail: GROUPS
                  required: true
                responses:
                  '200':
                    description: Expected response, updated successfully.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/TemplatedPAComponentPostSummaryRoot
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Component or template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - TemplatedPAComponents
                summary: Get templated PA component by id
                description: This endpoint fetches the templated PA component settings.
                operationId: getTemplatedPAComponentById
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a templated PA component
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a templated PA component
                      example: '01234567890123456789012345678901'
                responses:
                  '200':
                    description: Expected response, templated PA component details.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/TemplatedPAComponentRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Templated PA component not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              delete:
                tags:
                  - TemplatedPAComponents
                summary: Delete templated PA component
                description: This endpoint deletes an existing templated PA component
                operationId: deleteTemplatedPAComponents
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for a templated PA component
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for a templated PA component
                      example: '01234567890123456789012345678901'
                responses:
                  '204':
                    description: >-
                      Expected response, deleted the templated PA component
                      successfully.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Component not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/unlinked-templates:
              post:
                tags:
                  - UnlinkedPATemplates
                summary: Create unlinked PA template
                description: "This endpoint creates a template which is not linked to any specific PA3 tile. \r\n\r\nRemarks:\r\n\r\n*   Mandatory fields are required to be passed in POST requests and Optional fields are not necessary. \r\n    If no mandatory fields are passed, then we can use the template as a component and skip the component creation.\r\n    \r\n*   Mandatory, optional and locked fields can be  \"accounts\", \"benchmarks\", \"groups\", \"columns\", \"datasources\", \"dates\", \"currencyisocode\" and \"componentdetail\".\r\n\r\n*   We cannot override the Locked fields when creating the Component.\r\n\r\n*   Mandatory and locked strings are mutually exclusive.\r\n\r\n*   Any settings in the POST body will act as a one-time override over the settings saved in the PA template.\r\n\r\n*   Account identifiers must have .ACCT or .ACTM extension or BENCH: prefix. Holdings mode can be optionally set for every account. \r\n    Possible values for holdings mode are B&H (Buy and Hold), TBR (Transaction based returns), OMS (Order Management System), \r\n    VLT (Vaulted returns) or EXT (External Returns Data). Default holdings mode value is B&H.\r\n\r\n*   Multi-horizon frequencies are not supported through this endpoint.\r\n\r\n*   Componentdetail supports securities, groups, groupsall, and totals levels of granularity. However, if no value is passed, the default value is 'securities'.\r\n    Additionally, while 'groupsall' returns all the group levels in the PA component,\r\n    setting componentdetail to 'groups' only returns the expanded or collapsed group levels within the PA component.\r\n\r\n*   If we are overriding the grouping with a frequency, we will be overriding the grouping saved to the original component and also \r\n    overriding the default frequency of the Beginning of Period to whatever we pass in the request body.\r\n    \r\n*   If we are overriding gouping frequency without overriding the group id it will not be applied to the default groupings saved to the original component."
                operationId: createUnlinkedPATemplates
                requestBody:
                  description: Request Parameters
                  content:
                    application/json:
                      schema:
                        $ref: '#/components/schemas/UnlinkedPATemplateParametersRoot'
                      example:
                        data:
                          directory: Personal:UnlinkedPATemplates/
                          templateTypeId: >-
                            996E90B981AEE83F14029ED3D309FB3F03EC6E2ACC7FD42C22CBD5D279502CFD
                          description: >-
                            This is an unlinked PA template that only returns
                            security level data
                          accounts:
                            - id: SPN:SP50
                              holdingsmode: B&H
                            - id: MSCI_USA:984000
                              holdingsmode: B&H
                          benchmarks:
                            - id: SPN:SP50
                              holdingsmode: B&H
                            - id: DJGX:AMERICAS
                              holdingsmode: B&H
                          columns:
                            - id: >-
                                BD1720474AB8A80BDD79777F5B9CA594F4151C0554E30F9C916BA73BFAFC1FE0
                              statistics:
                                - eb9d6d91416e4224bacadc261787e56f
                          dates:
                            startdate: '20200101'
                            enddate: '20201215'
                            frequency: Monthly
                          groups:
                            - id: >-
                                5BCFFD17598FAEBD88EB4934EFB5FEF53849867D607ECEF232CD42D3369BBBCA
                              frequency: BeginningOfPeriod
                          datasources:
                            portfoliopricingsources:
                              - id: >-
                                  39A1C0C7BD46731552B29D913804EC5F3ED91E6B991AF298DEC88CCA2A9FC6B3
                            benchmarkpricingsources:
                              - id: >-
                                  9BB2A3142C450AF54A7486C1D37A210A64474B2499A1E4A30E19801B9FC55E8C
                            useportfoliopricingsourcesforbenchmark: false
                          currencyisocode: USD
                          componentdetail: GROUPS
                          content:
                            mandatory:
                              - accounts
                              - benchmarks
                            optional:
                              - groups
                              - columns
                            locked:
                              - dates
                  required: true
                responses:
                  '201':
                    description: Expected response, created a unlinked PA template.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/UnlinkedPATemplatePostSummaryRoot
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - UnlinkedPATemplates
                summary: Get unlinked PA templates
                description: This endpoint returns the list of unlinked PA templates.
                operationId: getUnlinkedPATemplates
                parameters:
                  - name: directory
                    in: query
                    description: Get unlinked PA templates in path.
                    schema:
                      type: string
                      description: Get unlinked PA templates in path.
                      example: Personal:UninkedPATemplates/
                  - name: category
                    in: query
                    description: Get unlinked PA templates by category.
                    schema:
                      type: string
                      description: Get unlinked PA templates by category.
                      example: Weights
                responses:
                  '200':
                    description: >-
                      Expected response, returns a list of unlinked PA
                      templates.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/UnlinkedPATemplateSummaryRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/unlinked-templates/{id}:
              put:
                tags:
                  - UnlinkedPATemplates
                summary: Update unlinked PA template
                description: "This endpoint updates an existing unlinked PA template.\r\n\r\nRemarks:\r\n            \r\n*   Mandatory fields are required to be passed in POST requests and Optional fields are not necessary. \r\n    If no mandatory fields are passed, then we can use the template as a component and skip the component creation.\r\n    \r\n*   Mandatory, optional and locked fields can be  \"accounts\", \"benchmarks\", \"groups\", \"columns\", \"datasources\", \"dates\", \"currencyisocode\" and \"componentdetail\".\r\n\r\n*   We cannot override the Locked fields when creating the Component.\r\n\r\n*   Mandatory and locked strings are mutually exclusive.\r\n\r\n*   Any settings in the POST body will act as a one-time override over the settings saved in the PA template.\r\n\r\n*   Account identifiers must have .ACCT or .ACTM extension or BENCH: prefix. Holdings mode can be optionally set for every account. \r\n    Possible values for holdings mode are B&H (Buy and Hold), TBR (Transaction based returns), OMS (Order Management System), \r\n    VLT (Vaulted returns) or EXT (External Returns Data). Default holdings mode value is B&H.\r\n\r\n*   Multi-horizon frequencies are not supported through this endpoint.\r\n\r\n*   Componentdetail supports securities, groups, groupsall, and totals levels of granularity. However, if no value is passed, the default value is 'securities'.\r\n    Additionally, while 'groupsall' returns all the group levels in the PA component,\r\n    setting componentdetail to 'groups' only returns the expanded or collapsed group levels within the PA component.\r\n\r\n*   If we are overriding the grouping with a frequency, we will be overriding the grouping saved to the original component and also overriding \r\n    the default frequency of the Beginning of Period to whatever we pass in the request body.\r\n    \r\n*   If we are overriding gouping frequency without overriding the group id it will not be applied to the default groupings saved to the original component."
                operationId: updateUnlinkedPATemplates
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for an unlinked PA template
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for an unlinked PA template
                      example: '01234567890123456789012345678901'
                requestBody:
                  description: Request Parameters
                  content:
                    application/json:
                      schema:
                        $ref: >-
                          #/components/schemas/UnlinkedPATemplateUpdateParametersRoot
                      example:
                        data:
                          description: >-
                            This is an unlinked PA template that only returns
                            security level data
                          accounts:
                            - id: SPN:SP50
                              holdingsmode: B&H
                            - id: MSCI_USA:984000
                              holdingsmode: B&H
                          benchmarks:
                            - id: SPN:SP50
                              holdingsmode: B&H
                            - id: DJGX:AMERICAS
                              holdingsmode: B&H
                          columns:
                            - id: >-
                                BD1720474AB8A80BDD79777F5B9CA594F4151C0554E30F9C916BA73BFAFC1FE0
                              statistics:
                                - eb9d6d91416e4224bacadc261787e56f
                          dates:
                            startdate: '20200101'
                            enddate: '20201215'
                            frequency: Monthly
                          groups:
                            - id: >-
                                5BCFFD17598FAEBD88EB4934EFB5FEF53849867D607ECEF232CD42D3369BBBCA
                              frequency: BeginningOfPeriod
                          datasources:
                            portfoliopricingsources:
                              - id: >-
                                  39A1C0C7BD46731552B29D913804EC5F3ED91E6B991AF298DEC88CCA2A9FC6B3
                            benchmarkpricingsources:
                              - id: >-
                                  9BB2A3142C450AF54A7486C1D37A210A64474B2499A1E4A30E19801B9FC55E8C
                            useportfoliopricingsourcesforbenchmark: false
                          currencyisocode: USD
                          componentdetail: GROUPS
                          content:
                            mandatory:
                              - accounts
                              - benchmarks
                            optional:
                              - columns
                            locked:
                              - groups
                  required: true
                responses:
                  '200':
                    description: Expected response, updated the unlinked PA template.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/UnlinkedPATemplatePostSummaryRoot
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              delete:
                tags:
                  - UnlinkedPATemplates
                summary: Delete unlinked PA template
                description: This endpoint deletes an existing unliked PA template.
                operationId: deleteUnlinkedPATemplates
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for an unlinked PA template
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for an unlinked PA template
                      example: '01234567890123456789012345678901'
                responses:
                  '204':
                    description: >-
                      Expected response, deleted the unlinked PA template
                      successfully.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
              get:
                tags:
                  - UnlinkedPATemplates
                summary: Get unlinked PA template details by id
                description: This endpoint fetches the template settings.
                operationId: getUnlinkedPATemplatesById
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for an unlinked PA template
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for an unlinked PA template
                      example: '01234567890123456789012345678901'
                responses:
                  '200':
                    description: >-
                      Expected response, get details of the unlinked PA
                      template.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/UnlinkedPATemplateRoot'
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Template not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/unlinked-templates/template-types:
              get:
                tags:
                  - UnlinkedPATemplates
                summary: Get default unlinked PA template types.
                description: This endpoint fetches default unlinked PA template types.
                operationId: getDefaultUnlinkedPATemplateTypes
                responses:
                  '200':
                    description: Expected response, default unlinked PA template types
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/UnlinkedPATemplateCategoryAndTypeRoot
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
            /analytics/engines/pa/v3/unlinked-templates/template-types/{id}:
              get:
                tags:
                  - UnlinkedPATemplates
                summary: Get unlinked PA template type details by id.
                description: This endpoint fetches the unlinked PA template type details.
                operationId: getDetailsType
                parameters:
                  - name: id
                    in: path
                    description: Unique identifier for an unlinked PA template type
                    required: true
                    schema:
                      type: string
                      description: Unique identifier for an unlinked PA template type
                responses:
                  '200':
                    description: >-
                      Expected response, details of the unlinked PA template
                      type
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: >-
                            #/components/schemas/UnlinkedPATemplateCategoryAndTypeDetailsRoot
                  '400':
                    description: >-
                      Invalid data provided. Please check the request parameters
                      before attempting again.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '401':
                    description: Missing or invalid authentication.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '403':
                    description: User is forbidden with current credentials
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '404':
                    description: Unlinked PA template type not found.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                    content:
                      application/json:
                        schema:
                          $ref: '#/components/schemas/ClientErrorResponse'
                  '406':
                    description: >-
                      Unsupported Accept header. Header needs to be set to
                      application/json.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      X-FactSet-Api-RateLimit-Limit:
                        description: Number of allowed requests for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Remaining:
                        description: Number of requests left for the time window.
                        schema:
                          type: string
                      X-FactSet-Api-RateLimit-Reset:
                        description: Number of seconds remaining till rate limit resets.
                        schema:
                          type: string
                  '429':
                    description: >-
                      Rate limit reached. Wait till the time specified in
                      Retry-After header value to make further requests.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                      Retry-After:
                        description: >-
                          Time to wait in seconds before making a new request as
                          the rate limit has reached.
                        schema:
                          type: string
                  '500':
                    description: >-
                      Server error. Log the X-DataDirect-Request-Key header to
                      assist in troubleshooting.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
                  '503':
                    description: Request timed out. Retry the request in sometime.
                    headers:
                      X-DataDirect-Request-Key:
                        description: FactSet's request key header.
                        schema:
                          type: string
                          description: FactSet's request key header.
                      X-FactSet-Api-Request-Key:
                        description: >-
                          Key to uniquely identify an Analytics API request.
                          Only available after successful authentication.
                        schema:
                          type: string
                          description: >-
                            Key to uniquely identify an Analytics API request.
                            Only available after successful authentication.
          components:
            schemas:
              AccountDirectories:
                type: object
                properties:
                  accounts:
                    type: array
                    items:
                      type: string
                    description: List of account and composite files.
                    nullable: true
                  directories:
                    type: array
                    items:
                      type: string
                    description: List of directories.
                    nullable: true
              AccountDirectoriesRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/AccountDirectories'
                  meta:
                    nullable: true
              ErrorSource:
                type: object
                properties:
                  pointer:
                    type: string
                    nullable: true
                  parameter:
                    type: string
                    nullable: true
              Error:
                type: object
                properties:
                  id:
                    type: string
                    nullable: true
                  code:
                    type: string
                    nullable: true
                  title:
                    type: string
                    nullable: true
                  detail:
                    type: string
                    nullable: true
                  source:
                    $ref: '#/components/schemas/ErrorSource'
              ClientErrorResponse:
                type: object
                properties:
                  errors:
                    type: array
                    items:
                      $ref: '#/components/schemas/Error'
                    nullable: true
              ColumnSummary:
                type: object
                properties:
                  name:
                    type: string
                    description: Column Name
                    nullable: true
                  directory:
                    type: string
                    description: Column Directory
                    nullable: true
                  category:
                    type: string
                    description: Column Category
                    nullable: true
                description: Column settings (name, directory, category)
              ColumnSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/ColumnSummary'
                  meta:
                    nullable: true
              Column:
                type: object
                properties:
                  defaultstatisticsids:
                    type: array
                    items:
                      type: string
                    description: Column statistic Id
                    nullable: true
                  name:
                    type: string
                    description: Column Name
                    nullable: true
                  directory:
                    type: string
                    description: Column Directory
                    nullable: true
                  category:
                    type: string
                    description: Column Category
                    nullable: true
              ColumnRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/Column'
                  meta:
                    nullable: true
              ColumnStatistic:
                type: object
                properties:
                  name:
                    type: string
                    description: Column Statistic Name
                    nullable: true
              ColumnStatisticRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/ColumnStatistic'
                  meta:
                    nullable: true
              ComponentSummary:
                type: object
                properties:
                  name:
                    type: string
                    description: Component name.
                    nullable: true
                  category:
                    type: string
                    description: Component category.
                    nullable: true
              ComponentSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/ComponentSummary'
                  meta:
                    nullable: true
              PAIdentifier:
                required:
                  - id
                type: object
                properties:
                  id:
                    type: string
                    description: User's FactSet account path OR benchmark.
                  holdingsmode:
                    type: string
                    description: Holdings Mode can be B&H, TBR, OMS, EXT or VLT.
                    nullable: true
              PADateParameters:
                required:
                  - enddate
                  - frequency
                type: object
                properties:
                  startdate:
                    type: string
                    description: Calculation's start date.
                    nullable: true
                  enddate:
                    type: string
                    description: Calculation's end date.
                  frequency:
                    type: string
                    description: Calculation's frequency.
                description: The date parameters for PA calculation.
              PAComponent:
                type: object
                properties:
                  id:
                    type: string
                    description: Component identifier.
                    nullable: true
                  accounts:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of accounts saved in the PA document.
                    nullable: true
                  benchmarks:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of benchmarks saved in the PA document.
                    nullable: true
                  currencyisocode:
                    type: string
                    nullable: true
                  dates:
                    $ref: '#/components/schemas/PADateParameters'
                  snapshot:
                    type: boolean
                    description: Is the component type snapshot or subperiod.
                  path:
                    type: string
                    description: The path to the document
                    nullable: true
                  name:
                    type: string
                    description: Component name.
                    nullable: true
                  category:
                    type: string
                    description: Component category.
                    nullable: true
              PAComponentRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/PAComponent'
                  meta:
                    nullable: true
              Currency:
                type: object
                properties:
                  name:
                    type: string
                    description: Name of currency.
                    nullable: true
              CurrencyRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/Currency'
                  meta:
                    nullable: true
              DateParametersSummary:
                type: object
                properties:
                  startdate:
                    type: string
                    description: Start date in YYYYMMDD format.
                    nullable: true
                  enddate:
                    type: string
                    description: End date in YYYYMMDD format.
                    nullable: true
              DateParametersSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/DateParametersSummary'
                  meta:
                    nullable: true
              DocumentDirectories:
                type: object
                properties:
                  documents:
                    type: array
                    items:
                      type: string
                    description: List of documents
                    nullable: true
                  directories:
                    type: array
                    items:
                      type: string
                    description: List of directories.
                    nullable: true
              DocumentDirectoriesRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/DocumentDirectories'
                  meta:
                    nullable: true
              Frequency:
                type: object
                properties:
                  name:
                    type: string
                    description: Frequency name.
                    nullable: true
              FrequencyRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/Frequency'
                  meta:
                    nullable: true
              Group:
                type: object
                properties:
                  name:
                    type: string
                    description: Group Name
                    nullable: true
                  directory:
                    type: string
                    description: Group Directory
                    nullable: true
                  category:
                    type: string
                    description: Group Category
                    nullable: true
              GroupRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/Group'
                  meta:
                    nullable: true
              TemplateContentTypes:
                type: object
                properties:
                  mandatory:
                    type: array
                    items:
                      type: string
                    description: Template mandatory fields
                    nullable: true
                  optional:
                    type: array
                    items:
                      type: string
                    description: Template optional fields
                    nullable: true
                  locked:
                    type: array
                    items:
                      type: string
                    description: Template locked fields
                    nullable: true
              LinkedPATemplateParameters:
                required:
                  - directory
                  - parentComponentId
                type: object
                properties:
                  directory:
                    type: string
                    description: The directory to create a linked PA template
                  parentComponentId:
                    type: string
                    description: Parent component id
                  description:
                    type: string
                    description: Template description
                    nullable: true
                  content:
                    $ref: '#/components/schemas/TemplateContentTypes'
              LinkedPATemplateParametersRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/LinkedPATemplateParameters'
                  meta:
                    nullable: true
              LinkedPATemplatePostSummary:
                type: object
                properties:
                  id:
                    type: string
                    description: Template id.
                    nullable: true
                  description:
                    type: string
                    description: Template description.
                    nullable: true
                  name:
                    type: string
                    description: Template name.
                    nullable: true
                  parentComponentId:
                    type: string
                    description: Template parent tile.
                    nullable: true
              LinkedPATemplatePostSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/LinkedPATemplatePostSummary'
                  meta:
                    nullable: true
              LinkedPATemplateSummary:
                type: object
                properties:
                  description:
                    type: string
                    description: Template description.
                    nullable: true
                  name:
                    type: string
                    description: Template name.
                    nullable: true
                  parentComponentId:
                    type: string
                    description: Template parent tile.
                    nullable: true
              LinkedPATemplateSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/LinkedPATemplateSummary'
                  meta:
                    nullable: true
              LinkedPATemplateUpdateParameters:
                type: object
                properties:
                  parentComponentId:
                    type: string
                    description: Parent component id
                    nullable: true
                  description:
                    type: string
                    description: Template description
                    nullable: true
                  content:
                    $ref: '#/components/schemas/TemplateContentTypes'
              LinkedPATemplateUpdateParametersRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/LinkedPATemplateUpdateParameters'
                  meta:
                    nullable: true
              LinkedPATemplate:
                type: object
                properties:
                  directory:
                    type: string
                    description: Template directory.
                    nullable: true
                  snapshot:
                    type: boolean
                    description: snapshot.
                  content:
                    $ref: '#/components/schemas/TemplateContentTypes'
                  id:
                    type: string
                    description: Template id.
                    nullable: true
                  description:
                    type: string
                    description: Template description.
                    nullable: true
                  name:
                    type: string
                    description: Template name.
                    nullable: true
                  parentComponentId:
                    type: string
                    description: Template parent tile.
                    nullable: true
              LinkedPATemplateRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/LinkedPATemplate'
                  meta:
                    nullable: true
              PACalculationGroup:
                type: object
                properties:
                  id:
                    type: string
                    description: FactSet-defined or User-defined Group identifier.
                    nullable: true
                  frequency:
                    type: string
                    description: Grouping frequency
                    nullable: true
              PACalculationColumn:
                type: object
                properties:
                  id:
                    type: string
                    description: FactSet-defined or User-defined Column identifier.
                    nullable: true
                  statistics:
                    type: array
                    items:
                      type: string
                    description: Column Statistic identifier
                    nullable: true
              PACalculationPricingSource:
                type: object
                properties:
                  id:
                    type: string
                    description: Pricing source identifier
                    nullable: true
              PACalculationDataSources:
                type: object
                properties:
                  portfoliopricingsources:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationPricingSource'
                    description: List of portfilio pricing source for the PA calculation
                    nullable: true
                  benchmarkpricingsources:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationPricingSource'
                    description: List of benchmark pricing source for the PA calculation
                    nullable: true
                  useportfoliopricingsourcesforbenchmark:
                    type: boolean
                    description: Use portfolio pricing sources for benchmark
                    nullable: true
              PACalculationParameters:
                required:
                  - componentid
                type: object
                properties:
                  componentid:
                    type: string
                    description: The PA Engine component identifier to analyze.
                  accounts:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of accounts.
                    nullable: true
                  benchmarks:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of benchmarks.
                    nullable: true
                  dates:
                    $ref: '#/components/schemas/PADateParameters'
                  groups:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationGroup'
                    description: >-
                      List of groupings for the PA calculation. This will take
                      precedence over the groupings saved in the PA document.
                    nullable: true
                  currencyisocode:
                    type: string
                    description: Currency ISO code for calculation.
                    nullable: true
                  columns:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationColumn'
                    description: >-
                      List of columns for the PA calculation. This will take
                      precedence over the columns saved in the PA document.
                    nullable: true
                  datasources:
                    $ref: '#/components/schemas/PACalculationDataSources'
                  componentdetail:
                    type: string
                    description: >-
                      Component detail type for the PA component. It can be
                      GROUPS or GROUPSALL or TOTALS or SECURITIES.
                    nullable: true
              CalculationMeta:
                type: object
                properties:
                  contentorganization:
                    enum:
                      - None
                      - Row
                      - Column
                      - SimplifiedRow
                    type: string
                    default: SimplifiedRow
                    deprecated: true
                  stachContentOrganization:
                    enum:
                      - None
                      - Row
                      - Column
                      - SimplifiedRow
                    type: string
                    default: SimplifiedRow
                  contenttype:
                    enum:
                      - Json
                      - Binary
                    type: string
                    default: Json
                    deprecated: true
                  format:
                    enum:
                      - JsonStach
                      - Table
                      - Tableau
                      - BinaryStach
                      - Bison
                      - Binary
                      - Pdf
                      - Pptx
                      - Feather
                    type: string
                    default: JsonStach
              PACalculationParametersRoot:
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/PACalculationParameters'
                    description: List of calculation parameters.
                    nullable: true
                  meta:
                    $ref: '#/components/schemas/CalculationMeta'
              CalculationUnitStatus:
                type: object
                properties:
                  status:
                    enum:
                      - Queued
                      - Executing
                      - Success
                      - Failed
                      - Cancelled
                    type: string
                    description: The status of calculation unit.
                  errors:
                    type: array
                    items:
                      $ref: '#/components/schemas/Error'
                    description: The error in a calculation unit.
                    nullable: true
                  result:
                    type: string
                    description: The result URL of the calculation.
                    nullable: true
                  progress:
                    type: string
                    description: The progress of the calculation unit.
                    nullable: true
                  points:
                    type: integer
                    description: The points for the calculation unit.
                    format: int32
                    nullable: true
                  warnings:
                    type: array
                    items:
                      type: string
                    description: The warnings in a calculation unit.
                    nullable: true
              CalculationStatus:
                type: object
                properties:
                  calculationid:
                    type: string
                    description: Calculation's identifier
                    nullable: true
                  status:
                    enum:
                      - Queued
                      - Executing
                      - Completed
                      - Cancelled
                    type: string
                    description: Calculation's status
                  units:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/CalculationUnitStatus'
                    description: Number of calculation units in batch.
                    nullable: true
              CalculationUnitStatusMeta:
                type: object
                properties:
                  info:
                    type: string
                    description: The Info URL of the calculation.
                    nullable: true
              CalculationStatusMeta:
                type: object
                properties:
                  units:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/CalculationUnitStatusMeta'
                    description: Meta of calculation units in batch.
                    nullable: true
              CalculationStatusRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/CalculationStatus'
                  meta:
                    $ref: '#/components/schemas/CalculationStatusMeta'
              ObjectRoot:
                required:
                  - data
                type: object
                properties:
                  data: {}
                  meta:
                    nullable: true
              CalculationsSummary:
                type: object
                properties:
                  status:
                    enum:
                      - Queued
                      - Executing
                      - Completed
                      - Cancelled
                    type: string
                    description: Last poll status of the calculation.
                  units:
                    type: integer
                    description: Number of calculation units in batch.
                    format: int32
                  requestTime:
                    type: string
                    description: Request time of calculation.
                    format: date-time
                  lastPollTime:
                    type: string
                    description: Last poll time of calculation.
                    format: date-time
              PaginationInfo:
                type: object
                properties:
                  pageNumber:
                    type: integer
                    format: int32
                  pageSize:
                    type: integer
                    format: int32
                  totalPages:
                    type: integer
                    format: int32
                  totalCalculations:
                    type: integer
                    format: int32
                  nextPage:
                    type: string
                    nullable: true
                  previousPage:
                    type: string
                    nullable: true
              PaginationMeta:
                type: object
                properties:
                  pagination:
                    $ref: '#/components/schemas/PaginationInfo'
              CalculationsSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/CalculationsSummary'
                  meta:
                    $ref: '#/components/schemas/PaginationMeta'
              PAPricingSource:
                type: object
                properties:
                  name:
                    type: string
                    description: Pricing source Name
                    nullable: true
                  directory:
                    type: string
                    description: Pricing source directory
                    nullable: true
                  category:
                    type: string
                    description: Pricing source category
                    nullable: true
              PAPricingSourceRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/PAPricingSource'
                  meta:
                    nullable: true
              PAComponentData:
                type: object
                properties:
                  accounts:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of accounts.
                    nullable: true
                  benchmarks:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of benchmarks.
                    nullable: true
                  groups:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationGroup'
                    description: >-
                      List of groupings for the PA calculation. This will take
                      precedence over the groupings saved in the PA document.
                    nullable: true
                  columns:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationColumn'
                    description: >-
                      List of columns for the PA calculation. This will take
                      precedence over the columns saved in the PA document.
                    nullable: true
                  dates:
                    $ref: '#/components/schemas/PADateParameters'
                  datasources:
                    $ref: '#/components/schemas/PACalculationDataSources'
                  currencyisocode:
                    type: string
                    description: Currency ISO code for calculation.
                    nullable: true
                  componentdetail:
                    type: string
                    description: >-
                      PA Storage type. It can be GROUPS or GROUPSALL or TOTALS
                      or SECURITIES.
                    nullable: true
              TemplatedPAComponentParameters:
                required:
                  - directory
                  - parentTemplateId
                type: object
                properties:
                  directory:
                    type: string
                    description: Directory to create templated components
                  parentTemplateId:
                    type: string
                    description: Parent template id
                  description:
                    type: string
                    description: Component description.
                    nullable: true
                  componentData:
                    $ref: '#/components/schemas/PAComponentData'
              TemplatedPAComponentParametersRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/TemplatedPAComponentParameters'
                  meta:
                    nullable: true
              TemplatedPAComponentPostSummary:
                type: object
                properties:
                  id:
                    type: string
                    nullable: true
                  description:
                    type: string
                    nullable: true
                  name:
                    type: string
                    nullable: true
                  parentTemplateId:
                    type: string
                    nullable: true
                  type:
                    type: string
                    nullable: true
              TemplatedPAComponentPostSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/TemplatedPAComponentPostSummary'
                  meta:
                    nullable: true
              TemplatedPAComponentSummary:
                type: object
                properties:
                  description:
                    type: string
                    nullable: true
                  name:
                    type: string
                    nullable: true
                  parentTemplateId:
                    type: string
                    nullable: true
                  type:
                    type: string
                    nullable: true
              TemplatedPAComponentSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/TemplatedPAComponentSummary'
                  meta:
                    nullable: true
              TemplatedPAComponentUpdateParameters:
                type: object
                properties:
                  parentTemplateId:
                    type: string
                    description: Parent template id
                    nullable: true
                  description:
                    type: string
                    description: Component description.
                    nullable: true
                  componentData:
                    $ref: '#/components/schemas/PAComponentData'
              TemplatedPAComponentUpdateParametersRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/TemplatedPAComponentUpdateParameters'
                  meta:
                    nullable: true
              TemplatedPAComponent:
                type: object
                properties:
                  id:
                    type: string
                    nullable: true
                  directory:
                    type: string
                    nullable: true
                  snapshot:
                    type: boolean
                  componentData:
                    $ref: '#/components/schemas/PAComponentData'
                  description:
                    type: string
                    nullable: true
                  name:
                    type: string
                    nullable: true
                  parentTemplateId:
                    type: string
                    nullable: true
                  type:
                    type: string
                    nullable: true
              TemplatedPAComponentRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/TemplatedPAComponent'
                  meta:
                    nullable: true
              UnlinkedPATemplateParameters:
                required:
                  - directory
                  - templateTypeId
                type: object
                properties:
                  directory:
                    type: string
                    description: The directory to create an unlinked PA template
                  templateTypeId:
                    type: string
                    description: Template type id
                  description:
                    type: string
                    description: Template description
                    nullable: true
                  accounts:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of accounts
                    nullable: true
                  benchmarks:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of benchmarks
                    nullable: true
                  columns:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationColumn'
                    description: List of columns for the PA calculation
                    nullable: true
                  dates:
                    $ref: '#/components/schemas/PADateParameters'
                  groups:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationGroup'
                    description: List of groupings for the PA calculation
                    nullable: true
                  datasources:
                    $ref: '#/components/schemas/PACalculationDataSources'
                  currencyisocode:
                    type: string
                    description: Currency ISO code for calculation.
                    nullable: true
                  componentdetail:
                    type: string
                    description: >-
                      PA storage type. It can be GROUPS or GROUPSALL or TOTALS
                      or SECURITIES.
                    nullable: true
                  content:
                    $ref: '#/components/schemas/TemplateContentTypes'
              UnlinkedPATemplateParametersRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/UnlinkedPATemplateParameters'
                  meta:
                    nullable: true
              UnlinkedPATemplatePostSummary:
                type: object
                properties:
                  id:
                    type: string
                    description: Template id.
                    nullable: true
                  description:
                    type: string
                    description: Template description.
                    nullable: true
                  name:
                    type: string
                    description: Template name.
                    nullable: true
                  category:
                    type: string
                    description: Unlinked template category
                    nullable: true
              UnlinkedPATemplatePostSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/UnlinkedPATemplatePostSummary'
                  meta:
                    nullable: true
              UnlinkedPATemplateSummary:
                type: object
                properties:
                  description:
                    type: string
                    description: Template description.
                    nullable: true
                  name:
                    type: string
                    description: Template name.
                    nullable: true
                  category:
                    type: string
                    description: Unlinked template category
                    nullable: true
              UnlinkedPATemplateSummaryRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/UnlinkedPATemplateSummary'
                  meta:
                    nullable: true
              UnlinkedPATemplateUpdateParameters:
                type: object
                properties:
                  description:
                    type: string
                    description: Template description
                    nullable: true
                  accounts:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of accounts
                    nullable: true
                  benchmarks:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of benchmarks
                    nullable: true
                  columns:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationColumn'
                    description: List of columns for the PA calculation
                    nullable: true
                  dates:
                    $ref: '#/components/schemas/PADateParameters'
                  groups:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationGroup'
                    description: List of groupings for the PA calculation
                    nullable: true
                  datasources:
                    $ref: '#/components/schemas/PACalculationDataSources'
                  currencyisocode:
                    type: string
                    description: Currency ISO code for calculation.
                    nullable: true
                  componentdetail:
                    type: string
                    description: >-
                      PA storage type. It can be GROUPS or GROUPSALL or TOTALS
                      or SECURITIES.
                    nullable: true
                  content:
                    $ref: '#/components/schemas/TemplateContentTypes'
              UnlinkedPATemplateUpdateParametersRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/UnlinkedPATemplateUpdateParameters'
                  meta:
                    nullable: true
              UnlinkedPATemplate:
                type: object
                properties:
                  id:
                    type: string
                    description: Template id.
                    nullable: true
                  directory:
                    type: string
                    description: Template directory.
                    nullable: true
                  templateTypeId:
                    type: string
                    description: Template type id
                    nullable: true
                  snapshot:
                    type: boolean
                    description: snapshot.
                  accounts:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of accounts
                    nullable: true
                  benchmarks:
                    type: array
                    items:
                      $ref: '#/components/schemas/PAIdentifier'
                    description: List of benchmarks
                    nullable: true
                  columns:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationColumn'
                    description: List of columns for the PA calculation
                    nullable: true
                  dates:
                    $ref: '#/components/schemas/PADateParameters'
                  groups:
                    type: array
                    items:
                      $ref: '#/components/schemas/PACalculationGroup'
                    description: List of groupings for the PA calculation
                    nullable: true
                  datasources:
                    $ref: '#/components/schemas/PACalculationDataSources'
                  currencyisocode:
                    type: string
                    description: Currency ISO code for calculation.
                    nullable: true
                  componentdetail:
                    type: string
                    description: >-
                      PA storage type. It can be GROUPS or GROUPSALL or TOTALS
                      or SECURITIES.
                    nullable: true
                  content:
                    $ref: '#/components/schemas/TemplateContentTypes'
                  description:
                    type: string
                    description: Template description.
                    nullable: true
                  name:
                    type: string
                    description: Template name.
                    nullable: true
                  category:
                    type: string
                    description: Unlinked template category
                    nullable: true
              UnlinkedPATemplateRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: '#/components/schemas/UnlinkedPATemplate'
                  meta:
                    nullable: true
              UnlinkedPATemplateCategoryAndType:
                type: object
                properties:
                  category:
                    type: string
                    description: Unlinked template category
                    nullable: true
                  name:
                    type: string
                    description: Unlinked template type
                    nullable: true
              UnlinkedPATemplateCategoryAndTypeRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    type: object
                    additionalProperties:
                      $ref: '#/components/schemas/UnlinkedPATemplateCategoryAndType'
                  meta:
                    nullable: true
              UnlinkedPATemplateColumnDetails:
                type: object
                properties:
                  name:
                    type: string
                    description: Unlinked template column name
                    nullable: true
                  id:
                    type: string
                    description: FactSet-defined or User-defined Column identifier.
                    nullable: true
                  statistics:
                    type: array
                    items:
                      type: string
                    description: Column Statistic identifier
                    nullable: true
              UnlinkedPATemplateGroupDetails:
                type: object
                properties:
                  name:
                    type: string
                    description: Unlinked template group name
                    nullable: true
                  id:
                    type: string
                    description: FactSet-defined or User-defined Group identifier.
                    nullable: true
                  frequency:
                    type: string
                    description: Grouping frequency
                    nullable: true
              UnlinkedPATemplateCategoryAndTypeDetails:
                type: object
                properties:
                  id:
                    type: string
                    description: Type Id
                    nullable: true
                  columns:
                    type: array
                    items:
                      $ref: '#/components/schemas/UnlinkedPATemplateColumnDetails'
                    description: List of default columns
                    nullable: true
                  groups:
                    type: array
                    items:
                      $ref: '#/components/schemas/UnlinkedPATemplateGroupDetails'
                    description: List of default groupings
                    nullable: true
                  snapshot:
                    type: boolean
                    description: Snapshot
                  category:
                    type: string
                    description: Unlinked template category
                    nullable: true
                  name:
                    type: string
                    description: Unlinked template type
                    nullable: true
              UnlinkedPATemplateCategoryAndTypeDetailsRoot:
                required:
                  - data
                type: object
                properties:
                  data:
                    $ref: >-
                      #/components/schemas/UnlinkedPATemplateCategoryAndTypeDetails
                  meta:
                    nullable: true
            securitySchemes:
              FactSetApiKey:
                type: http
                scheme: basic
              FactSetOAuth2:
                type: oauth2
                flows:
                  clientCredentials:
                    tokenUrl: https://auth.factset.com/as/token.oauth2
                    scopes: {}
          security:
            - FactSetApiKey: []
            - FactSetOAuth2: []
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/pa-engine-api
    overlays:
      - type: API Evangelist Ratings
        url: overlays/pa-engine-openapi-api-evangelist-ratings.yml
      - type: APIs.io Search
        url: overlays/pa-engine-openapi-search.yml
    aid: factset:factset-pa-engine-api
  - name: FactSet SPAR Engine API
    description: >-
      Through the SPAR API (Style, Performance, and Risk) monitor your
      portfolios’ returns against equity and fixed income benchmarks, and peer
      universes, with MPT risk statistics such as beta, standard deviation,
      r-squared, alpha, and tracking error…
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/spar-engine-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/spar-engine-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/spar-engine-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/spar-engine-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/spar-engine-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/spar-engine-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: SPAR Engine API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /analytics/engines/spar/v3/accounts/{accountPath}/returns-type:
              get:
                tags:
                  - Get
                  - Account
                  - Returns
                  - Type
                  - Details
                  - Path
                  - Returns
                  - Type
                summary: Get SPAR account returns type details
                description: >-
                  This endpoint returns the returns type of account associated
                  with SPAR
            /analytics/lookups/v3/accounts/{path}:
              get:
                tags:
                  - Get
                  - Accounts
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                summary: Get accounts and sub-directories in a directory
                description: >-
                  This endpoint looks up all ACCT and ACTM files and
                  sub-directories in a given directory.
            /analytics/engines/spar/v3/benchmarks:
              get:
                tags:
                  - Get
                  - Benchmark
                  - Details
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                summary: Get SPAR benchmark details
                description: >-
                  This endpoint returns the details of a given SPAR benchmark
                  identifier.
            /analytics/engines/spar/v3/components:
              get:
                tags:
                  - Get
                  - Components
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                summary: Get SPAR components
                description: >-
                  This endpoint returns the list of SPAR components in a given
                  SPAR document.
            /analytics/engines/spar/v3/components/{id}:
              get:
                tags:
                  - Get
                  - Component
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                summary: Get SPAR component by id
                description: >-
                  This endpoint returns the default settings of a SPAR
                  component.
            /analytics/lookups/v3/currencies:
              get:
                tags:
                  - Get
                  - Currencies
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                summary: Get currencies
                description: >-
                  This endpoint lists all the currencies that can be applied to
                  any calculation.
            /analytics/engines/spar/v3/documents/{path}:
              get:
                tags:
                  - Gets
                  - R3
                  - Documents
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                summary: Gets SPAR3 documents and sub-directories in a directory
                description: >-
                  This endpoint looks up all SPAR3 documents and sub-directories
                  in a given directory.
            /analytics/engines/spar/v3/frequencies:
              get:
                tags:
                  - Get
                  - Frequencies
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                summary: Get SPAR frequencies
                description: >-
                  This endpoint lists all the frequencies that can be applied to
                  a SPAR calculation.
            /analytics/engines/spar/v3/calculations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Calculation
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Create and Run SPAR calculation
                description: "This endpoint runs the SPAR calculation specified in the POST body parameters.\r\nIt can take one or more units as input.\r\n\r\nRemarks:\r\n\r\n*\tAny settings in POST body will act as a one-time override over the settings saved in the SPAR template."
              get:
                tags:
                  - Get
                  - All
                  - Calculations
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Get all calculations
                description: This endpoints returns all calculation requests.
            /analytics/engines/spar/v3/calculations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Calculation
                  - And
                  - Run
                  - It.
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Create or Update SPAR calculation and run it.
                description: "This endpoint updates and run the SPAR calculation specified in the PUT body parameters. This also allows creating new SPAR calculations with custom ids.\r\nIt can take one or more units as input.\r\n\r\nRemarks:\r\n\r\n*\tAny settings in PUT body will act as a one-time override over the settings saved in the SPAR template."
              get:
                tags:
                  - Get
                  - Calculation
                  - Parameters
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Get SPAR calculation parameters by id
                description: >-
                  This is the endpoint that returns the calculation parameters
                  passed for a calculation.
              delete:
                tags:
                  - Cancel
                  - Calculation
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                summary: Cancel SPAR calculation
                description: >-
                  This is the endpoint to cancel a previously submitted
                  calculation.
            /analytics/engines/spar/v3/calculations/{id}/status:
              get:
                tags:
                  - Get
                  - Calculation
                  - Status
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                  - Status
                summary: Get SPAR calculation status by id
                description: "This is the endpoint to check on the progress of a previously requested calculation.\r\nIf the calculation has finished computing, the location header will point to the result url."
            /analytics/engines/spar/v3/calculations/{id}/units/{unitId}/result:
              get:
                tags:
                  - Get
                  - Calculation
                  - Result
                  - By
                  - Id
                  - Path
                  - Returns
                  - Type
                  - Analytics
                  - Lookups
                  - V3
                  - Accounts
                  - Engines
                  - Spar
                  - Benchmarks
                  - Components
                  - Id
                  - Currencies
                  - Documents
                  - Frequencies
                  - Calculations
                  - Status
                  - Result
                summary: Get SPAR calculation result by id
                description: "This is the endpoint to get the result of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON."
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catal
    overlays:
      - type: APIs.io Search
        url: overlays/spar-engine-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/spar-engine-openapi-api-evangelist-ratings.yml
    aid: factset:factset-spar-engine-api
  - name: FactSet Vault API
    description: >-
      Through the Vault API, request validated pre-calculated returns and
      attribution data archived in Portfolio Vault to streamline your official
      performance and reporting workflows.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/vault-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/vault-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/vault-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/vault-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/vault-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/vault-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Vault API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /analytics/engines/vault/v3/components:
              get:
                tags:
                  - Get
                  - Vault
                  - Components
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                summary: Get Vault components
                description: >-
                  This endpoint returns the list of Vault components in a given
                  Vault document.
            /analytics/engines/vault/v3/components/{id}:
              get:
                tags:
                  - Get
                  - Vault
                  - Component
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                summary: Get Vault component by id
                description: >-
                  This endpoint returns the default settings of a Vault
                  component.
            /analytics/engines/vault/v3/configurations:
              get:
                tags:
                  - Get
                  - Vault
                  - Configurations
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                summary: Get Vault configurations
                description: >-
                  This endpoint returns all the Vault configurations saved in
                  the provided account.
            /analytics/engines/vault/v3/configurations/{id}:
              get:
                tags:
                  - Get
                  - Vault
                  - Configuration
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                summary: Get Vault configuration by id
                description: >-
                  This endpoint returns details for a Vault configuration as
                  well as a list of accounts it is used in.
            /analytics/engines/vault/v3/dates:
              get:
                tags:
                  - Convert
                  - Vault
                  - Dates
                  - To
                  - Absolute
                  - Format
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                summary: Convert Vault dates to absolute format
                description: >-
                  This endpoint converts the given start and end dates in
                  FactSet date format to yyyymmdd format for a Vault
                  calculation. For more information on FactSet date format,
                  please refer to the Vault API documentation under the 'API
                  Documentation' section in the developer portal.
            /analytics/engines/vault/v3/documents/{path}:
              get:
                tags:
                  - Get
                  - Vault
                  - Documents
                  - And
                  - Sub-directories
                  - In
                  - Directory
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                summary: Get Vault documents and sub-directories in a directory
                description: >-
                  This endpoint looks up all Vault documents and sub-directories
                  in a given directory.
            /analytics/engines/vault/v3/frequencies:
              get:
                tags:
                  - Get
                  - Vault
                  - Frequencies
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                summary: Get Vault frequencies
                description: >-
                  This endpoint lists all the frequencies that can be applied to
                  a Vault calculation.
            /analytics/engines/vault/v3/calculations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Vault
                  - Calculation
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                summary: Create and Run Vault calculation
                description: "This endpoint runs the Vault calculation specified in the POST body parameters.\r\nIt can take one or more units as input.\r\n\r\nRemarks:\r\n\r\n*   Start and and end date must be within the configuration's min and max date range"
              get:
                tags:
                  - Get
                  - All
                  - Calculations
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                summary: Get all calculations
                description: This endpoints returns all calculation requests.
            /analytics/engines/vault/v3/calculations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Vault
                  - Calculation
                  - And
                  - Run
                  - It.
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                summary: Create or Update Vault calculation and run it.
                description: "This endpoint updates and run the Vault calculation specified in the PUT body parameters. This also allows creating new Vault calculations with custom ids.\r\nIt can take one or more units as input.\r\n\r\nRemarks:\r\n\r\n*   Start and and end date must be within the configuration's min and max date range"
              get:
                tags:
                  - Get
                  - Vault
                  - Calculation
                  - Parameters
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                summary: Get Vault calculation parameters by id
                description: >-
                  This is the endpoint that returns the calculation parameters
                  passed for a calculation.
              delete:
                tags:
                  - Cancel
                  - Vault
                  - Calculation
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                summary: Cancel Vault calculation by id
                description: >-
                  This is the endpoint to cancel a previously submitted
                  calculation.
            /analytics/engines/vault/v3/calculations/{id}/status:
              get:
                tags:
                  - Get
                  - Vault
                  - Calculation
                  - Status
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                  - Status
                summary: Get Vault calculation status by id
                description: "This is the endpoint to check on the progress of a previously requested calculation.\r\nIf the calculation has finished computing, the location header will point to the result url."
            /analytics/engines/vault/v3/calculations/{id}/units/{unitId}/result:
              get:
                tags:
                  - Get
                  - Vault
                  - Calculation
                  - Result
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Vault
                  - V3
                  - Components
                  - Id
                  - Configurations
                  - Dates
                  - Documents
                  - Path
                  - Frequencies
                  - Calculations
                  - Status
                  - Result
                summary: Get Vault calculation result by id
                description: "This is the endpoint to get the result of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON."
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api
    overlays:
      - type: APIs.io Search
        url: overlays/vault-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/vault-openapi-api-evangelist-ratings.yml
    aid: factset:factset-vault-api
  - name: FactSet Fixed Income Analytics Batcher API
    description: >-
      The Fixed Income Analytics Batcher API allows the user to enrich portfolio
      holdings with fixed income analytics and monitor requests interactively.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/fixed-income-analytics-batcher-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-analytics-batcher-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-analytics-batcher-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-analytics-batcher-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-analytics-batcher-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-analytics-batcher-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: FIAB API
            license:
              name: Apache License 2.0
              url: http://www.apache.org/licenses/LICENSE-2.0.txt
          paths:
            /analytics/engines/fiab/v1/calculations:
              post:
                tags:
                  - Run
                  - Calculation
                  - Analytics
                  - Engines
                  - Fiab
                  - V1
                  - Calculations
                summary: Run FIAB calculation
                description: "This endpoint creates a new FIAB calculation.\r\nThis must be used first before get status or cancelling endpoints with a calculation id.\r\nA successful response will contain the URL to check the status of the calculation request.\r\n\r\nRemarks:\r\n*\tAny settings in POST body will act as a one-time override over the settings saved in the FIAB template."
              get:
                tags:
                  - Get
                  - All
                  - Calculation
                  - Summaries
                  - Analytics
                  - Engines
                  - Fiab
                  - V1
                  - Calculations
                summary: Get all FIAB calculation summaries
                description: This endpoints returns all FIAB calculation requests.
            /analytics/engines/fiab/v1/calculations/{id}:
              get:
                tags:
                  - Get
                  - Calculation
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Fiab
                  - V1
                  - Calculations
                  - Id
                summary: Get FIAB calculation by id
                description: >-
                  This is the endpoint to check on the progress of a previously
                  r
    overlays:
      - type: APIs.io Search
        url: overlays/fixed-income-analytics-batcher-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/fixed-income-analytics-batcher-openapi-api-evangelist-ratings.yml
    aid: factset:factset-fixed-income-analytics-batcher-api
  - name: FactSet Fixed Income Calculation API
    description: >-
      Leverage FactSet's Fixed Income Calculation Engine to derive analytics on
      the fly
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/fixed-income-calculation-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-calculation-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-calculation-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-calculation-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-calculation-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/fixed-income-calculation-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: FI API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /analytics/engines/fi/v3/discount-curves:
              get:
                tags:
                  - Get
                  - Discount
                  - Curves
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                summary: Get Discount Curves
                description: >-
                  This endpoint lists all the discount curves that can be
                  applied to a FI calculation.
            /analytics/engines/fi/v3/calculations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Calculation
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                  - Calculations
                summary: Create and Run FI calculation
                description: >-
                  This endpoint creates and runs a new FI calculation specified
                  in the post body.
            /analytics/engines/fi/v3/calculations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Calculation
                  - And
                  - Run
                  - It.
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                  - Calculations
                  - Id
                summary: Create or Update FI calculation and run it.
                description: >-
                  This endpoint updates and run the FI optimization specified in
                  the PUT body parameters. It also allows the creation of new FI
                  optimization with custom id.
              get:
                tags:
                  - Get
                  - Calculation
                  - Parameters
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                  - Calculations
                  - Id
                summary: Get FI calculation parameters by id
                description: >-
                  This is the endpoint that returns the calculation parameters
                  passed for a calculation.
              delete:
                tags:
                  - Cancel
                  - Calculation
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                  - Calculations
                  - Id
                summary: Cancel FI calculation by id
                description: >-
                  This is the endpoint to cancel a previously submitted
                  calculation.
            /analytics/engines/fi/v3/calculations/{id}/status:
              get:
                tags:
                  - Get
                  - Calculation
                  - Status
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                  - Calculations
                  - Id
                  - Status
                summary: Get FI calculation status by id
                description: "This is the endpoint to check on the progress of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON.\r\nOtherwise, the calculation is still running and the X-FactSet-Api-PickUp-Progress header will contain a progress percentage."
            /analytics/engines/fi/v3/calculations/{id}/result:
              get:
                tags:
                  - Get
                  - Calculation
                  - Result
                  - By
                  - Id
                  - Analytics
                  - Engines
                  - Fi
                  - V3
                  - Discount
                  - Curves
                  - Calculations
                  - Id
                  - Status
                  - Result
                summary: Get FI calculation result by id
                description: "This is the endpoint to get the result of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON."
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalog/fixed-in
    overlays:
      - type: APIs.io Search
        url: overlays/fixed-income-calculation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/fixed-income-calculation-openapi-api-evangelist-ratings.yml
    aid: factset:factset-fixed-income-calculation-api
  - name: FactSet Quant Engine API
    description: >-
      Use Quant Engine API to retrieve quantitative dataset from FactSet Content
      Database
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://developer.factset.com/api-catalog/quant-engine-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://developer.factset.com/api-catalog/quant-engine-api#overview
      - type: SDKs
        url: https://developer.factset.com/api-catalog/quant-engine-api#sdkLibrary
      - type: Jupyter Notebooks
        url: https://developer.factset.com/api-catalog/quant-engine-api#notebooks
      - type: Code Snippets
        url: https://developer.factset.com/api-catalog/quant-engine-api#codeSnippet
      - type: Change Log
        url: https://developer.factset.com/api-catalog/quant-engine-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.1
          info:
            title: Quant API
            license:
              name: Apache License, Version 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0
          paths:
            /calculations:
              post:
                tags:
                  - Create
                  - And
                  - Run
                  - Quant
                  - Engine
                  - Calculation
                  - Calculations
                summary: Create and Run Quant Engine calculation
                description: "This endpoint runs the Quant Engine calculation specified in the POST body parameters.\r\nIt can take one or more calculation units as input."
              get:
                tags:
                  - Get
                  - All
                  - Calculations
                  - Calculations
                summary: Get all calculations
                description: This endpoints returns all calculation requests.
            /calculations/{id}:
              put:
                tags:
                  - Create
                  - Or
                  - Update
                  - Quant
                  - Engine
                  - Calculation
                  - And
                  - Run
                  - It.
                  - Calculations
                  - Id
                summary: Create or update Quant Engine calculation and run it.
                description: "This endpoint updates and runs the Quant Engine calculation specified in the PUT body parameters. This also allows creating new Quant Engine calculations with custom ids.\r\nIt can take one or more calculation units as input."
              get:
                tags:
                  - Get
                  - Quant
                  - Engine
                  - Calculation
                  - Parameters
                  - By
                  - Id
                  - Calculations
                  - Id
                summary: Get Quant Engine calculation parameters by id
                description: >-
                  This is the endpoint that returns the calculation parameters
                  passed for a calculation.
              delete:
                tags:
                  - Cancel
                  - Quant
                  - Calculation
                  - By
                  - Id
                  - Calculations
                  - Id
                summary: Cancel Quant calculation by id
                description: >-
                  This is the endpoint to cancel a previously submitted
                  calculation.
            /calculations/{id}/status:
              get:
                tags:
                  - Get
                  - Quant
                  - Engine
                  - Calculation
                  - Status
                  - By
                  - Id
                  - Calculations
                  - Id
                  - Status
                summary: Get Quant Engine calculation status by id
                description: "This is the endpoint to check on the progress of a previously requested calculation.\r\nIf the calculation has finished computing, the location header will point to the result url.\r\nOtherwise, the calculation is still running and the X-FactSet-Api-PickUp-Progress header will contain a progress percentage."
            /calculations/{id}/units/{unitId}/result:
              get:
                tags:
                  - Get
                  - Quant
                  - Engine
                  - Calculation
                  - Result
                  - By
                  - Id
                  - Calculations
                  - Id
                  - Status
                  - Result
                summary: Get Quant Engine calculation result by id
                description: "This is the endpoint to get the result of a previously requested calculation.\r\nIf the calculation has finished computing, the body of the response will contain the requested document in JSON."
            /calculations/{id}/units/{unitId}/info:
              get:
                tags:
                  - Get
                  - Quant
                  - Engine
                  - Calculation
                  - Metadata
                  - Information
                  - By
                  - Id
                  - Calculations
                  - Id
                  - Status
                  - Result
                  - Info
                summary: Get Quant Engine calculation metadata information by id
                description: >-
                  This is the endpoint to get the metadata information of a
                  previously requested calculation.
          externalDocs:
            description: API Documentation
            url: https://developer.factset.com/api-catalo
    overlays:
      - type: APIs.io Search
        url: overlays/quant-engine-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/quant-engine-openapi-api-evangelist-ratings.yml
    aid: factset:factset-quant-engine-api
  - name: FactSet Programmatic Environment API
    description: FactSet Programmatic Environment API
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://developer.factset.com/api-catalog/factset-programmatic-environment-api
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: >-
          https://developer.factset.com/api-catalog/factset-programmatic-environment-api#overview
      - type: SDKs
        url: >-
          https://developer.factset.com/api-catalog/factset-programmatic-environment-api#sdkLibrary
      - type: Jupyter Notebooks
        url: >-
          https://developer.factset.com/api-catalog/factset-programmatic-environment-api#notebooks
      - type: Code Snippets
        url: >-
          https://developer.factset.com/api-catalog/factset-programmatic-environment-api#codeSnippet
      - type: Change Log
        url: >-
          https://developer.factset.com/api-catalog/factset-programmatic-environment-api#changelog
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: FPE API
          paths:
            /analytics/quant/fpe/v1/calculations:
              post:
                tags:
                  - Starts
                  - New
                  - Script
                  - Calculation
                  - Analytics
                  - Quant
                  - Fpe
                  - V1
                  - Calculations
                summary: Starts a new script calculation
                description: >-
                  This endpoint takes a python script and starts executing it
                  within FPE
            /analytics/quant/fpe/v1/calculations/{id}:
              get:
                tags:
                  - Get
                  - Calculation
                  - Status
                  - By
                  - Id
                  - Analytics
                  - Quant
                  - Fpe
                  - V1
                  - Calculations
                  - Id
                summary: Get calculation status by id
                description: >-
                  This is the endpoint to check on the progress of a previous
                  calculation request.
            /analytics/quant/fpe/v1/calculations/{id}/output:
              get:
                tags:
                  - Get
                  - Calculation
                  - Output
                  - For
                  - Specific
                  - Analytics
                  - Quant
                  - Fpe
                  - V1
                  - Calculations
                  - Id
                  - Output
                summary: Get calculation output for a specific calculation
                description: >-
                  This endpoint returns the specified output from the
                  calculation.
            /analytics/quant/fpe/v1/calculations/{id}/log:
              get:
                tags:
                  - Get
                  - Calculation
                  - Log
                  - For
                  - Specific
                  - Analytics
                  - Quant
                  - Fpe
                  - V1
                  - Calculations
                  - Id
                  - Output
                  - Log
                summary: Get calculation log for a specific calculation
                description: This endpoint returns the log from the calculation.
            /analytics/quant/fpe/v1/files/{server}/{file}:
              post:
                tags:
                  - Starts
                  - File
                  - Upload
                  - Analytics
                  - Quant
                  - Fpe
                  - V1
                  - Calculations
                  - Id
                  - Output
                  - Log
                  - Files
                  - Server
                  - File
                summary: Starts a file upload
                description: This endpoint takes a file and uploads it
            /analytics/quant/fpe/v1/files/uploads/{id}:
              get:
                tags:
                  - Get
                  - Upload
                  - Status
                  - By
                  - Id
                  - Analytics
                  - Quant
                  - Fpe
                  - V1
                  - Calculations
                  - Id
                  - Output
                  - Log
                  - Files
                  - Server
                  - File
                  - Uploads
                summary: Get upload status by id
                description: This is the endpoint to check on the progress of a pr
    overlays:
      - type: APIs.io Search
        url: overlays/programmatic-environment-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/programmatic-environment-openapi-api-evangelist-ratings.yml
    aid: factset:factset-programmatic-environment-api
  - aid: stripe:stripe-tax-api
    name: Stripe Tax API
    description: >-
      Automate sales tax, VAT, and GST compliance on all your transactions—low
      or no code integrations available.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/tax
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/tax
      - type: OpenAPI
        data:
          openapi: 3.0.0
          info:
            title: Stripe Tax API
          paths:
            /v1/tax/calculations:
              post:
                description: >-
                  <p>Calculates tax based on input and returns a Tax
                  <code>Calculation</code> object.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
            /v1/tax/calculations/{calculation}/line_items:
              get:
                description: >-
                  <p>Retrieves the line items of a persisted tax calculation as
                  a collection.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
            /v1/tax/registrations:
              get:
                description: >-
                  <p>Returns a list of Tax <code>Registration</code>
                  objects.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
              post:
                description: <p>Creates a new Tax <code>Registration</code> object.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
            /v1/tax/registrations/{id}:
              post:
                description: >-
                  <p>Updates an existing Tax <code>Registration</code>
                  object.</p>


                  <p>A registration cannot be deleted after it has been created.
                  If you wish to end a registration you may do so by setting
                  <code>expires_at</code>.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
            /v1/tax/settings:
              get:
                description: <p>Retrieves Tax <code>Settings</code> for a merchant.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
              post:
                description: >-
                  <p>Updates Tax <code>Settings</code> parameters used in tax
                  calculations. All parameters are editable but none can be
                  removed once set.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
            /v1/tax/transactions/create_from_calculation:
              post:
                description: >-
                  <p>Creates a Tax <code>Transaction</code> from a
                  calculation.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
            /v1/tax/transactions/create_reversal:
              post:
                description: >-
                  <p>Partially or fully reverses a previously created
                  <code>Transaction</code>.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
            /v1/tax/transactions/{transaction}:
              get:
                description: <p>Retrieves a Tax <code>Transaction</code> object.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
            /v1/tax/transactions/{transaction}/line_items:
              get:
                description: >-
                  <p>Retrieves the line items of a committed standalone
                  transaction as a collection.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
            /v1/tax_codes:
              get:
                description: >-
                  <p>A list of <a
                  href="https://stripe.com/docs/tax/tax-categories">all tax
                  codes available</a> to add to Products in order to allow
                  specific tax calculations.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
                  - Tax_codes
            /v1/tax_codes/{id}:
              get:
                description: >-
                  <p>Retrieves the details of an existing tax code. Supply the
                  unique tax code ID and Stripe will return the corresponding
                  tax code information.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
                  - Tax_codes
            /v1/tax_rates:
              get:
                description: >-
                  <p>Returns a list of your tax rates. Tax rates are returned
                  sorted by creation date, with the most recently created tax
                  rates appearing first.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
                  - Tax_codes
                  - Tax_rates
              post:
                description: <p>Creates a new tax rate.</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
                  - Tax_codes
                  - Tax_rates
            /v1/tax_rates/{tax_rate}:
              get:
                description: <p>Retrieves a tax rate with the given ID</p>
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
                  - Tax_codes
                  - Tax_rates
                  - Tax_rate
              post:
                description: <p>Updates an existing tax
                tags:
                  - V1
                  - Tax
                  - Calculations
                  - Calculation
                  - Line_items
                  - Registrations
                  - Id
                  - Settings
                  - Transactions
                  - Create_from_calculation
                  - Create_reversal
                  - Transaction
                  - Tax_codes
                  - Tax_rates
                  - Tax_ra
    overlays:
      - type: APIs.io Search
        url: overlays/tax-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/tax-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---