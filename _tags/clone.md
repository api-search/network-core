---
name: Clone
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/clone.png
url: https://example.com/apis/clone.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Clone
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
  - name: codecatalyst
    description: >-
      <p>Welcome to the Amazon CodeCatalyst API reference. This reference
      provides descriptions of operations and data types for Amazon
      CodeCatalyst. You can use the Amazon CodeCatalyst API to work with the
      following objects. </p> <p>Spaces, by calling the following:</p> <ul> <li>
      <p> <a>DeleteSpace</a>, which deletes a space.</p> </li> <li> <p>
      <a>GetSpace</a>, which returns information about a space.</p> </li> <li>
      <p> <a>GetSubscription</a>, which returns information about the Amazon Web
      Services account used for billing purposes and the billing plan for the
      space.</p> </li> <li> <p> <a>ListSpaces</a>, which retrieves a list of
      spaces.</p> </li> <li> <p> <a>UpdateSpace</a>, which changes one or more
      values for a space.</p> </li> </ul> <p>Projects, by calling the
      following:</p> <ul> <li> <p> <a>CreateProject</a> which creates a project
      in a specified space.</p> </li> <li> <p> <a>GetProject</a>, which returns
      information about a project.</p> </li> <li> <p> <a>ListProjects</a>, which
      retrieves a list of projects in a space.</p> </li> </ul> <p>Users, by
      calling the following:</p> <ul> <li> <p> <a>GetUserDetails</a>, which
      returns information about a user in Amazon CodeCatalyst.</p> </li> </ul>
      <p>Source repositories, by calling the following:</p> <ul> <li> <p>
      <a>CreateSourceRepository</a>, which creates an empty Git-based source
      repository in a specified project.</p> </li> <li> <p>
      <a>CreateSourceRepositoryBranch</a>, which creates a branch in a specified
      repository where you can work on code.</p> </li> <li> <p>
      <a>DeleteSourceRepository</a>, which deletes a source repository.</p>
      </li> <li> <p> <a>GetSourceRepository</a>, which returns information about
      a source repository.</p> </li> <li> <p>
      <a>GetSourceRepositoryCloneUrls</a>, which returns information about the
      URLs that can be used with a Git client to clone a source repository.</p>
      </li> <li> <p> <a>ListSourceRepositories</a>, which retrieves a list of
      source repositories in a project.</p> </li> <li> <p>
      <a>ListSourceRepositoryBranches</a>, which retrieves a list of branches in
      a source repository.</p> </li> </ul> <p>Dev Environments and the Amazon
      Web Services Toolkits, by calling the following:</p> <ul> <li> <p>
      <a>CreateDevEnvironment</a>, which creates a Dev Environment, where you
      can quickly work on the code stored in the source repositories of your
      project.</p> </li> <li> <p> <a>DeleteDevEnvironment</a>, which deletes a
      Dev Environment.</p> </li> <li> <p> <a>GetDevEnvironment</a>, which
      returns information about a Dev Environment.</p> </li> <li> <p>
      <a>ListDevEnvironments</a>, which retrieves a list of Dev Environments in
      a project.</p> </li> <li> <p> <a>ListDevEnvironmentSessions</a>, which
      retrieves a list of active Dev Environment sessions in a project.</p>
      </li> <li> <p> <a>StartDevEnvironment</a>, which starts a specified Dev
      Environment and puts it into an active state.</p> </li> <li> <p>
      <a>StartDevEnvironmentSession</a>, which starts a session to a specified
      Dev Environment.</p> </li> <li> <p> <a>StopDevEnvironment</a>, which stops
      a specified Dev Environment and puts it into an stopped state.</p> </li>
      <li> <p> <a>StopDevEnvironmentSession</a>, which stops a session for a
      specified Dev Environment.</p> </li> <li> <p> <a>UpdateDevEnvironment</a>,
      which changes one or more values for a Dev Environment.</p> </li> </ul>
      <p>Workflows, by calling the following:</p> <ul> <li> <p>
      <a>GetWorkflow</a>, which returns information about a workflow.</p> </li>
      <li> <p> <a>GetWorkflowRun</a>, which returns information about a
      specified run of a workflow.</p> </li> <li> <p> <a>ListWorkflowRuns</a>,
      which retrieves a list of runs of a specified workflow.</p> </li> <li> <p>
      <a>ListWorkflows</a>, which retrieves a list of workflows in a specified
      project.</p> </li> <li> <p> <a>StartWorkflowRun</a>, which starts a run of
      a specified workflow.</p> </li> </ul> <p>Security, activity, and resource
      management in Amazon CodeCatalyst, by calling the following:</p> <ul> <li>
      <p> <a>CreateAccessToken</a>, which creates a personal access token (PAT)
      for the current user.</p> </li> <li> <p> <a>DeleteAccessToken</a>, which
      deletes a specified personal access token (PAT).</p> </li> <li> <p>
      <a>ListAccessTokens</a>, which lists all personal access tokens (PATs)
      associated with a user.</p> </li> <li> <p> <a>ListEventLogs</a>, which
      retrieves a list of events that occurred during a specified time period in
      a space.</p> </li> <li> <p> <a>VerifySession</a>, which verifies whether
      the calling user has a valid Amazon CodeCatalyst login and session.</p>
      </li> </ul> <note> <p>If you are using the Amazon CodeCatalyst APIs with
      an SDK or the CLI, you must configure your computer to work with Amazon
      CodeCatalyst and single sign-on (SSO). For more information, see <a
      href="https://docs.aws.amazon.com/codecatalyst/latest/userguide/set-up-cli.html">Setting
      up to use the CLI with Amazon CodeCatalyst</a> and the SSO documentation
      for your SDK.</p> </note>
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
            title: codecatalyst
          paths:
            /v1/accessTokens:
              POST:
                summary: ListAccessTokens
                description: >-
                  <p>Lists all personal access tokens (PATs) associated with the
                  user who calls the API. You can only list PATs associated with
                  your Amazon Web Services Builder ID.</p>
                tags:
                  - Lists
                  - Access
                  - Tokens
                  - Tokens
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments:
              PUT:
                summary: CreateDevEnvironment
                description: >-
                  <p>Creates a Dev Environment in Amazon CodeCatalyst, a
                  cloud-based development environment that you can use to
                  quickly work on the code stored in the source repositories of
                  your project. </p> <note> <p>When created in the Amazon
                  CodeCatalyst console, by default a Dev Environment is
                  configured to have a 2 core processor, 4GB of RAM, and 16GB of
                  persistent storage. None of these defaults apply to a Dev
                  Environment created programmatically.</p> </note>
                tags:
                  - Create
                  - Dev
                  - Environments
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
            /v1/spaces/{spaceName}/projects:
              POST:
                summary: ListProjects
                description: <p>Retrieves a list of projects.</p>
                tags:
                  - Lists
                  - Projects
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
            /v1/spaces/{spaceName}/projects/{projectName}/sourceRepositories/{name}:
              GET:
                summary: GetSourceRepository
                description: <p>Returns information about a source repository.</p>
                tags:
                  - Get
                  - Source
                  - Repositories
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
            /v1/spaces/{spaceName}/projects/{projectName}/sourceRepositories/{sourceRepositoryName}/branches/{name}:
              PUT:
                summary: CreateSourceRepositoryBranch
                description: >-
                  <p>Creates a branch in a specified source repository in Amazon
                  CodeCatalyst. </p> <note> <p>This API only creates a branch in
                  a source repository hosted in Amazon CodeCatalyst. You cannot
                  use this API to create a branch in a linked repository.</p>
                  </note>
                tags:
                  - Create
                  - Source
                  - Repositories
                  - Branch
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
            /v1/accessTokens/{id}:
              DELETE:
                summary: DeleteAccessToken
                description: >-
                  <p>Deletes a specified personal access token (PAT). A personal
                  access token can only be deleted by the user who created
                  it.</p>
                tags:
                  - Delete
                  - Access
                  - Tokens
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments/{id}:
              PATCH:
                summary: UpdateDevEnvironment
                description: >-
                  <p>Changes one or more values for a Dev Environment. Updating
                  certain values of the Dev Environment will cause a
                  restart.</p>
                tags:
                  - Update
                  - Dev
                  - Environments
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
            /v1/spaces/{spaceName}/projects/{name}:
              PATCH:
                summary: UpdateProject
                description: <p>Changes one or more values for a project.</p>
                tags:
                  - Update
                  - Projects
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
            /v1/spaces/{name}:
              PATCH:
                summary: UpdateSpace
                description: <p>Changes one or more values for a space.</p>
                tags:
                  - Update
                  - Space
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
            /v1/spaces/{spaceName}/projects/{projectName}/sourceRepositories/{sourceRepositoryName}/cloneUrls:
              GET:
                summary: GetSourceRepositoryCloneUrls
                description: >-
                  <p>Returns information about the URLs that can be used with a
                  Git client to clone a source repository.</p>
                tags:
                  - Get
                  - Source
                  - Repositories
                  - Clone
                  - URL
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
            /v1/spaces/{spaceName}/subscription:
              GET:
                summary: GetSubscription
                description: >-
                  <p>Returns information about the Amazon Web Services account
                  used for billing purposes and the billing plan for the
                  space.</p>
                tags:
                  - Get
                  - Subscriptions
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
            /userDetails:
              GET:
                summary: GetUserDetails
                description: <p>Returns information about a user. </p>
                tags:
                  - Get
                  - Users
                  - Details
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
            /v1/spaces/{spaceName}/projects/{projectName}/workflows/{id}:
              GET:
                summary: GetWorkflow
                description: <p>Returns information about a workflow.</p>
                tags:
                  - Get
                  - Workflows
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
            /v1/spaces/{spaceName}/projects/{projectName}/workflowRuns/{id}:
              GET:
                summary: GetWorkflowRun
                description: >-
                  <p>Returns information about a specified run of a
                  workflow.</p>
                tags:
                  - Get
                  - Workflows
                  - Runs
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments/{devEnvironmentId}/sessions:
              POST:
                summary: ListDevEnvironmentSessions
                description: >-
                  <p>Retrieves a list of active sessions for a Dev Environment
                  in a project.</p>
                tags:
                  - Lists
                  - Dev
                  - Environments
                  - Sessions
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
            /v1/spaces/{spaceName}/devEnvironments:
              POST:
                summary: ListDevEnvironments
                description: <p>Retrieves a list of Dev Environments in a project.</p>
                tags:
                  - Lists
                  - Dev
                  - Environments
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
            /v1/spaces/{spaceName}/eventLogs:
              POST:
                summary: ListEventLogs
                description: >-
                  <p>Retrieves a list of events that occurred during a specific
                  time in a space. You can use these events to audit user and
                  system activity in a space. For more information, see <a
                  href="https://docs.aws.amazon.com/codecatalyst/latest/userguide/ipa-monitoring.html">Monitoring</a>
                  in the <i>Amazon CodeCatalyst User Guide</i>.</p> <note>
                  <p>ListEventLogs guarantees events for the last 30 days in a
                  given space. You can also view and retrieve a list of
                  management events over the last 90 days for Amazon
                  CodeCatalyst in the CloudTrail console by viewing Event
                  history, or by creating a trail to create and maintain a
                  record of events that extends past 90 days. For more
                  information, see <a
                  href="https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events.html">Working
                  with CloudTrail Event History</a> and <a
                  href="https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-getting-started.html">Working
                  with CloudTrail trails</a>.</p> </note>
                tags:
                  - Lists
                  - Events
                  - Logs
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
            /v1/spaces/{spaceName}/projects/{projectName}/sourceRepositories:
              POST:
                summary: ListSourceRepositories
                description: <p>Retrieves a list of source repositories in a project.</p>
                tags:
                  - Lists
                  - Source
                  - Repositories
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
            /v1/spaces/{spaceName}/projects/{projectName}/sourceRepositories/{sourceRepositoryName}/branches:
              POST:
                summary: ListSourceRepositoryBranches
                description: >-
                  <p>Retrieves a list of branches in a specified source
                  repository.</p>
                tags:
                  - Lists
                  - Source
                  - Repositories
                  - Branches
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
            /v1/spaces:
              POST:
                summary: ListSpaces
                description: <p>Retrieves a list of spaces.</p>
                tags:
                  - Lists
                  - Spaces
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
            /v1/spaces/{spaceName}/projects/{projectName}/workflowRuns:
              PUT:
                summary: StartWorkflowRun
                description: <p>Begins a run of a specified workflow.</p>
                tags:
                  - Start
                  - Workflows
                  - Runs
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
            /v1/spaces/{spaceName}/projects/{projectName}/workflows:
              POST:
                summary: ListWorkflows
                description: <p>Retrieves a list of workflows in a specified project.</p>
                tags:
                  - Lists
                  - Workflows
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments/{id}/start:
              PUT:
                summary: StartDevEnvironment
                description: >-
                  <p>Starts a specified Dev Environment and puts it into an
                  active state. </p>
                tags:
                  - Start
                  - Dev
                  - Environments
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
                  - Start
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments/{id}/session:
              PUT:
                summary: StartDevEnvironmentSession
                description: <p>Starts a session for a specified Dev Environment.</p>
                tags:
                  - Start
                  - Dev
                  - Environments
                  - Sessions
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
                  - Start
                  - Sessions
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments/{id}/stop:
              PUT:
                summary: StopDevEnvironment
                description: >-
                  <p>Pauses a specified Dev Environment and places it in a
                  non-running state. Stopped Dev Environments do not consume
                  compute minutes.</p>
                tags:
                  - Stop
                  - Dev
                  - Environments
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
                  - Start
                  - Sessions
                  - Stop
            /v1/spaces/{spaceName}/projects/{projectName}/devEnvironments/{id}/session/{sessionId}:
              DELETE:
                summary: StopDevEnvironmentSession
                description: <p>Stops a session for a specified Dev Environment.</p>
                tags:
                  - Stop
                  - Dev
                  - Environments
                  - Sessions
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
                  - Start
                  - Sessions
                  - Stop
            /session:
              GET:
                summary: VerifySession
                description: >-
                  <p>Verifies whether the calling user has a valid Amazon
                  CodeCatalyst login and session. If successful, this returns
                  the ID of the user in Amazon CodeCat
                tags:
                  - Verify
                  - Sessions
                  - Tokens
                  - Names
                  - Projects
                  - Projects
                  - Dev
                  - Environments
                  - Source
                  - Repositories
                  - Repositories
                  - Branches
                  - Identifiers
                  - V1
                  - Spaces
                  - Clone
                  - URL
                  - Subscriptions
                  - Details
                  - Workflows
                  - Workflows
                  - Runs
                  - Environments
                  - Sessions
                  - Events
                  - Logs
                  - Start
                  - Sessions
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/codecatalyst-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codecatalyst-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codecatalyst
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---