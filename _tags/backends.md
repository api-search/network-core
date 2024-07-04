---
name: Backends
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/backends.png
url: https://example.com/apis/backends.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Backends
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
  - name: amplify
    description: >-
      <p>Amplify enables developers to develop and deploy cloud-powered mobile
      and web apps. Amplify Hosting provides a continuous delivery and hosting
      service for web applications. For more information, see the <a
      href="https://docs.aws.amazon.com/amplify/latest/userguide/welcome.html">Amplify
      Hosting User Guide</a>. The Amplify Framework is a comprehensive set of
      SDKs, libraries, tools, and documentation for client app development. For
      more information, see the <a href="https://docs.amplify.aws/">Amplify
      Framework.</a> </p>
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
            title: amplify
          paths:
            /apps:
              GET:
                summary: ListApps
                description: <p>Returns a list of the existing Amplify apps. </p>
                tags:
                  - Lists
                  - Applications
                  - Applications
            /apps/{appId}/backendenvironments:
              GET:
                summary: ListBackendEnvironments
                description: <p>Lists the backend environments for an Amplify app. </p>
                tags:
                  - Lists
                  - Backends
                  - Environments
                  - Applications
                  - Identifiers
                  - Backend Environments
            /apps/{appId}/branches:
              GET:
                summary: ListBranches
                description: <p> Lists the branches of an Amplify app. </p>
                tags:
                  - Lists
                  - Branches
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
            /apps/{appId}/branches/{branchName}/deployments:
              POST:
                summary: CreateDeployment
                description: >-
                  <p>Creates a deployment for a manually deployed Amplify app.
                  Manually deployed apps are not connected to a repository. </p>
                  <p>The maximum duration between the
                  <code>CreateDeployment</code> call and the
                  <code>StartDeployment</code> call cannot exceed 8 hours. If
                  the duration exceeds 8 hours, the <code>StartDeployment</code>
                  call and the associated <code>Job</code> will fail.</p>
                tags:
                  - Create
                  - Deployments
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
            /apps/{appId}/domains:
              GET:
                summary: ListDomainAssociations
                description: <p> Returns the domain associations for an Amplify app. </p>
                tags:
                  - Lists
                  - Domains
                  - Associations
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
            /apps/{appId}/webhooks:
              GET:
                summary: ListWebhooks
                description: <p>Returns a list of webhooks for an Amplify app. </p>
                tags:
                  - Lists
                  - Webhooks
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
            /apps/{appId}:
              POST:
                summary: UpdateApp
                description: <p>Updates an existing Amplify app. </p>
                tags:
                  - Update
                  - Applications
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
            /apps/{appId}/backendenvironments/{environmentName}:
              GET:
                summary: GetBackendEnvironment
                description: <p>Returns a backend environment for an Amplify app. </p>
                tags:
                  - Get
                  - Backends
                  - Environments
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
            /apps/{appId}/branches/{branchName}:
              POST:
                summary: UpdateBranch
                description: <p> Updates a branch for an Amplify app. </p>
                tags:
                  - Update
                  - Branch
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
            /apps/{appId}/domains/{domainName}:
              POST:
                summary: UpdateDomainAssociation
                description: <p> Creates a new domain association for an Amplify app.</p>
                tags:
                  - Update
                  - Domains
                  - Association
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
            /apps/{appId}/branches/{branchName}/jobs/{jobId}:
              GET:
                summary: GetJob
                description: <p> Returns a job for a branch of an Amplify app. </p>
                tags:
                  - Get
                  - Jobs
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
            /webhooks/{webhookId}:
              POST:
                summary: UpdateWebhook
                description: <p>Updates a webhook. </p>
                tags:
                  - Update
                  - Webhooks
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
            /apps/{appId}/accesslogs:
              POST:
                summary: GenerateAccessLogs
                description: >-
                  <p>Returns the website access logs for a specific time range
                  using a presigned URL. </p>
                tags:
                  - Generate
                  - Access
                  - Logs
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
            /artifacts/{artifactId}:
              GET:
                summary: GetArtifactUrl
                description: >-
                  <p>Returns the artifact info that corresponds to an artifact
                  id. </p>
                tags:
                  - Get
                  - Artifacts
                  - URL
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
            /apps/{appId}/branches/{branchName}/jobs/{jobId}/artifacts:
              GET:
                summary: ListArtifacts
                description: >-
                  <p>Returns a list of artifacts for a specified app, branch,
                  and job. </p>
                tags:
                  - Lists
                  - Artifacts
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
                  - Artifacts
            /apps/{appId}/branches/{branchName}/jobs:
              POST:
                summary: StartJob
                description: <p> Starts a new job for a branch of an Amplify app. </p>
                tags:
                  - Start
                  - Jobs
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
                  - Artifacts
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Untags a resource with a specified Amazon Resource Name
                  (ARN).</p>
                tags:
                  - Untag
                  - Resources
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
                  - Artifacts
                  - ARN
            /apps/{appId}/branches/{branchName}/deployments/start:
              POST:
                summary: StartDeployment
                description: >-
                  <p>Starts a deployment for a manually deployed app. Manually
                  deployed apps are not connected to a repository. </p> <p>The
                  maximum duration between the <code>CreateDeployment</code>
                  call and the <code>StartDeployment</code> call cannot exceed 8
                  hours. If the duration exceeds 8 hours, the
                  <code>StartDeployment</code> call and the associated
                  <code>Job</code> will fail.</p>
                tags:
                  - Start
                  - Deployments
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
                  - Artifacts
                  - ARN
                  - Start
            /apps/{appId}/branches/{branchName}/jobs/{jobId}/stop:
              DELETE:
                summary: StopJob
                description: <p> Stops a job that is in progress for a branch of an Ampli
                tags:
                  - Stop
                  - Jobs
                  - Applications
                  - Identifiers
                  - Backend Environments
                  - Branches
                  - Branch
                  - Names
                  - Deployments
                  - Domains
                  - Webhooks
                  - Environments
                  - Domains
                  - Jobs
                  - Jobs
                  - Access Logs
                  - Artifacts
                  - ARN
                  - Start
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/amplify-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/amplify-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:amplify
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---