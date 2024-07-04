---
name: Challenges
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/challenges.png
url: https://example.com/apis/challenges.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Challenges
apis:
  - name: amplifybackend
    description: <p>AWS Amplify Admin API</p>
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
            title: amplifybackend
          paths:
            /backend/{appId}/environments/{backendEnvironmentName}/clone:
              POST:
                summary: CloneBackend
                description: <p>This operation clones an existing backend.</p>
                tags:
                  - Clone
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
            /backend:
              POST:
                summary: CreateBackend
                description: >-
                  <p>This operation creates a backend for an Amplify app.
                  Backends are automatically created at the time of app
                  creation.</p>
                tags:
                  - Create
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
            /backend/{appId}/api:
              POST:
                summary: CreateBackendAPI
                description: <p>Creates a new backend API resource.</p>
                tags:
                  - Create
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
            /backend/{appId}/auth:
              POST:
                summary: CreateBackendAuth
                description: <p>Creates a new backend authentication resource.</p>
                tags:
                  - Create
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
            /backend/{appId}/config:
              POST:
                summary: CreateBackendConfig
                description: <p>Creates a config object for a backend.</p>
                tags:
                  - Create
                  - Backends
                  - Configurations
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
            /backend/{appId}/storage:
              POST:
                summary: CreateBackendStorage
                description: <p>Creates a backend storage resource.</p>
                tags:
                  - Create
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
            /backend/{appId}/challenge:
              POST:
                summary: CreateToken
                description: >-
                  <p>Generates a one-time challenge code to authenticate a user
                  into your Amplify Admin UI.</p>
                tags:
                  - Create
                  - Tokens
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
            /backend/{appId}/environments/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackend
                description: >-
                  <p>Removes an existing environment from your Amplify
                  project.</p>
                tags:
                  - Delete
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/api/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackendAPI
                description: <p>Deletes an existing backend API resource.</p>
                tags:
                  - Delete
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/auth/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackendAuth
                description: <p>Deletes an existing backend authentication resource.</p>
                tags:
                  - Delete
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/storage/{backendEnvironmentName}/remove:
              POST:
                summary: DeleteBackendStorage
                description: <p>Removes the specified backend storage resource.</p>
                tags:
                  - Delete
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
            /backend/{appId}/challenge/{sessionId}/remove:
              POST:
                summary: DeleteToken
                description: >-
                  <p>Deletes the challenge token based on the given appId and
                  sessionId.</p>
                tags:
                  - Delete
                  - Tokens
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
            /backend/{appId}/api/{backendEnvironmentName}/generateModels:
              POST:
                summary: GenerateBackendAPIModels
                description: >-
                  <p>Generates a model schema for an existing backend API
                  resource.</p>
                tags:
                  - Generate
                  - Backends
                  - Models
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
            /backend/{appId}/details:
              POST:
                summary: GetBackend
                description: >-
                  <p>Provides project-level details for your Amplify UI
                  project.</p>
                tags:
                  - Get
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
            /backend/{appId}/api/{backendEnvironmentName}/details:
              POST:
                summary: GetBackendAPI
                description: <p>Gets the details for a backend API.</p>
                tags:
                  - Get
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
            /backend/{appId}/api/{backendEnvironmentName}/getModels:
              POST:
                summary: GetBackendAPIModels
                description: >-
                  <p>Gets a model introspection schema for an existing backend
                  API resource.</p>
                tags:
                  - Get
                  - Backends
                  - Models
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
            /backend/{appId}/auth/{backendEnvironmentName}/details:
              POST:
                summary: GetBackendAuth
                description: <p>Gets a backend auth details.</p>
                tags:
                  - Get
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
            /backend/{appId}/job/{backendEnvironmentName}/{jobId}:
              POST:
                summary: UpdateBackendJob
                description: <p>Updates a specific job.</p>
                tags:
                  - Update
                  - Backends
                  - Jobs
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
            /backend/{appId}/storage/{backendEnvironmentName}/details:
              POST:
                summary: GetBackendStorage
                description: <p>Gets details for a backend storage resource.</p>
                tags:
                  - Get
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
            /backend/{appId}/challenge/{sessionId}:
              GET:
                summary: GetToken
                description: >-
                  <p>Gets the challenge token based on the given appId and
                  sessionId.</p>
                tags:
                  - Get
                  - Tokens
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
            /backend/{appId}/auth/{backendEnvironmentName}/import:
              POST:
                summary: ImportBackendAuth
                description: <p>Imports an existing backend authentication resource.</p>
                tags:
                  - Import
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
            /backend/{appId}/storage/{backendEnvironmentName}/import:
              POST:
                summary: ImportBackendStorage
                description: <p>Imports an existing backend storage resource.</p>
                tags:
                  - Import
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
            /backend/{appId}/job/{backendEnvironmentName}:
              POST:
                summary: ListBackendJobs
                description: <p>Lists the jobs for the backend of an Amplify app.</p>
                tags:
                  - Lists
                  - Backends
                  - Jobs
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
            /s3Buckets:
              POST:
                summary: ListS3Buckets
                description: <p>The list of S3 buckets in your account.</p>
                tags:
                  - Lists
                  - S3
                  - Buckets
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/remove:
              POST:
                summary: RemoveAllBackends
                description: >-
                  <p>Removes all backend environments from your Amplify
                  project.</p>
                tags:
                  - Removes
                  - All
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/config/remove:
              POST:
                summary: RemoveBackendConfig
                description: >-
                  <p>Removes the AWS resources required to access the Amplify
                  Admin UI.</p>
                tags:
                  - Removes
                  - Backends
                  - Configurations
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/api/{backendEnvironmentName}:
              POST:
                summary: UpdateBackendAPI
                description: <p>Updates an existing backend API resource.</p>
                tags:
                  - Update
                  - Backends
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/auth/{backendEnvironmentName}:
              POST:
                summary: UpdateBackendAuth
                description: <p>Updates an existing backend authentication resource.</p>
                tags:
                  - Update
                  - Backends
                  - Authentication
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
            /backend/{appId}/config/update:
              POST:
                summary: UpdateBackendConfig
                description: >-
                  <p>Updates the AWS resources required to access the Amplify
                  Admin UI.</p>
                tags:
                  - Update
                  - Backends
                  - Configurations
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
                  - Update
            /backend/{appId}/storage/{backendEnvironmentName}:
              POST:
                summary: UpdateBackendStorage
                description: <p>Updates an existing backend storage res
                tags:
                  - Update
                  - Backends
                  - Storage
                  - Identifiers
                  - Environments
                  - Backends
                  - Environments
                  - Names
                  - Clone
                  - APIs
                  - Authentication
                  - Configurations
                  - Storage
                  - Challenges
                  - Removes
                  - Sessions
                  - Generate
                  - Models
                  - Details
                  - Get
                  - Jobs
                  - Import
                  - Buckets
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/amplifybackend-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/amplifybackend-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:amplifybackend
  - aid: twilio:twilio-verify-api
    name: Twilio Verify API
    description: >-
      Set up SMS or voice verifications to quickly authenticate users, fight
      fraud, and protect user accounts.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/en-us/trusted-activation/verify
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/en-us/trusted-activation/verify
      - type: Pricing
        url: https://www.twilio.com/en-us/verify/pricing
      - type: OpenAPI
        data:
          info:
            title: Twilio - Verify
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v2/Services/{ServiceSid}/AccessTokens:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new enrollment Access Token for the Entity
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
            /v2/Services/{ServiceSid}/AccessTokens/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch an Access Token for the Entity
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
            /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Bucket for a Rate Limit
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
              get:
                description: Retrieve a list of all Buckets for a Rate Limit.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
            /v2/Services/{ServiceSid}/RateLimits/{RateLimitSid}/Buckets/{Sid}:
              description: 'TODO: Resource-level docs'
              post:
                description: Update a specific Bucket.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
              get:
                description: Fetch a specific Bucket.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
              delete:
                description: Delete a specific Bucket.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
            /v2/Services/{ServiceSid}/Entities/{Identity}/Challenges:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Challenge for the Factor
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
              get:
                description: Retrieve a list of all Challenges for a Factor.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
            /v2/Services/{ServiceSid}/Entities/{Identity}/Challenges/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Challenge.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
              post:
                description: Verify a specific Challenge.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
            /v2/Services/{ServiceSid}/Entities:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Entity for the Service
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
              get:
                description: Retrieve a list of all Entities for a Service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
            /v2/Services/{ServiceSid}/Entities/{Identity}:
              description: 'TODO: Resource-level docs'
              delete:
                description: Delete a specific Entity.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
              get:
                description: Fetch a specific Entity.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
            /v2/Services/{ServiceSid}/Entities/{Identity}/Factors/{Sid}:
              description: 'TODO: Resource-level docs'
              delete:
                description: Delete a specific Factor.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
              get:
                description: Fetch a specific Factor.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
              post:
                description: >-
                  Update a specific Factor. This endpoint can be used to Verify
                  a Factor if passed an `AuthPayload` param.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
            /v2/Services/{ServiceSid}/Entities/{Identity}/Factors:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Factors for an Entity.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
              post:
                description: Create a new Factor for the Entity
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
            /v2/Forms/{FormType}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch the forms for a specific Form Type.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
            /v2/Services/{ServiceSid}/MessagingConfigurations:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new MessagingConfiguration for a service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
              get:
                description: Retrieve a list of all Messaging Configurations for a Service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
            /v2/Services/{ServiceSid}/MessagingConfigurations/{Country}:
              description: 'TODO: Resource-level docs'
              post:
                description: Update a specific MessagingConfiguration
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
              get:
                description: Fetch a specific MessagingConfiguration.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
              delete:
                description: Delete a specific MessagingConfiguration.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
            /v2/Services/{ServiceSid}/Entities/{Identity}/Challenges/{ChallengeSid}/Notifications:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Notification for the corresponding Challenge
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
            /v2/Services/{ServiceSid}/RateLimits:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Rate Limit for a Service
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
              get:
                description: Retrieve a list of all Rate Limits for a service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
            /v2/Services/{ServiceSid}/RateLimits/{Sid}:
              description: 'TODO: Resource-level docs'
              post:
                description: Update a specific Rate Limit.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
              get:
                description: Fetch a specific Rate Limit.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
              delete:
                description: Delete a specific Rate Limit.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
            /v2/SafeList/Numbers:
              description: 'TODO: Resource-level docs'
              post:
                description: Add a new phone number to SafeList.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
            /v2/SafeList/Numbers/{PhoneNumber}:
              description: 'TODO: Resource-level docs'
              get:
                description: Check if a phone number exists in SafeList.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
              delete:
                description: Remove a phone number from SafeList.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
            /v2/Services:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Verification Service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
              get:
                description: Retrieve a list of all Verification Services for an account.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
            /v2/Services/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Verification Service Instance.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
              delete:
                description: Delete a specific Verification Service Instance.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
              post:
                description: Update a specific Verification Service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
            /v2/Services/{ServiceSid}/Verifications:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Verification using a Service
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
            /v2/Services/{ServiceSid}/Verifications/{Sid}:
              description: 'TODO: Resource-level docs'
              post:
                description: Update a Verification status
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
              get:
                description: Fetch a specific Verification
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
            /v2/Attempts:
              description: 'TODO: Resource-level docs'
              get:
                description: List all the verification attempts for a given Account.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
            /v2/Attempts/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific verification attempt.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
            /v2/Attempts/Summary:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Get a summary of how many attempts were made and how many were
                  converted.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
            /v2/Services/{ServiceSid}/VerificationCheck:
              description: 'TODO: Resource-level docs'
              post:
                description: challenge a specific Verification Check.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
            /v2/Templates:
              description: 'TODO: Resource-level docs'
              get:
                description: List all the available templates for a given Account.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
                  - Templates
            /v2/Services/{ServiceSid}/Webhooks:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Webhook for the Service
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
                  - Templates
                  - Webhooks
              get:
                description: Retrieve a list of all Webhooks for a Service.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
                  - Templates
                  - Webhooks
            /v2/Services/{ServiceSid}/Webhooks/{Sid}:
              description: 'TODO: Resource-level docs'
              post:
                description: ''
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
                  - Templates
                  - Webhooks
              delete:
                description: Delete a specific Webhook.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
                  - Templates
                  - Webhooks
              get:
                description: Fetch a specific Webhook.
                tags:
                  - Services
                  - Service
                  - Sid
                  - Access
                  - Tokens
                  - Rate
                  - Limits
                  - Limit
                  - Buckets
                  - Entities
                  - Identity
                  - Challenges
                  - Factors
                  - Forms
                  - Form
                  - Type
                  - Messaging
                  - Configurations
                  - Country
                  - Challenge
                  - Notifications
                  - Safe
                  - List
                  - Numbers
                  - Phone
                  - Number
                  - Verifications
                  - Attempts
                  - Summary
                  - Verification
                  - Check
                  - Templates
                  - Webhooks
          tags:
            - name: VerifyV2AccessToken
            - name: VerifyV2Bucket
            - name: VerifyV2Challenge
            - name: VerifyV2Entity
            - name: VerifyV2Factor
            - name: VerifyV2Form
            - name: VerifyV2MessagingConfiguration
            - name: VerifyV2NewFactor
            - name: VerifyV2Notification
            - name: VerifyV2RateLimit
            - name: VerifyV2Safelist
            - name: VerifyV2Service
            - name: VerifyV2Template
            - name: VerifyV2Verification
            - name: VerifyV2VerificationAttempt
            - name: VerifyV2VerificationAttemptsSummary
            - name: VerifyV2VerificationCheck
            - name: VerifyV2Webhook
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/verify-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/verify-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---