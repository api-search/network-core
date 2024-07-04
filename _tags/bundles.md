---
name: Bundles
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/bundles.png
url: https://example.com/apis/bundles.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Bundles
apis:
  - name: appfabric
    description: >-
      <p>Amazon Web Services AppFabric quickly connects software as a service
      (SaaS) applications across your organization. This allows IT and security
      teams to easily manage and secure applications using a standard schema,
      and employees can complete everyday tasks faster using generative
      artificial intelligence (AI). You can use these APIs to complete AppFabric
      tasks, such as setting up audit log ingestions or viewing user access. For
      more information about AppFabric, including the required permissions to
      use the service, see the <a
      href="https://docs.aws.amazon.com/appfabric/latest/adminguide/">Amazon Web
      Services AppFabric Administration Guide</a>. For more information about
      using the Command Line Interface (CLI) to manage your AppFabric resources,
      see the <a
      href="https://docs.aws.amazon.com/cli/latest/reference/appfabric/index.html">AppFabric
      section of the CLI Reference</a>.</p>
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
            title: appfabric
          paths:
            /useraccess/batchget:
              POST:
                summary: BatchGetUserAccessTasks
                description: >-
                  <p>Gets user access details in a batch request.</p> <p>This
                  action polls data from the tasks that are kicked off by the
                  <code>StartUserAccessTasks</code> action.</p>
                tags:
                  - Batches
                  - Get
                  - Users
                  - Access
                  - Tasks
                  - User Access
                  - Batches
            /appbundles/{appBundleIdentifier}/appauthorizations/{appAuthorizationIdentifier}/connect:
              POST:
                summary: ConnectAppAuthorization
                description: >-
                  <p>Establishes a connection between Amazon Web Services
                  AppFabric and an application, which allows AppFabric to call
                  the APIs of the application.</p>
                tags:
                  - Connect
                  - Applications
                  - Authorization
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
            /appbundles/{appBundleIdentifier}/appauthorizations:
              GET:
                summary: ListAppAuthorizations
                description: >-
                  <p>Returns a list of all app authorizations configured for an
                  app bundle.</p>
                tags:
                  - Lists
                  - Applications
                  - Authorization
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
            /appbundles:
              GET:
                summary: ListAppBundles
                description: <p>Returns a list of app bundles.</p>
                tags:
                  - Lists
                  - Applications
                  - Bundles
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
            /appbundles/{appBundleIdentifier}/ingestions:
              GET:
                summary: ListIngestions
                description: >-
                  <p>Returns a list of all ingestions configured for an app
                  bundle.</p>
                tags:
                  - Lists
                  - Ingestions
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
            /appbundles/{appBundleIdentifier}/ingestions/{ingestionIdentifier}/ingestiondestinations:
              GET:
                summary: ListIngestionDestinations
                description: >-
                  <p>Returns a list of all ingestion destinations configured for
                  an ingestion.</p>
                tags:
                  - Lists
                  - Ingestion
                  - Destinations
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
            /appbundles/{appBundleIdentifier}/appauthorizations/{appAuthorizationIdentifier}:
              PATCH:
                summary: UpdateAppAuthorization
                description: >-
                  <p>Updates an app authorization within an app bundle, which
                  allows AppFabric to connect to an application.</p> <p>If the
                  app authorization was in a <code>connected</code> state,
                  updating the app authorization will set it back to a
                  <code>PendingConnect</code> state.</p>
                tags:
                  - Update
                  - Applications
                  - Authorization
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
            /appbundles/{appBundleIdentifier}:
              GET:
                summary: GetAppBundle
                description: <p>Returns information about an app bundle.</p>
                tags:
                  - Get
                  - Applications
                  - Bundles
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
            /appbundles/{appBundleIdentifier}/ingestions/{ingestionIdentifier}:
              GET:
                summary: GetIngestion
                description: <p>Returns information about an ingestion.</p>
                tags:
                  - Get
                  - Ingestion
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
            /appbundles/{appBundleIdentifier}/ingestions/{ingestionIdentifier}/ingestiondestinations/{ingestionDestinationIdentifier}:
              PATCH:
                summary: UpdateIngestionDestination
                description: >-
                  <p>Updates an ingestion destination, which specifies how an
                  application's ingested data is processed by Amazon Web
                  Services AppFabric and where it's delivered.</p>
                tags:
                  - Update
                  - Ingestion
                  - Destinations
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
                  - Destinations
            /tags/{resourceArn}:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag or tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
                  - Destinations
                  - ARN
            /appbundles/{appBundleIdentifier}/ingestions/{ingestionIdentifier}/start:
              POST:
                summary: StartIngestion
                description: >-
                  <p>Starts (enables) an ingestion, which collects data from an
                  application.</p>
                tags:
                  - Start
                  - Ingestion
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
                  - Destinations
                  - ARN
                  - Start
            /useraccess/start:
              POST:
                summary: StartUserAccessTasks
                description: >-
                  <p>Starts the tasks to search user access status for a
                  specific email address.</p> <p>The tasks are stopped when the
                  user access status data is found. The tasks are terminated
                  when the API calls to the application time out.</p>
                tags:
                  - Start
                  - Users
                  - Access
                  - Tasks
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
                  - Destinations
                  - ARN
                  - Start
            /appbundles/{appBundleIdentifier}/ingestions/{ingestionIdentifier}/stop:
              POST:
                summary: StopIngestion
                description: <p>Stops (disables) an inge
                tags:
                  - Stop
                  - Ingestion
                  - User Access
                  - Batches
                  - Bundles
                  - Identifiers
                  - Application Authorizations
                  - Applications
                  - Authorization
                  - Connect
                  - Application Bundles
                  - Ingestions
                  - Ingestion
                  - Ingestion Destinations
                  - Destinations
                  - ARN
                  - Start
                  - St
    overlays:
      - type: APIs.io Search
        url: overlays/appfabric-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appfabric-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appfabric
  - name: mobile
    description: >-
      <p> AWS Mobile Service provides mobile app and website developers with
      capabilities required to configure AWS resources and bootstrap their
      developer desktop projects with the necessary SDKs, constants, tools and
      samples to make use of those resources. </p>
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
            title: mobile
          paths:
            /projects:
              GET:
                summary: ListProjects
                description: <p> Lists projects in AWS Mobile Hub. </p>
                tags:
                  - Lists
                  - Projects
                  - Projects
            /projects/{projectId}:
              DELETE:
                summary: DeleteProject
                description: <p> Delets a project in AWS Mobile Hub. </p>
                tags:
                  - Delete
                  - Projects
                  - Projects
                  - Identifiers
            /bundles/{bundleId}:
              POST:
                summary: ExportBundle
                description: >-
                  <p> Generates customized software development kit (SDK) and or
                  tool packages used to integrate mobile web or mobile app
                  clients with backend AWS resources. </p>
                tags:
                  - Export
                  - Bundles
                  - Projects
                  - Identifiers
            /project:
              GET:
                summary: DescribeProject
                description: <p> Gets details about a project in AWS Mobile Hub. </p>
                tags:
                  - Describe
                  - Projects
                  - Projects
                  - Identifiers
                  - Projects
            /exports/{projectId}:
              POST:
                summary: ExportProject
                description: >-
                  <p> Exports project configuration to a snapshot which can be
                  downloaded and shared. Note that mobile app push credentials
                  are encrypted in exported projects, so they can only be shared
                  successfully within the same AWS account. </p>
                tags:
                  - Export
                  - Projects
                  - Projects
                  - Identifiers
                  - Projects
            /bundles:
              GET:
                summary: ListBundles
                description: <p> List all available bundles. </p>
                tags:
                  - Lists
                  - Bundles
                  - Projects
                  - Identifiers
                  - Projects
                  - Bundles
            /update:
              POST:
                summary: UpdateProject
                description: <p> Update an existing pr
                tags:
                  - Update
                  - Projects
                  - Projects
                  - Identifiers
                  - Projects
                  - Bundles
                  - Upda
    overlays:
      - type: APIs.io Search
        url: overlays/mobile-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mobile-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mobile
  - name: quicksight
    description: >-
      <fullname>Amazon QuickSight API Reference</fullname> <p>Amazon QuickSight
      is a fully managed, serverless business intelligence service for the
      Amazon Web Services Cloud that makes it easy to extend data and insights
      to every user in your organization. This API reference contains
      documentation for a programming interface that you can use to manage
      Amazon QuickSight. </p>
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
            title: quicksight
          paths:
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/ingestions/{IngestionId}:
              GET:
                summary: DescribeIngestion
                description: <p>Describes a SPICE ingestion.</p>
                tags:
                  - Describe
                  - Ingestion
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
            /accounts/{AwsAccountId}/customizations:
              PUT:
                summary: UpdateAccountCustomization
                description: >-
                  <p>Updates Amazon QuickSight customizations for the current
                  Amazon Web Services Region. Currently, the only customization
                  that you can use is a theme.</p> <p>You can use customizations
                  for your Amazon Web Services account or, if you specify a
                  namespace, for a Amazon QuickSight namespace instead.
                  Customizations that apply to a namespace override
                  customizations that apply to an Amazon Web Services account.
                  To find out which customizations apply, use the
                  <code>DescribeAccountCustomization</code> API operation. </p>
                tags:
                  - Update
                  - Account
                  - Customizations
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
            /account/{AwsAccountId}:
              GET:
                summary: DescribeAccountSubscription
                description: >-
                  <p>Use the DescribeAccountSubscription operation to receive a
                  description of an Amazon QuickSight account's subscription. A
                  successful API call returns an <code>AccountInfo</code> object
                  that includes an account's name, subscription status,
                  authentication type, edition, and notification email
                  address.</p>
                tags:
                  - Describe
                  - Account
                  - Subscriptions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
            /accounts/{AwsAccountId}/analyses/{AnalysisId}:
              PUT:
                summary: UpdateAnalysis
                description: <p>Updates an analysis in Amazon QuickSight</p>
                tags:
                  - Update
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
            /accounts/{AwsAccountId}/dashboards/{DashboardId}:
              PUT:
                summary: UpdateDashboard
                description: >-
                  <p>Updates a dashboard in an Amazon Web Services account.</p>
                  <note> <p>Updating a Dashboard creates a new dashboard version
                  but does not immediately publish the new version. You can
                  update the published version of a dashboard by using the
                  <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_UpdateDashboardPublishedVersion.html">UpdateDashboardPublishedVersion</a>
                  </code> API operation.</p> </note>
                tags:
                  - Update
                  - Dashboard
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
            /accounts/{AwsAccountId}/data-sets:
              GET:
                summary: ListDataSets
                description: >-
                  <p>Lists all of the datasets belonging to the current Amazon
                  Web Services account in an Amazon Web Services Region.</p>
                  <p>The permissions resource is
                  <code>arn:aws:quicksight:region:aws-account-id:dataset/*</code>.</p>
                tags:
                  - Lists
                  - Data
                  - Sets
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
            /accounts/{AwsAccountId}/data-sources:
              GET:
                summary: ListDataSources
                description: >-
                  <p>Lists data sources in current Amazon Web Services Region
                  that belong to this Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Data
                  - Sources
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
            /accounts/{AwsAccountId}/folders/{FolderId}:
              PUT:
                summary: UpdateFolder
                description: <p>Updates the name of a folder.</p>
                tags:
                  - Update
                  - Folder
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
            /accounts/{AwsAccountId}/folders/{FolderId}/members/{MemberType}/{MemberId}:
              DELETE:
                summary: DeleteFolderMembership
                description: >-
                  <p>Removes an asset, such as a dashboard, analysis, or
                  dataset, from a folder.</p>
                tags:
                  - Delete
                  - Folder
                  - Membership
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups:
              GET:
                summary: ListGroups
                description: <p>Lists all user groups in Amazon QuickSight. </p>
                tags:
                  - Lists
                  - Groups
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups/{GroupName}/members/{MemberName}:
              GET:
                summary: DescribeGroupMembership
                description: >-
                  <p>Use the <code>DescribeGroupMembership</code> operation to
                  determine if a user is a member of the specified group. If the
                  user exists and is a member of the specified group, an
                  associated <code>GroupMember</code> object is returned.</p>
                tags:
                  - Describe
                  - Group
                  - Membership
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
            /accounts/{AwsAccountId}/namespaces/{Namespace}/iam-policy-assignments/:
              POST:
                summary: CreateIAMPolicyAssignment
                description: >-
                  <p>Creates an assignment with one specified IAM policy,
                  identified by its Amazon Resource Name (ARN). This policy
                  assignment is attached to the specified groups or users of
                  Amazon QuickSight. Assignment names are unique per Amazon Web
                  Services account. To avoid overwriting rules in other
                  namespaces, use assignment names that are unique.</p>
                tags:
                  - Create
                  - Policies
                  - Assignment
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
            /accounts/{AwsAccountId}:
              POST:
                summary: CreateNamespace
                description: >-
                  <p>(Enterprise edition only) Creates a new namespace for you
                  to use with Amazon QuickSight.</p> <p>A namespace allows you
                  to isolate the Amazon QuickSight users and groups that are
                  registered for that namespace. Users that access the namespace
                  can share assets only with other users or groups in the same
                  namespace. They can't see users and groups in other
                  namespaces. You can create a namespace after your Amazon Web
                  Services account is subscribed to Amazon QuickSight. The
                  namespace must be unique within the Amazon Web Services
                  account. By default, there is a limit of 100 namespaces per
                  Amazon Web Services account. To increase your limit, create a
                  ticket with Amazon Web Services Support. </p>
                tags:
                  - Create
                  - Namespaces
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/refresh-schedules:
              PUT:
                summary: UpdateRefreshSchedule
                description: <p>Updates a refresh schedule for a dataset.</p>
                tags:
                  - Update
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
            /accounts/{AwsAccountId}/namespaces/{Namespace}/roles/{Role}/members/{MemberName}:
              DELETE:
                summary: DeleteRoleMembership
                description: <p>Removes a group from a role.</p>
                tags:
                  - Delete
                  - Roles
                  - Membership
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
            /accounts/{AwsAccountId}/templates/{TemplateId}:
              PUT:
                summary: UpdateTemplate
                description: >-
                  <p>Updates a template from an existing Amazon QuickSight
                  analysis or another template.</p>
                tags:
                  - Update
                  - Templates
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
            /accounts/{AwsAccountId}/templates/{TemplateId}/aliases/{AliasName}:
              PUT:
                summary: UpdateTemplateAlias
                description: <p>Updates the template alias of a template.</p>
                tags:
                  - Update
                  - Templates
                  - Alias
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
            /accounts/{AwsAccountId}/themes/{ThemeId}:
              PUT:
                summary: UpdateTheme
                description: <p>Updates a theme.</p>
                tags:
                  - Update
                  - Theme
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
            /accounts/{AwsAccountId}/themes/{ThemeId}/aliases/{AliasName}:
              PUT:
                summary: UpdateThemeAlias
                description: <p>Updates an alias of a theme.</p>
                tags:
                  - Update
                  - Theme
                  - Alias
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
            /accounts/{AwsAccountId}/topics:
              GET:
                summary: ListTopics
                description: <p>Lists all of the topics within an account.</p>
                tags:
                  - Lists
                  - Topics
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
            /accounts/{AwsAccountId}/topics/{TopicId}/schedules:
              GET:
                summary: ListTopicRefreshSchedules
                description: <p>Lists all of the refresh schedules for a topic.</p>
                tags:
                  - Lists
                  - Topics
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
            /accounts/{AwsAccountId}/vpc-connections:
              GET:
                summary: ListVPCConnections
                description: >-
                  <p>Lists all of the VPC connections in the current set Amazon
                  Web Services Region of an Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Connections
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
            /accounts/{AwsAccountId}/data-sets/{DataSetId}:
              PUT:
                summary: UpdateDataSet
                description: >-
                  <p>Updates a dataset. This operation doesn't support datasets
                  that include uploaded files as a source. Partial updates are
                  not supported by this operation.</p>
                tags:
                  - Update
                  - Data
                  - Sets
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/refresh-properties:
              PUT:
                summary: PutDataSetRefreshProperties
                description: >-
                  <p>Creates or updates the dataset refresh properties for the
                  dataset.</p>
                tags:
                  - Put
                  - Data
                  - Sets
                  - Refresh
                  - Properties
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
            /accounts/{AwsAccountId}/data-sources/{DataSourceId}:
              PUT:
                summary: UpdateDataSource
                description: <p>Updates a data source.</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups/{GroupName}:
              PUT:
                summary: UpdateGroup
                description: <p>Changes a group description. </p>
                tags:
                  - Update
                  - Group
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
            /accounts/{AwsAccountId}/namespace/{Namespace}/iam-policy-assignments/{AssignmentName}:
              DELETE:
                summary: DeleteIAMPolicyAssignment
                description: <p>Deletes an existing IAM policy assignment.</p>
                tags:
                  - Delete
                  - Policies
                  - Assignment
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
            /accounts/{AwsAccountId}/identity-propagation-config/{Service}:
              POST:
                summary: UpdateIdentityPropagationConfig
                description: >-
                  <p>Adds or updates services and authorized targets to
                  configure what the Amazon QuickSight IAM Identity Center
                  application can access.</p> <p>This operation is only
                  supported for Amazon QuickSight accounts using IAM Identity
                  Center</p>
                tags:
                  - Update
                  - Identity
                  - Propagation
                  - Configurations
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
            /accounts/{AwsAccountId}/namespaces/{Namespace}:
              GET:
                summary: DescribeNamespace
                description: <p>Describes the current namespace.</p>
                tags:
                  - Describe
                  - Namespaces
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/refresh-schedules/{ScheduleId}:
              GET:
                summary: DescribeRefreshSchedule
                description: <p>Provides a summary of a refresh schedule.</p>
                tags:
                  - Describe
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
            /accounts/{AwsAccountId}/namespaces/{Namespace}/roles/{Role}/custom-permission:
              PUT:
                summary: UpdateRoleCustomPermission
                description: >-
                  <p>Updates the custom permissions that are associated with a
                  role.</p>
                tags:
                  - Update
                  - Roles
                  - Custom
                  - Permission
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
            /accounts/{AwsAccountId}/topics/{TopicId}:
              PUT:
                summary: UpdateTopic
                description: <p>Updates a topic.</p>
                tags:
                  - Update
                  - Topics
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
            /accounts/{AwsAccountId}/topics/{TopicId}/schedules/{DatasetId}:
              PUT:
                summary: UpdateTopicRefreshSchedule
                description: <p>Updates a topic refresh schedule.</p>
                tags:
                  - Update
                  - Topics
                  - Refresh
                  - Schedules
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users/{UserName}:
              PUT:
                summary: UpdateUser
                description: <p>Updates an Amazon QuickSight user.</p>
                tags:
                  - Update
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
            /accounts/{AwsAccountId}/namespaces/{Namespace}/user-principals/{PrincipalId}:
              DELETE:
                summary: DeleteUserByPrincipalId
                description: <p>Deletes a user identified by its principal ID. </p>
                tags:
                  - Delete
                  - Users
                  - By
                  - Principals
                  - Identifiers
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
            /accounts/{AwsAccountId}/vpc-connections/{VPCConnectionId}:
              PUT:
                summary: UpdateVPCConnection
                description: <p>Updates a VPC connection.</p>
                tags:
                  - Update
                  - Connections
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
            /accounts/{AwsAccountId}/settings:
              PUT:
                summary: UpdateAccountSettings
                description: >-
                  <p>Updates the Amazon QuickSight settings in your Amazon Web
                  Services account.</p>
                tags:
                  - Update
                  - Account
                  - Settings
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
            /accounts/{AwsAccountId}/analyses/{AnalysisId}/definition:
              GET:
                summary: DescribeAnalysisDefinition
                description: >-
                  <p>Provides a detailed description of the definition of an
                  analysis.</p> <note> <p>If you do not need to know details
                  about the content of an Analysis, for instance if you are
                  trying to check the status of a recently created or updated
                  Analysis, use the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_DescribeAnalysis.html">
                  <code>DescribeAnalysis</code> </a> instead. </p> </note>
                tags:
                  - Describe
                  - Analysis
                  - Definitions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
            /accounts/{AwsAccountId}/analyses/{AnalysisId}/permissions:
              PUT:
                summary: UpdateAnalysisPermissions
                description: <p>Updates the read and write permissions for an analysis.</p>
                tags:
                  - Update
                  - Analysis
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
            /accounts/{AwsAccountId}/asset-bundle-export-jobs/{AssetBundleExportJobId}:
              GET:
                summary: DescribeAssetBundleExportJob
                description: >-
                  <p>Describes an existing export job.</p> <p>Poll job
                  descriptions after a job starts to know the status of the job.
                  When a job succeeds, a URL is provided to download the
                  exported assets' data from. Download URLs are valid for five
                  minutes after they are generated. You can call the
                  <code>DescribeAssetBundleExportJob</code> API for a new
                  download URL as needed.</p> <p>Job descriptions are available
                  for 14 days after the job starts.</p>
                tags:
                  - Describe
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
            /accounts/{AwsAccountId}/asset-bundle-import-jobs/{AssetBundleImportJobId}:
              GET:
                summary: DescribeAssetBundleImportJob
                description: >-
                  <p>Describes an existing import job.</p> <p>Poll job
                  descriptions after starting a job to know when it has
                  succeeded or failed. Job descriptions are available for 14
                  days after job starts.</p>
                tags:
                  - Describe
                  - Assets
                  - Bundles
                  - Import
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/definition:
              GET:
                summary: DescribeDashboardDefinition
                description: >-
                  <p>Provides a detailed description of the definition of a
                  dashboard.</p> <note> <p>If you do not need to know details
                  about the content of a dashboard, for instance if you are
                  trying to check the status of a recently created or updated
                  dashboard, use the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_DescribeDashboard.html">
                  <code>DescribeDashboard</code> </a> instead. </p> </note>
                tags:
                  - Describe
                  - Dashboard
                  - Definitions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/permissions:
              PUT:
                summary: UpdateDashboardPermissions
                description: <p>Updates read and write permissions on a dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/snapshot-jobs/{SnapshotJobId}:
              GET:
                summary: DescribeDashboardSnapshotJob
                description: >-
                  <p>Describes an existing snapshot job.</p> <p>Poll job
                  descriptions after a job starts to know the status of the job.
                  For information on available status codes, see
                  <code>JobStatus</code>.</p>
                tags:
                  - Describe
                  - Dashboard
                  - Snapshots
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/snapshot-jobs/{SnapshotJobId}/result:
              GET:
                summary: DescribeDashboardSnapshotJobResult
                description: >-
                  <p>Describes the result of an existing snapshot job that has
                  finished running.</p> <p>A finished snapshot job will return a
                  <code>COMPLETED</code> or <code>FAILED</code> status when you
                  poll the job with a <code>DescribeDashboardSnapshotJob</code>
                  API call.</p> <p>If the job has not finished running, this
                  operation returns a message that says <code>Dashboard Snapshot
                  Job with id &lt;SnapshotjobId&gt; has not reached a terminal
                  state.</code>.</p>
                tags:
                  - Describe
                  - Dashboard
                  - Snapshots
                  - Jobs
                  - Results
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/permissions:
              POST:
                summary: UpdateDataSetPermissions
                description: >-
                  <p>Updates the permissions on a dataset.</p> <p>The
                  permissions resource is
                  <code>arn:aws:quicksight:region:aws-account-id:dataset/data-set-id</code>.</p>
                tags:
                  - Update
                  - Data
                  - Sets
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/data-sources/{DataSourceId}/permissions:
              POST:
                summary: UpdateDataSourcePermissions
                description: <p>Updates the permissions to a data source.</p>
                tags:
                  - Update
                  - Data
                  - Source
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/folders/{FolderId}/permissions:
              PUT:
                summary: UpdateFolderPermissions
                description: <p>Updates permissions of a folder.</p>
                tags:
                  - Update
                  - Folder
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
            /accounts/{AwsAccountId}/folders/{FolderId}/resolved-permissions:
              GET:
                summary: DescribeFolderResolvedPermissions
                description: >-
                  <p>Describes the folder resolved permissions. Permissions
                  consists of both folder direct permissions and the inherited
                  permissions from the ancestor folders.</p>
                tags:
                  - Describe
                  - Folder
                  - Resolved
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
            /accounts/{AwsAccountId}/namespaces/{Namespace}/iam-policy-assignments/{AssignmentName}:
              PUT:
                summary: UpdateIAMPolicyAssignment
                description: >-
                  <p>Updates an existing IAM policy assignment. This operation
                  updates only the optional parameter or parameters that are
                  specified in the request. This overwrites all of the users
                  included in <code>Identities</code>. </p>
                tags:
                  - Update
                  - Policies
                  - Assignment
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
            /accounts/{AwsAccountId}/ip-restriction:
              POST:
                summary: UpdateIpRestriction
                description: >-
                  <p>Updates the content and status of IP rules. To use this
                  operation, you must provide the entire map of rules. You can
                  use the <code>DescribeIpRestriction</code> operation to get
                  the current rule map.</p>
                tags:
                  - Update
                  - IP
                  - Restrictions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/templates/{TemplateId}/definition:
              GET:
                summary: DescribeTemplateDefinition
                description: >-
                  <p>Provides a detailed description of the definition of a
                  template.</p> <note> <p>If you do not need to know details
                  about the content of a template, for instance if you are
                  trying to check the status of a recently created or updated
                  template, use the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_DescribeTemplate.html">
                  <code>DescribeTemplate</code> </a> instead. </p> </note>
                tags:
                  - Describe
                  - Templates
                  - Definitions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/templates/{TemplateId}/permissions:
              PUT:
                summary: UpdateTemplatePermissions
                description: <p>Updates the resource permissions for a template.</p>
                tags:
                  - Update
                  - Templates
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/themes/{ThemeId}/permissions:
              PUT:
                summary: UpdateThemePermissions
                description: >-
                  <p>Updates the resource permissions for a theme. Permissions
                  apply to the action to grant or revoke permissions on, for
                  example <code>"quicksight:DescribeTheme"</code>.</p> <p>Theme
                  permissions apply in groupings. Valid groupings include the
                  following for the three levels of permissions, which are user,
                  owner, or no permissions: </p> <ul> <li> <p>User</p> <ul> <li>
                  <p> <code>"quicksight:DescribeTheme"</code> </p> </li> <li>
                  <p> <code>"quicksight:DescribeThemeAlias"</code> </p> </li>
                  <li> <p> <code>"quicksight:ListThemeAliases"</code> </p> </li>
                  <li> <p> <code>"quicksight:ListThemeVersions"</code> </p>
                  </li> </ul> </li> <li> <p>Owner</p> <ul> <li> <p>
                  <code>"quicksight:DescribeTheme"</code> </p> </li> <li> <p>
                  <code>"quicksight:DescribeThemeAlias"</code> </p> </li> <li>
                  <p> <code>"quicksight:ListThemeAliases"</code> </p> </li> <li>
                  <p> <code>"quicksight:ListThemeVersions"</code> </p> </li>
                  <li> <p> <code>"quicksight:DeleteTheme"</code> </p> </li> <li>
                  <p> <code>"quicksight:UpdateTheme"</code> </p> </li> <li> <p>
                  <code>"quicksight:CreateThemeAlias"</code> </p> </li> <li> <p>
                  <code>"quicksight:DeleteThemeAlias"</code> </p> </li> <li> <p>
                  <code>"quicksight:UpdateThemeAlias"</code> </p> </li> <li> <p>
                  <code>"quicksight:UpdateThemePermissions"</code> </p> </li>
                  <li> <p> <code>"quicksight:DescribeThemePermissions"</code>
                  </p> </li> </ul> </li> <li> <p>To specify no permissions, omit
                  the permissions list.</p> </li> </ul>
                tags:
                  - Update
                  - Theme
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/topics/{TopicId}/permissions:
              PUT:
                summary: UpdateTopicPermissions
                description: <p>Updates the permissions of a topic.</p>
                tags:
                  - Update
                  - Topics
                  - Permissions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/topics/{TopicId}/refresh/{RefreshId}:
              GET:
                summary: DescribeTopicRefresh
                description: <p>Describes the status of a topic refresh.</p>
                tags:
                  - Describe
                  - Topics
                  - Refresh
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
            /accounts/{AwsAccountId}/embed-url/anonymous-user:
              POST:
                summary: GenerateEmbedUrlForAnonymousUser
                description: >-
                  <p>Generates an embed URL that you can use to embed an Amazon
                  QuickSight dashboard or visual in your website, without having
                  to register any reader users. Before you use this action, make
                  sure that you have configured the dashboards and
                  permissions.</p> <p>The following rules apply to the generated
                  URL:</p> <ul> <li> <p>It contains a temporary bearer token. It
                  is valid for 5 minutes after it is generated. Once redeemed
                  within this period, it cannot be re-used again.</p> </li> <li>
                  <p>The URL validity period should not be confused with the
                  actual session lifetime that can be customized using the
                  <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_GenerateEmbedUrlForAnonymousUser.html#QS-GenerateEmbedUrlForAnonymousUser-request-SessionLifetimeInMinutes">SessionLifetimeInMinutes</a>
                  </code> parameter. The resulting user session is valid for 15
                  minutes (minimum) to 10 hours (maximum). The default session
                  duration is 10 hours.</p> </li> <li> <p>You are charged only
                  when the URL is used or there is interaction with Amazon
                  QuickSight.</p> </li> </ul> <p>For more information, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics.html">Embedded
                  Analytics</a> in the <i>Amazon QuickSight User Guide</i>.</p>
                  <p>For more information about the high-level steps for
                  embedding and for an interactive demo of the ways you can
                  customize embedding, visit the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/quicksight-dev-portal.html">Amazon
                  QuickSight Developer Portal</a>.</p>
                tags:
                  - Generate
                  - Embed
                  - URL
                  - For
                  - Anonymous
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
            /accounts/{AwsAccountId}/embed-url/registered-user:
              POST:
                summary: GenerateEmbedUrlForRegisteredUser
                description: >-
                  <p>Generates an embed URL that you can use to embed an Amazon
                  QuickSight experience in your website. This action can be used
                  for any type of user registered in an Amazon QuickSight
                  account. Before you use this action, make sure that you have
                  configured the relevant Amazon QuickSight resource and
                  permissions.</p> <p>The following rules apply to the generated
                  URL:</p> <ul> <li> <p>It contains a temporary bearer token. It
                  is valid for 5 minutes after it is generated. Once redeemed
                  within this period, it cannot be re-used again.</p> </li> <li>
                  <p>The URL validity period should not be confused with the
                  actual session lifetime that can be customized using the
                  <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_GenerateEmbedUrlForRegisteredUser.html#QS-GenerateEmbedUrlForRegisteredUser-request-SessionLifetimeInMinutes">SessionLifetimeInMinutes</a>
                  </code> parameter.</p> <p>The resulting user session is valid
                  for 15 minutes (minimum) to 10 hours (maximum). The default
                  session duration is 10 hours.</p> </li> <li> <p>You are
                  charged only when the URL is used or there is interaction with
                  Amazon QuickSight.</p> </li> </ul> <p>For more information,
                  see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics.html">Embedded
                  Analytics</a> in the <i>Amazon QuickSight User Guide</i>.</p>
                  <p>For more information about the high-level steps for
                  embedding and for an interactive demo of the ways you can
                  customize embedding, visit the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/quicksight-dev-portal.html">Amazon
                  QuickSight Developer Portal</a>.</p>
                tags:
                  - Generate
                  - Embed
                  - URL
                  - For
                  - Registered
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/embed-url:
              GET:
                summary: GetDashboardEmbedUrl
                description: >-
                  <p>Generates a temporary session URL and authorization
                  code(bearer token) that you can use to embed an Amazon
                  QuickSight read-only dashboard in your website or application.
                  Before you use this command, make sure that you have
                  configured the dashboards and permissions. </p> <p>Currently,
                  you can use <code>GetDashboardEmbedURL</code> only from the
                  server, not from the user's browser. The following rules apply
                  to the generated URL:</p> <ul> <li> <p>They must be used
                  together.</p> </li> <li> <p>They can be used one time
                  only.</p> </li> <li> <p>They are valid for 5 minutes after you
                  run this command.</p> </li> <li> <p>You are charged only when
                  the URL is used or there is interaction with Amazon
                  QuickSight.</p> </li> <li> <p>The resulting user session is
                  valid for 15 minutes (default) up to 10 hours (maximum). You
                  can use the optional <code>SessionLifetimeInMinutes</code>
                  parameter to customize session duration.</p> </li> </ul>
                  <p>For more information, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics-deprecated.html">Embedding
                  Analytics Using GetDashboardEmbedUrl</a> in the <i>Amazon
                  QuickSight User Guide</i>.</p> <p>For more information about
                  the high-level steps for embedding and for an interactive demo
                  of the ways you can customize embedding, visit the <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/quicksight-dev-portal.html">Amazon
                  QuickSight Developer Portal</a>.</p>
                tags:
                  - Get
                  - Dashboard
                  - Embed
                  - URL
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
            /accounts/{AwsAccountId}/session-embed-url:
              GET:
                summary: GetSessionEmbedUrl
                description: >-
                  <p>Generates a session URL and authorization code that you can
                  use to embed the Amazon Amazon QuickSight console in your web
                  server code. Use <code>GetSessionEmbedUrl</code> where you
                  want to provide an authoring portal that allows users to
                  create data sources, datasets, analyses, and dashboards. The
                  users who access an embedded Amazon QuickSight console need
                  belong to the author or admin security cohort. If you want to
                  restrict permissions to some of these features, add a custom
                  permissions profile to the user with the <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_UpdateUser.html">UpdateUser</a>
                  </code> API operation. Use <code> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/APIReference/API_RegisterUser.html">RegisterUser</a>
                  </code> API operation to add a new user with a custom
                  permission profile attached. For more information, see the
                  following sections in the <i>Amazon QuickSight User
                  Guide</i>:</p> <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/embedded-analytics.html">Embedding
                  Analytics</a> </p> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/customizing-permissions-to-the-quicksight-console.html">Customizing
                  Access to the Amazon QuickSight Console</a> </p> </li> </ul>
                tags:
                  - Get
                  - Sessions
                  - Embed
                  - URL
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/analyses:
              GET:
                summary: ListAnalyses
                description: >-
                  <p>Lists Amazon QuickSight analyses that exist in the
                  specified Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/asset-bundle-export-jobs:
              GET:
                summary: ListAssetBundleExportJobs
                description: >-
                  <p>Lists all asset bundle export jobs that have been taken
                  place in the last 14 days. Jobs created more than 14 days ago
                  are deleted forever and are not returned. If you are using the
                  same job ID for multiple jobs,
                  <code>ListAssetBundleExportJobs</code> only returns the most
                  recent job that uses the repeated job ID.</p>
                tags:
                  - Lists
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/asset-bundle-import-jobs:
              GET:
                summary: ListAssetBundleImportJobs
                description: >-
                  <p>Lists all asset bundle import jobs that have taken place in
                  the last 14 days. Jobs created more than 14 days ago are
                  deleted forever and are not returned. If you are using the
                  same job ID for multiple jobs,
                  <code>ListAssetBundleImportJobs</code> only returns the most
                  recent job that uses the repeated job ID.</p>
                tags:
                  - Lists
                  - Assets
                  - Bundles
                  - Import
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/versions:
              GET:
                summary: ListDashboardVersions
                description: >-
                  <p>Lists all the versions of the dashboards in the Amazon
                  QuickSight subscription.</p>
                tags:
                  - Lists
                  - Dashboard
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/dashboards:
              GET:
                summary: ListDashboards
                description: <p>Lists dashboards in an Amazon Web Services account.</p>
                tags:
                  - Lists
                  - Dashboards
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/folders/{FolderId}/members:
              GET:
                summary: ListFolderMembers
                description: >-
                  <p>List all assets (<code>DASHBOARD</code>,
                  <code>ANALYSIS</code>, and <code>DATASET</code>) in a folder.
                  </p>
                tags:
                  - Lists
                  - Folder
                  - Members
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/folders:
              GET:
                summary: ListFolders
                description: <p>Lists all folders in an account.</p>
                tags:
                  - Lists
                  - Folders
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups/{GroupName}/members:
              GET:
                summary: ListGroupMemberships
                description: <p>Lists member users in a group.</p>
                tags:
                  - Lists
                  - Group
                  - Memberships
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
            /accounts/{AwsAccountId}/namespaces/{Namespace}/v2/iam-policy-assignments:
              GET:
                summary: ListIAMPolicyAssignments
                description: >-
                  <p>Lists the IAM policy assignments in the current Amazon
                  QuickSight account.</p>
                tags:
                  - Lists
                  - Policies
                  - Assignments
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users/{UserName}/iam-policy-assignments:
              GET:
                summary: ListIAMPolicyAssignmentsForUser
                description: >-
                  <p>Lists all of the IAM policy assignments, including the
                  Amazon Resource Names (ARNs), for the IAM policies assigned to
                  the specified user and group, or groups that the user belongs
                  to.</p>
                tags:
                  - Lists
                  - Policies
                  - Assignments
                  - For
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/identity-propagation-config:
              GET:
                summary: ListIdentityPropagationConfigs
                description: >-
                  <p>Lists all services and authorized targets that the Amazon
                  QuickSight IAM Identity Center application can access.</p>
                  <p>This operation is only supported for Amazon QuickSight
                  accounts that use IAM Identity Center.</p>
                tags:
                  - Lists
                  - Identity
                  - Propagation
                  - Configurations
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/data-sets/{DataSetId}/ingestions:
              GET:
                summary: ListIngestions
                description: <p>Lists the history of SPICE ingestions for a dataset.</p>
                tags:
                  - Lists
                  - Ingestions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/namespaces:
              GET:
                summary: ListNamespaces
                description: >-
                  <p>Lists the namespaces for the specified Amazon Web Services
                  account. This operation doesn't list deleted namespaces.</p>
                tags:
                  - Lists
                  - Namespaces
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /accounts/{AwsAccountId}/namespaces/{Namespace}/roles/{Role}/members:
              GET:
                summary: ListRoleMemberships
                description: <p>Lists all groups that are associated with a role.</p>
                tags:
                  - Lists
                  - Roles
                  - Memberships
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
            /resources/{ResourceArn}/tags:
              DELETE:
                summary: UntagResource
                description: <p>Removes a tag or tags from a resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/templates/{TemplateId}/aliases:
              GET:
                summary: ListTemplateAliases
                description: <p>Lists all the aliases of a template.</p>
                tags:
                  - Lists
                  - Templates
                  - Aliases
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/templates/{TemplateId}/versions:
              GET:
                summary: ListTemplateVersions
                description: >-
                  <p>Lists all the versions of the templates in the current
                  Amazon QuickSight account.</p>
                tags:
                  - Lists
                  - Templates
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/templates:
              GET:
                summary: ListTemplates
                description: >-
                  <p>Lists all the templates in the current Amazon QuickSight
                  account.</p>
                tags:
                  - Lists
                  - Templates
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/themes/{ThemeId}/aliases:
              GET:
                summary: ListThemeAliases
                description: <p>Lists all the aliases of a theme.</p>
                tags:
                  - Lists
                  - Theme
                  - Aliases
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/themes/{ThemeId}/versions:
              GET:
                summary: ListThemeVersions
                description: >-
                  <p>Lists all the versions of the themes in the current Amazon
                  Web Services account.</p>
                tags:
                  - Lists
                  - Theme
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/themes:
              GET:
                summary: ListThemes
                description: >-
                  <p>Lists all the themes in the current Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Themes
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users/{UserName}/groups:
              GET:
                summary: ListUserGroups
                description: >-
                  <p>Lists the Amazon QuickSight groups that an Amazon
                  QuickSight user is a member of.</p>
                tags:
                  - Lists
                  - Users
                  - Groups
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/namespaces/{Namespace}/users:
              POST:
                summary: RegisterUser
                description: >-
                  <p>Creates an Amazon QuickSight user whose identity is
                  associated with the Identity and Access Management (IAM)
                  identity or role specified in the request. When you register a
                  new user from the Amazon QuickSight API, Amazon QuickSight
                  generates a registration URL. The user accesses this
                  registration URL to create their account. Amazon QuickSight
                  doesn't send a registration email to users who are registered
                  from the Amazon QuickSight API. If you want new users to
                  receive a registration email, then add those users in the
                  Amazon QuickSight console. For more information on registering
                  a new user in the Amazon QuickSight console, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/managing-users.html#inviting-users">
                  Inviting users to access Amazon QuickSight</a>.</p>
                tags:
                  - Register
                  - Users
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
            /accounts/{AwsAccountId}/restore/analyses/{AnalysisId}:
              POST:
                summary: RestoreAnalysis
                description: <p>Restores an analysis.</p>
                tags:
                  - Restore
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
            /accounts/{AwsAccountId}/search/analyses:
              POST:
                summary: SearchAnalyses
                description: >-
                  <p>Searches for analyses that belong to the user specified in
                  the filter.</p> <note> <p>This operation is eventually
                  consistent. The results are best effort and may not reflect
                  very recent updates and changes.</p> </note>
                tags:
                  - Search
                  - Analysis
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/dashboards:
              POST:
                summary: SearchDashboards
                description: >-
                  <p>Searches for dashboards that belong to a user. </p> <note>
                  <p>This operation is eventually consistent. The results are
                  best effort and may not reflect very recent updates and
                  changes.</p> </note>
                tags:
                  - Search
                  - Dashboards
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/data-sets:
              POST:
                summary: SearchDataSets
                description: >-
                  <p>Use the <code>SearchDataSets</code> operation to search for
                  datasets that belong to an account.</p>
                tags:
                  - Search
                  - Data
                  - Sets
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/data-sources:
              POST:
                summary: SearchDataSources
                description: >-
                  <p>Use the <code>SearchDataSources</code> operation to search
                  for data sources that belong to an account.</p>
                tags:
                  - Search
                  - Data
                  - Sources
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/search/folders:
              POST:
                summary: SearchFolders
                description: <p>Searches the subfolders in a folder.</p>
                tags:
                  - Search
                  - Folders
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/namespaces/{Namespace}/groups-search:
              POST:
                summary: SearchGroups
                description: >-
                  <p>Use the <code>SearchGroups</code> operation to search
                  groups in a specified Amazon QuickSight namespace using the
                  supplied filters.</p>
                tags:
                  - Search
                  - Groups
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/asset-bundle-export-jobs/export:
              POST:
                summary: StartAssetBundleExportJob
                description: >-
                  <p>Starts an Asset Bundle export job.</p> <p>An Asset Bundle
                  export job exports specified Amazon QuickSight assets. You can
                  also choose to export any asset dependencies in the same job.
                  Export jobs run asynchronously and can be polled with a
                  <code>DescribeAssetBundleExportJob</code> API call. When a job
                  is successfully completed, a download URL that contains the
                  exported assets is returned. The URL is valid for 5 minutes
                  and can be refreshed with a
                  <code>DescribeAssetBundleExportJob</code> API call. Each
                  Amazon QuickSight account can run up to 5 export jobs
                  concurrently.</p> <p>The API caller must have the necessary
                  permissions in their IAM role to access each resource before
                  the resources can be exported.</p>
                tags:
                  - Start
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/asset-bundle-import-jobs/import:
              POST:
                summary: StartAssetBundleImportJob
                description: >-
                  <p>Starts an Asset Bundle import job.</p> <p>An Asset Bundle
                  import job imports specified Amazon QuickSight assets into an
                  Amazon QuickSight account. You can also choose to import a
                  naming prefix and specified configuration overrides. The
                  assets that are contained in the bundle file that you provide
                  are used to create or update a new or existing asset in your
                  Amazon QuickSight account. Each Amazon QuickSight account can
                  run up to 5 import jobs concurrently.</p> <p>The API caller
                  must have the necessary <code>"create"</code>,
                  <code>"describe"</code>, and <code>"update"</code> permissions
                  in their IAM role to access each resource type that is
                  contained in the bundle file before the resources can be
                  imported.</p>
                tags:
                  - Start
                  - Assets
                  - Bundles
                  - Import
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/snapshot-jobs:
              POST:
                summary: StartDashboardSnapshotJob
                description: >-
                  <p>Starts an asynchronous job that generates a dashboard
                  snapshot. You can request one of the following format
                  configurations per API call.</p> <ul> <li> <p>1 paginated
                  PDF</p> </li> <li> <p>1 Excel workbook</p> </li> <li> <p>5
                  CSVs</p> </li> </ul> <p>Poll job descriptions with a
                  <code>DescribeDashboardSnapshotJob</code> API call. Once the
                  job succeeds, use the
                  <code>DescribeDashboardSnapshotJobResult</code> API to obtain
                  the download URIs that the job generates.</p>
                tags:
                  - Start
                  - Dashboard
                  - Snapshots
                  - Jobs
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/linked-entities:
              PUT:
                summary: UpdateDashboardLinks
                description: <p>Updates the linked analyses on a dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Links
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
                  - Linked
                  - Entities
            /accounts/{AwsAccountId}/dashboards/{DashboardId}/versions/{VersionNumber}:
              PUT:
                summary: UpdateDashboardPublishedVersion
                description: <p>Updates the published version of a dashboard.</p>
                tags:
                  - Update
                  - Dashboard
                  - Published
                  - Versions
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
                  - Linked
                  - Entities
                  - Versions
                  - Numbers
            /accounts/{AwsAccountId}/public-sharing-settings:
              PUT:
                summary: UpdatePublicSharingSettings
                description: >-
                  <p>Use the <code>UpdatePublicSharingSettings</code> operation
                  to turn on or turn off the public sharing settings of an
                  Amazon QuickSight dashboard.</p> <p>To use this operation,
                  turn on session capacity pricing for your Amazon QuickSight
                  account.</p> <p>Before you can turn on public sharing on your
                  account, make sure to give public sharing permissions to an
                  administrative user in the Identity and Access Management
                  (IAM) console. For more information on using IAM with Amazon
                  QuickSight, see <a
                  href="https://docs.aws.amazon.com/quicksight/latest/user/security_iam_service-with-iam.html">Using
                  Amazon QuickSight with IAM</a> in the <i>Amazon QuickSight
                  User Guid
                tags:
                  - Update
                  - Public
                  - Sharing
                  - Settings
                  - Aws
                  - Account
                  - Identifiers
                  - Data
                  - Sets
                  - Sets
                  - Ingestions
                  - Ingestion
                  - Customizations
                  - Analysis
                  - Analysis
                  - Dashboards
                  - Dashboard
                  - Sources
                  - Folders
                  - Folder
                  - Members
                  - Members
                  - Types
                  - Namespaces
                  - Namespaces
                  - Groups
                  - Group
                  - Names
                  - IAM
                  - Policies
                  - Assignments
                  - Refresh
                  - Schedules
                  - Roles
                  - Roles
                  - Templates
                  - Templates
                  - Aliases
                  - Alias
                  - Themes
                  - Theme
                  - Topics
                  - Topics
                  - VPC
                  - Connections
                  - Properties
                  - Source
                  - Assignment
                  - Identity
                  - Propagation
                  - Configurations
                  - Services
                  - Schedules
                  - Custom
                  - Permission
                  - Datasets
                  - Users
                  - Users
                  - Principals
                  - Principals
                  - Connections
                  - Settings
                  - Definitions
                  - Permissions
                  - Assets
                  - Bundles
                  - Export
                  - Jobs
                  - Jobs
                  - Import
                  - Snapshots
                  - Results
                  - Resolved
                  - IP
                  - Restrictions
                  - Embed
                  - URL
                  - Anonymous
                  - Registered
                  - Sessions
                  - Versions
                  - V2
                  - Resources
                  - ARN
                  - Tags
                  - Restore
                  - Search
                  - Linked
                  - Entities
                  - Versions
                  - Numbers
                  - Public
                  - Shari
    overlays:
      - type: APIs.io Search
        url: overlays/quicksight-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/quicksight-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:quicksight
  - aid: twilio:twilio-numbers-api
    name: Twilio Numbers API
    description: Needs description.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.twilio.com/docs/
    baseURL: https:/api.twilio.com
    tags: []
    properties:
      - type: Documentation
        url: https://www.twilio.com/docs/
      - type: OpenAPI
        data:
          info:
            title: Twilio - Numbers
            license:
              name: Apache 2.0
              url: https://www.apache.org/licenses/LICENSE-2.0.html
          openapi: 3.0.1
          paths:
            /v2/HostedNumber/AuthorizationDocuments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific AuthorizationDocument.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
              delete:
                description: Cancel the AuthorizationDocument request.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
            /v2/HostedNumber/AuthorizationDocuments:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve a list of AuthorizationDocuments belonging to the
                  account initiating the request.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
              post:
                description: >-
                  Create an AuthorizationDocument for authorizing the hosting of
                  phone number capabilities on Twilio's platform.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
            /v2/HostedNumber/Orders/Bulk/{BulkHostingSid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific BulkHostedNumberOrder.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
            /v2/HostedNumber/Orders/Bulk:
              description: 'TODO: Resource-level docs'
            /v2/RegulatoryCompliance/Bundles:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Bundle.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
              get:
                description: Retrieve a list of all Bundles for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
            /v2/RegulatoryCompliance/Bundles/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Bundle instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
              post:
                description: Updates a Bundle in an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
              delete:
                description: Delete a specific Bundle.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/Copies:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Creates a new copy of a Bundle. It will internally create
                  copies of all the bundle items (identities and documents) of
                  the original bundle
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
              get:
                description: Retrieve a list of all Bundles Copies for a Bundle.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
            /v2/HostedNumber/AuthorizationDocuments/{SigningDocumentSid}/DependentHostedNumberOrders:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve a list of dependent HostedNumberOrders belonging to
                  the AuthorizationDocument.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
            /v2/RegulatoryCompliance/EndUsers:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new End User.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
              get:
                description: Retrieve a list of all End User for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
            /v2/RegulatoryCompliance/EndUsers/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific End User Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
              post:
                description: Update an existing End User.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
              delete:
                description: Delete a specific End User.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
            /v2/RegulatoryCompliance/EndUserTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all End-User Types.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
            /v2/RegulatoryCompliance/EndUserTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific End-User Type Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/Evaluations:
              description: 'TODO: Resource-level docs'
              post:
                description: Creates an evaluation for a bundle
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
              get:
                description: >-
                  Retrieve a list of Evaluations associated to the Bundle
                  resource.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/Evaluations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Evaluation Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/HostedNumber/Orders/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific HostedNumberOrder.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
              delete:
                description: >-
                  Cancel the HostedNumberOrder (only available when the status
                  is in `received`).
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/HostedNumber/Orders:
              description: 'TODO: Resource-level docs'
              get:
                description: >-
                  Retrieve a list of HostedNumberOrders belonging to the account
                  initiating the request.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
              post:
                description: Host a phone number's capability on Twilio's platform.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/ItemAssignments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Assigned Item.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
              get:
                description: Retrieve a list of all Assigned Items for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/ItemAssignments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Assigned Item Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
              delete:
                description: Remove an Assignment Item Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
            /v2/RegulatoryCompliance/Regulations:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Regulations.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
            /v2/RegulatoryCompliance/Regulations/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Regulation Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
            /v2/RegulatoryCompliance:
              description: 'TODO: Resource-level docs'
            /v2/RegulatoryCompliance/Bundles/{BundleSid}/ReplaceItems:
              description: 'TODO: Resource-level docs'
              post:
                description: >-
                  Replaces all bundle items in the target bundle (specified in
                  the path) with all the bundle items of the source bundle
                  (specified by the from_bundle_sid body param)
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
            /v2/RegulatoryCompliance/SupportingDocuments:
              description: 'TODO: Resource-level docs'
              post:
                description: Create a new Supporting Document.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
              get:
                description: Retrieve a list of all Supporting Document for an account.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
            /v2/RegulatoryCompliance/SupportingDocuments/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch specific Supporting Document Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
              post:
                description: Update an existing Supporting Document.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
              delete:
                description: Delete a specific Supporting Document.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
            /v2/RegulatoryCompliance/SupportingDocumentTypes:
              description: 'TODO: Resource-level docs'
              get:
                description: Retrieve a list of all Supporting Document Types.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
            /v2/RegulatoryCompliance/SupportingDocumentTypes/{Sid}:
              description: 'TODO: Resource-level docs'
              get:
                description: Fetch a specific Supporting Document Type Instance.
                tags:
                  - Hosted
                  - Number
                  - Authorization
                  - Documents
                  - Sid
                  - Orders
                  - Bulk
                  - Hosting
                  - Regulatory
                  - Compliance
                  - Bundles
                  - Bundle
                  - Copies
                  - Signing
                  - Document
                  - Dependent
                  - End
                  - Users
                  - User
                  - Types
                  - Evaluations
                  - Item
                  - Assignments
                  - Regulations
                  - Replace
                  - Items
                  - Supporting
          tags:
            - name: NumbersV2AuthorizationDocument
            - name: NumbersV2BulkHostedNumberOrder
            - name: NumbersV2Bundle
            - name: NumbersV2BundleCopy
            - name: NumbersV2DependentHostedNumberOrder
            - name: NumbersV2EndUser
            - name: NumbersV2EndUserType
            - name: NumbersV2Evaluation
            - name: NumbersV2HostedNumberOrder
            - name: NumbersV2ItemAssignment
            - name: NumbersV2Regulation
            - name: NumbersV2ReplaceItems
            - name: NumbersV2SupportingDocument
            - name: NumbersV2SupportingDocumentType
          x-maturity:
            - name: GA
              description: This product is Generally Available.
            - name: Beta
              description: >-
                PLEASE NOTE that this is a Beta product that is subject to
                change. U
    overlays:
      - type: APIs.io Search
        url: overlays/numbers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/numbers-openapi-api-evangelist-ratings.yml
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---